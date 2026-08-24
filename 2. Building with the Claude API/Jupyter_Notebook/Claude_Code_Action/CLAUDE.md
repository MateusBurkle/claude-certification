# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

`app_starter/` is a Python package ("Document Tools") that implements document-related tools exposed through an **MCP (Model Context Protocol) server**, so they can be called by AI assistants. The server is built with `mcp[cli]` (`FastMCP`).

## Commands

Run all commands from `app_starter/` (that directory is the actual Python project — `pyproject.toml` lives there, not at the repo root).

```bash
# Create venv and install the package in editable mode
uv venv
uv pip install -e .

# Start the MCP server
uv run main.py

# Run all tests
uv run pytest

# Run a single test
uv run pytest tests/test_document.py::TestBinaryDocumentToMarkdown::test_binary_document_to_markdown_with_docx
```

There is no separate build or lint command configured in this project.

### Windows / OneDrive note

This repo lives under OneDrive on Windows, where `uv`'s default hardlink install mode fails with `error: Failed to install ... failed to hardlink file ... incompatible links` (OneDrive doesn't support hardlinks for files it syncs). If you hit that, set copy mode first:

```bash
export UV_LINK_MODE=copy
```

## Architecture

- **`main.py`** — the MCP server entrypoint. It creates a `FastMCP("docs")` instance and explicitly registers each tool function with `mcp.tool()(function)`. A function in `tools/` is *not* callable by an assistant until it's registered here — currently only `add` (from `tools/math.py`) is registered, even though `tools/document.py` defines `binary_document_to_markdown`.
- **`tools/`** — plain Python functions implementing the actual tool logic, one module per tool domain (`math.py`, `document.py`). These are pure functions with no MCP-specific code in them; MCP wiring happens only in `main.py`.
- **`tools/document.py`** — uses `markitdown` (`MarkItDown`) to convert binary document data (docx, pdf, etc., read into a `BytesIO`) into markdown text via `StreamInfo(extension=file_type)`.
- **`tests/`** — pytest tests mirroring the `tools/` modules (e.g. `tests/test_document.py` tests `tools/document.py`). `tests/fixtures/` holds real sample documents (`mcp_docs.docx`, `mcp_docs.pdf`) used as test input rather than mocks.

## Code conventions

- Always apply appropriate type hints to function arguments (and return types), as already done throughout `tools/` (e.g. `binary_data: bytes, file_type: str) -> str` in `tools/document.py`, `a: float, b: float) -> float` in `tools/math.py`).

## Defining new MCP tools

This is the pattern the codebase follows (from `app_starter/README.md` and `tools/math.py`):

1. Write the tool as a plain Python function in the appropriate `tools/*.py` module.
2. Type each parameter and give it a `pydantic.Field(description=...)` default so the MCP schema carries a description per argument:

   ```python
   from pydantic import Field

   def my_tool(
       param1: str = Field(description="Detailed description of this parameter"),
       param2: int = Field(description="Explain what this parameter does"),
   ) -> ReturnType:
       """Comprehensive docstring here"""
       ...
   ```

3. Write a docstring that:
   - Begins with a one-line summary
   - Gives a detailed explanation of the functionality
   - Explains when to use (and when *not* to use) the tool
   - Includes usage examples with expected input/output (see `add`'s doctest-style examples in `tools/math.py`)
4. Register the function in `main.py` with `mcp.tool()(my_function)`.
5. Add a corresponding test under `tests/`, following the existing per-module test file convention.
