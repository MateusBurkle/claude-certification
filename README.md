# Claude Certification — Study Repository

Repositório com o material de estudo, notebooks práticos e anotações da minha preparação para a certificação da Anthropic (Anthropic Academy).

## 📁 Estrutura de pastas

```
Claude_Curso/
├── 1.Introduction to agent skills/
└── 2. Building with the Claude API/
```

### `1.Introduction to agent skills/`

Material do Curso 1 (concluído): um `.docx` por aula, uma planilha `weak_topics_tracking_1.xlsx` com o acompanhamento de acertos/erros, e um `.docx` de rodada de reforço.

### `2. Building with the Claude API/`

Material do Curso 2 (em andamento), dividido em três tipos de conteúdo:

- **`Modulo2_XX_*.docx`** — os documentos de estudo, um por seção do curso (ex: `Modulo2_05_Tool_Use_with_Claude.docx`). Cada um reúne todas as aulas daquela seção, com resumo, diagramas e questões de múltipla escolha.
- **`BRIEFING_Contexto/`** — contém o `BRIEFING_Estudo_Certificacao_Claude.md`, o arquivo de contexto que uso para retomar o trabalho em um novo chat (formato dos documentos, progresso por seção, pontos fracos, etc.).
- **`VoyageAI_API_Key_Directions.pdf`** — guia oficial da Voyage para gerar uma API key (usada nos exercícios de embeddings/RAG).

#### `Jupyter_Notebook/`

Pasta principal de exercícios práticos, organizada por tópico:

| Pasta | Conteúdo |
|---|---|
| `requests/`, `streaming/`, `temperature/` | Notebooks das aulas iniciais de request flow, streaming e temperature |
| `Prompt_Engeerning/`, `Prompt_Evals/` | Prompt engineering e avaliação de prompts |
| `Tools/` | Tool use — funções, schemas, streaming com tools, web search |
| `RAG/` | Chunking, embeddings, vector DB, BM25, hybrid search |
| `Features_of_Claude/` | Extended thinking, image support, citations, documents |
| `Control_Output/` | Controle de formato/estrutura de saída |

O arquivo **`.env`** com as chaves de API fica dentro desta pasta (`Jupyter_Notebook/.env`), pois é o diretório a partir do qual os notebooks chamam `load_dotenv()`. Esse arquivo **não é versionado** (está no `.gitignore`).

#### `Banco Arquivos Jupyter Notebook/`

Cópia de referência de notebooks de etapas anteriores do curso (request flow, prompt eval, streaming, temperature), mantida como backup/histórico separado da pasta de trabalho principal.

## 🔑 Como configurar as chaves de API

Os notebooks usam duas chaves, carregadas via [`python-dotenv`](https://pypi.org/project/python-dotenv/) a partir de um arquivo `.env`.

**1. Instale as dependências:**

```bash
pip install anthropic voyageai python-dotenv
```

**2. Consiga suas chaves:**

- **Anthropic:** crie uma conta e uma chave em [console.anthropic.com](https://console.anthropic.com). É necessário ter **billing configurado** (mesmo com crédito pequeno) — sem isso a API recusa a chave com erro de autenticação mesmo que ela esteja correta.
- **Voyage AI:** siga o passo a passo em `2. Building with the Claude API/VoyageAI_API_Key_Directions.pdf` (usada nos notebooks de embeddings/RAG).

**3. Crie o arquivo `.env`:**

Dentro de `2. Building with the Claude API/Jupyter_Notebook/`, crie um arquivo chamado `.env` com o seguinte conteúdo:

```env
ANTHROPIC_API_KEY=coloque_sua_chave_da_anthropic_aqui
VOYAGE_API_KEY=coloque_sua_chave_da_voyage_aqui
```

**4. Pronto.** No início de cada notebook, a chamada `load_dotenv()` carrega essas variáveis automaticamente, e `Anthropic()` / `voyageai.Client()` as usam sem precisar passar a chave manualmente no código.

> ⚠️ **Nunca** commite o arquivo `.env` nem cole sua chave em texto, print ou notebook. Ele já está no `.gitignore` — mantenha assim.
