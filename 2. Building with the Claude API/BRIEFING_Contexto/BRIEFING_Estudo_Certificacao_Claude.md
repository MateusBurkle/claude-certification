# 📋 Briefing — Preparação Certificação Anthropic (Claude)

> **Como usar:** anexe este arquivo no início de um novo chat e diga "Leia o briefing, vamos continuar". Isso dá ao assistente todo o contexto do que estamos fazendo.
> 
> *Última atualização: 24/08/2026 — Seção 7 (Features of Claude) concluída com 8 aulas. Seção 8 (Model Context Protocol) concluída com 11 aulas (Introducing MCP; MCP Clients; Project Setup; Defining Tools with MCP; The Server Inspector; Implementing a Client; Defining Resources; Accessing Resources; Defining Prompts; Prompts in the Client; MCP Review).*

---

## 🎯 Objetivo geral

Estou me preparando para tirar uma **certificação da Anthropic** (prova em **inglês**). Estou fazendo os cursos da Anthropic Academy e, a cada aula, o assistente gera material de estudo pra mim.

Ordem dos cursos que estou seguindo:

1. Introduction to Agent Skills ✅ **(concluído)**
2. **Building with the Claude API** ⬅️ *estou aqui (Módulo 2)*
3. Introduction to Model Context Protocol
4. Claude Code in Action

---

## 📄 Formato dos documentos de estudo (IMPORTANTE — seguir à risca)

Para cada aula que eu enviar (colo o texto + imagens da aula), gere um documento **.docx** com:

- **Fonte:** Ink Free (aparência manuscrita; é fonte do Windows, funciona no meu Word)
- **Idioma:** tudo em **inglês** (resumo e perguntas), pois a prova é em inglês
- **Estrutura do resumo (dinâmico e enxuto — NÃO um ensaio):**
  - **Core idea** — 1-2 frases com a ideia central
  - **Key points** — bullets curtos com termos-chave em **destaque**
  - **Conceitos essenciais** — um subtítulo por seção/bloco que a própria aula já tinha (usar os nomes originais da aula, não inventar agrupamentos novos); cada um com **parágrafo curto de 3-5 frases** (~60-100 palavras) — parafrasear de perto o que a aula diz, sem camadas extras de análise/interpretação
  - **Diagramas e tabelas ficam intercalados no texto**, logo depois do parágrafo a que se referem — nunca em um bloco único de "Diagramas"/"Tabelas" no fim da aula. Usar as imagens reais que eu mandar na conversa (embutidas no docx), com legenda; não recriar do zero
  - **Tabelas** — pequenas, só para conteúdo genuinamente comparativo/listável
- **Perguntas:** **5 questões** de múltipla escolha, alternativas **A a E**, SEM gabarito no documento
- **Gabarito:** só quando eu enviar minhas respostas → aí corrige, explica cada erro e registra no tracking
- **Foco no que é NOVO:** ao adicionar uma aula, não redocumentar conceitos/diagramas que já estão em aulas anteriores da mesma seção — só o que a aula acrescenta.
- **Referência de densidade:** o padrão certo é o do `Modulo2_03_Prompt_Evaluation.docx` (Seção 3) — resumos objetivos e próximos do texto original da aula. Se um resumo de aula ficar visivelmente mais "inchado"/analítico que as aulas anteriores da mesma seção, é sinal de que fugiu do padrão — comparar densidade com a aula anterior antes de fechar o documento.

### Organização em documentos-mãe por SEÇÃO

- **1 documento por seção do curso** (não 1 por aula). Cada aula vira uma subseção dentro do documento-mãe, com índice (Contents) no topo.
- Quando eu adicionar uma aula a uma seção existente, **eu reanexo o .docx da seção** e o assistente adiciona a nova aula no fim + atualiza o índice.
- Ao trocar de seção, começa **um documento-mãe novo** (não continua no da seção anterior).
- Formatação a seguir sempre: fonte Ink Free; título da aula em marrom escuro (`#5A3E1B`, negrito); subtítulos (Core idea, Key points, cada conceito, Practice Questions) em marrom claro (`#7A5A2E`, negrito); termos-chave em negrito `#5A3E1B` dentro dos bullets; tabelas com borda preta simples, sem sombreamento; legendas de imagem em itálico cinza (`#888888`); perguntas de prática em fonte Arial. (Padrão confirmado a partir do `Modulo2_03_Prompt_Evaluation.docx`.)

### Seções do Curso 2 (Building with the Claude API) — 10 no total:

1. Anthropic Overview → `Modulo2_01_Anthropic_Overview.docx` ✅ **concluída**
2. Accessing Claude with the API → `Modulo2_02_Accessing_Claude_with_the_API.docx` ✅ **concluída (7 aulas, 39 páginas)**
3. Prompt Evaluation → `Modulo2_03_Prompt_Evaluation.docx` ✅ **concluída (6 aulas)**
4. Prompt Engineering Techniques → `Modulo2_04_Prompt_Engineering_Techniques.docx` ✅ **concluída (5 aulas)**
5. Tool Use with Claude → `Modulo2_05_Tool_Use_with_Claude.docx` ✅ **concluída (6 aulas)**
6. RAG and Agentic Search → `Modulo2_06_RAG_and_Agentic_Search.docx` ✅ **concluída (7 aulas)**
7. Features of Claude → `Modulo2_07_Features_of_Claude.docx` ✅ **concluída (8 aulas)**
8. Model Context Protocol → `Modulo2_08_Model_Context_Protocol.docx` ✅ **concluída (11 aulas, 44 páginas)**
9. **Anthropic Apps — Claude Code and Computer Use** ⬅️ *próxima seção*
10. Agents and Workflows

*(O curso tem ~86 aulas no total distribuídas nessas seções.)*

### Conteúdo da Seção 2 (concluída) — para referência

1. The Request Flow & How Claude Processes It
2. Making Your First API Request
3. Multi-Turn Conversations
4. System Prompts
5. Temperature
6. Response Streaming
7. Structured Data

### Conteúdo da Seção 3 (concluída) — para referência

1. Prompt Evaluation — engineering vs evaluation; as 3 opções após escrever um prompt
2. A Typical Eval Workflow — os 5 passos; grader; média como métrica objetiva
3. Generating Test Datasets — goal/input/output; meta-prompt para gerar o dataset; Haiku
4. Running the Eval — `run_prompt`, `run_test_case`, `run_eval`; score hardcoded 10
5. Model-Based Grading — code/model/human graders; critérios; `grade_by_model`; média com `statistics.mean`
6. Code Based Grading — code grader (Format, Valid Syntax) vs model grader (Task Following); `validate_json`/`validate_python`/`validate_regex`; campo `"format"` no dataset; pre-fill genérico ```` ```code ````; score combinado `(model_score + syntax_score) / 2`

### Conteúdo da Seção 4 (concluída) — para referência

1. Prompt Engineering — ciclo iterativo (set a goal → write → evaluate → apply technique → re-evaluate); `PromptEvaluator`, `max_concurrent_tasks`, `generate_dataset()`, `extra_criteria`
2. Being Clear and Direct — clareza (linguagem simples) vs. diretividade (instrução + verbo de ação); score 2.32 → 3.92
3. Being Specific — output guidelines vs. process steps; quando usar cada um; score 3.92 → 7.86
4. Structure with XML Tags — tags descritivas como delimitadores (`<sales_records>`, `<my_code>`/`<docs>`, `<athlete_information>`)
5. Providing Examples — one-shot/multi-shot; `<sample_input>`/`<ideal_output>`; tirar exemplos das notas mais altas da própria avaliação; explicar por que o output é ideal

### Conteúdo da Seção 5 (concluída) — para referência

1. Introducing Tool Use — problema sem tools (Claude não tem acesso a dados externos/tempo real); fluxo de 4 passos (Initial Request → Tool Request → Data Retrieval → Final Response); exemplo do clima aplicando o fluxo genérico; benefícios-chave (real-time information, external system integration, dynamic responses, structured interaction)
2. Project Overview: Reminder Tool — projeto prático de reminders ("Set a reminder for my doctor's appointment..."); 3 limitações do Claude (hora exata, soma de datas, não sabe setar reminder); 3 ferramentas a implementar (get current date time, add duration to date time, set a reminder), construídas uma por vez começando pela mais simples
3. Tool Function — definição (função Python plain executada quando Claude decide que precisa de dado extra); boas práticas (nomes descritivos, validar inputs, mensagens de erro que o Claude usa para retry); implementação de `get_current_datetime(date_format=...)` com validação e exemplos de uso; próximo passo é escrever o JSON schema
4. Tool Schemas — JSON Schema não é específico de IA (spec de validação de dados já existente); 3 partes do tool spec (name, description, input_schema); boas práticas de descrição (3-4 frases, quando usar, o que retorna, descrições detalhadas por argumento); gerar o schema pedindo ao próprio Claude (com a documentação de tool use como contexto); padrão de nomenclatura `function_name_schema`; `ToolParam` da lib Anthropic para type safety
5. Handling Message Blocks — parâmetro `tools=[...]` na chamada da API; mensagens multi-bloco (Text Block + ToolUse Block) quando Claude decide usar uma tool; conteúdo do ToolUse block (id, name, input, type="tool_use"); preservar `response.content` inteiro ao salvar no histórico; fluxo completo de 5 passos (enviar → receber texto+tool_use → executar função → enviar resultado → resposta final); necessidade de atualizar helper functions para suportar conteúdo multi-bloco
6. Sending Tool Results — executar a função com `**response.content[1].input` (unpacking); tool_result block (`tool_use_id`, `content` serializado como string, `is_error`) dentro de uma mensagem `user`; múltiplas tool calls em uma resposta, cada uma com ID único que precisa ser casado no resultado; follow-up request precisa do histórico completo + o novo tool_result; a chamada final ainda precisa incluir `tools=[...]` mesmo sem esperar nova tool call

### Conteúdo da Seção 6 (concluída) — para referência

1. Introducing Retrieval Augmented Generation — problema com documentos grandes (ex: doc financeiro de 800 páginas) que não cabem no prompt; Opção 1 (colocar tudo no prompt) e suas limitações (limite de tamanho, Claude menos eficaz, custo e latência maiores); Opção 2/RAG (quebrar em chunks no preprocessing, buscar só os chunks relevantes na hora da pergunta); benefícios (foco, escala, eficiência) vs. desafios (preprocessing, mecanismo de busca, contexto faltante, estratégia de chunking); quando vale a pena usar RAG
2. Text Chunking Strategies — impacto direto da qualidade do chunking na qualidade do sistema RAG; exemplo do erro "bug" (medical research vs. software engineering); 3 abordagens principais (size-based, structure-based, semantic-based); size-based (`chunk_by_char`, downsides de cortar palavras/contexto, overlap como solução); structure-based (`chunk_by_section` via regex em headers Markdown); semantic-based (NLP, caro mas mais relevante); sentence-based como meio-termo prático (`chunk_by_sentence`); como escolher a estratégia por caso de uso
3. Text Embeddings — encontrar chunks relevantes é um problema de busca; semantic search usa embeddings (em vez de keyword matching); embedding = representação numérica do significado de um texto, cada número entre -1 e +1; não sabemos precisamente o que cada número representa (exemplos como "how happy" são apenas ilustrativos); VoyageAI como provedor recomendado (Anthropic não oferece embeddings); `generate_embedding()` com `voyageai.Client().embed(...)`; o desafio real é comparar embeddings, não gerá-los
4. The Full RAG Flow — exemplo numérico completo do pipeline (chunk → embed → normalizar → armazenar em vector database → embed da query → normalizar → buscar por similaridade → montar prompt final); modelo de embedding imaginário de 2 números (medical/software) para tornar o exemplo tangível; normalização escala o vetor para magnitude 1.0; vector database é otimizado para armazenar/comparar embeddings; cosine similarity (cosseno do ângulo entre vetores, -1 a 1) como métrica de busca, com cálculo completo (0.983 vs 0.398); cosine distance = 1 − cosine similarity; montagem do prompt final só com o chunk vencedor
5. Implementing the RAG Flow — implementação em código dos 5 passos (chunk → generate embeddings → create vector store → embed user query → search); `chunk_by_section` reaproveitado; `generate_embedding()` agora aceita lista de strings (batch); `VectorIndex()` + `store.add_vector(embedding, {"content": chunk})` guardando embedding E texto original (necessário porque a busca sozinha só retorna números); `store.search(user_embedding, 2)` retornando os 2 chunks mais próximos com distância; exemplo real com distância 0.71 (Software Engineering) vs 0.72 (Methodology) — menor distância = maior similaridade
6. BM25 Lexical Search — limitação do semantic search puro (pode perder termos exatos, ex: ID de incidente "INC-2023-Q4-011"); hybrid search = semantic search + lexical search em paralelo, depois merge; BM25 (Best Match 25) como algoritmo de lexical search: tokenizar query → contar frequência dos termos em todos os documentos → dar mais peso a termos raros → retornar chunks com mais instâncias dos termos mais pesados; `BM25Index()` + `store.add_document({"content": chunk})` + `store.search(query, n)`; BM25 funciona bem para termos técnicos/IDs/frases específicas, complementando o semantic search
7. A Multi-Index RAG Pipeline — VectorIndex e BM25Index compartilham a mesma API (`add_document`/`search`), o que permite uni-los numa classe `Retriever`; Reciprocal Rank Fusion (RRF) para combinar rankings de fontes diferentes de forma justa; fórmula `RRF_score(d) = Σ 1/(k + rank_i(d))`, k=1 no exemplo (60 é o padrão usual); exemplo completo com cálculo de scores e ranking final; implementação da classe `Retriever` (wraps múltiplos índices, mesma interface); teste do híbrido melhorando os resultados vs. busca vetorial pura; extensibilidade — qualquer novo índice que implemente `SearchIndex` (add_document/search) se encaixa automaticamente na fusão

### Conteúdo da Seção 7 (concluída) — para referência

1. Extended Thinking — "scratch paper" do Claude: bloco de raciocínio (`thinking`) separado do bloco de texto final, ativado com `thinking=True` e `thinking_budget` (mínimo 1024 tokens, `max_tokens` precisa ser maior que o budget); benefícios (melhor raciocínio, mais precisão, transparência) vs. trade-offs (custo maior, latência maior, tratamento de resposta mais complexo); quando usar — decisão guiada por avaliação de prompt (rodar sem thinking primeiro, só ativar se a precisão não bater depois do prompt já otimizado), não um padrão para toda chamada; `signature` — token criptográfico que garante que o texto do thinking não foi alterado antes de devolver à API; `redacted_thinking` — bloco criptografado quando o raciocínio interno é sinalizado pelos sistemas de segurança, mantém o contexto sem expor o conteúdo; string mágica de teste para forçar um redacted thinking block
2. Image Support — limites (até 100 imagens por request, máx 5MB, 8000px se for 1 imagem, 2000px se forem múltiplas, base64 ou URL, custo em tokens = (largura × altura)/750); image block + text block juntos na mesma mensagem `user`; mesmo fluxo de mensagens do texto puro (Claude responde com text block); as mesmas técnicas de prompt engineering do texto valem para imagens — pergunta simples ("quantas bolinhas?") pode dar resposta errada; melhora de precisão com (1) metodologia passo a passo (identificar e numerar, depois verificar contando de outro jeito) e (2) exemplos one-shot (imagem de referência com contagem conhecida antes da imagem alvo); exemplo real de fire risk assessment com imagem de satélite — prompt estruturado em etapas (localizar residência, analisar galhos sobre o telhado, avaliar vulnerabilidade a incêndio, avaliar espaço defensável, só então dar um rating de 1 a 4) produz resultado muito mais confiável que um prompt vago
3. PDF Support — código quase idêntico ao de imagens, só muda: extensão do arquivo (.pdf), nome da variável (`file_bytes` em vez de `image_bytes`, só por clareza), tipo do bloco (`"document"` em vez de `"image"`) e media_type (`"application/pdf"` em vez de `"image/png"`); Claude extrai de um PDF não só texto puro, mas também imagens/gráficos embutidos, tabelas com suas relações de dados, e a estrutura/formatação do documento — funciona como solução única para resumos, análise de dados ou extração de conteúdo específico
4. Citations — mostra exatamente de onde no documento Claude tirou cada informação, em vez de só confiar na resposta; ativado com dois campos extras no document block: `title` (nome legível do doc) e `citations: {"enabled": True}`; estrutura da citação tem 5 campos — `cited_text` (trecho exato citado), `document_index` (qual documento, se houver mais de um), `document_title`, `start_page_number`/`end_page_number` (onde o trecho começa/termina); com fonte em texto puro (`"type": "text"`) em vez de PDF, os campos de página viram posições de caractere; valor está na UI construída em cima disso (hover no marcador de citação mostra a fonte); quando usar — verificação de precisão, documentos autoritativos, transparência crítica, ou quando o usuário quer explorar o contexto ao redor de um fato
5. Prompt Caching — acelera respostas e reduz custo reaproveitando trabalho computacional de requests anteriores; sem cache, cada request faz preprocessing do zero (tokenizar prompt, criar embeddings de cada token, adicionar contexto) e joga tudo fora depois de gerar a resposta — desperdício em requests de follow-up que repetem o mesmo conteúdo (ex: refinar um resumo do mesmo texto longo); com cache, o request inicial grava o resultado do preprocessing num cache em vez de descartar — funciona como uma lookup table ("se eu ver essa mensagem de novo, reaproveito o trabalho já feito"); benefícios (respostas mais rápidas, custo menor no conteúdo cacheado, otimização automática — request inicial grava, follow-ups leem) vs. limitações (cache dura só 1 hora; só vale a pena quando o mesmo conteúdo se repete com alta frequência); melhores casos de uso — análise de documento (várias perguntas sobre o mesmo documento grande) e edição iterativa (conteúdo base constante, refinando aspectos específicos)
6. Rules of Prompt Caching — caching NÃO é automático, precisa adicionar manualmente um "cache breakpoint" (`"cache_control": {"type": "ephemeral"}`) num bloco; tudo antes e incluindo o breakpoint é cacheado; cache só é reaproveitado se o conteúdo até o breakpoint for idêntico (até adicionar "please" invalida e força reprocessar tudo); precisa da forma longhand do text block (com `"type": "text"` explícito) porque a forma shorthand (string simples) não tem onde colocar o `cache_control`; breakpoint pode atravessar várias mensagens (user/assistant) — colocar num later message cacheia tudo antes dele também, útil para cachear todo o contexto da conversa até um ponto; breakpoints também valem em system prompts, tool definitions, image blocks e tool use/result blocks — system prompt e tools são os melhores candidatos porque raramente mudam entre requests; ordem de processamento interna: tools → system prompt → messages; até 4 breakpoints por request; tamanho mínimo para caching: 1024 tokens somados (não por bloco individual)
7. Prompt Caching in Action — implementação em código: cache em tools vai no ÚLTIMO tool da lista (não na lista toda), copiando `tools` e o último tool antes de adicionar `cache_control` para não mutar o original (`tools_clone[-1].copy()`) e evitar problema se a ordem dos tools mudar depois; system prompt precisa virar uma lista com um text block (`[{"type": "text", "text": system, "cache_control": {...}}]`) em vez de string simples, mesma lógica shorthand/longhand; resposta da API reporta `cache_creation_input_tokens` (escreveu no cache) no primeiro request e `cache_read_input_tokens` (leu do cache) nos seguintes, com o mesmo valor quando o conteúdo é idêntico; cache é sensível a qualquer mudança de 1 caractere; caching é granular — se o system prompt muda mas os tools ficam iguais, a resposta mostra leitura parcial do cache (tools) + escrita nova (system prompt), só paga pelo que realmente mudou
8. Code Execution and Files API — Files API: upload do arquivo uma vez via chamada separada → recebe um `FileMetadata` com um `file_id` único → referencia esse ID nas mensagens seguintes em vez de mandar base64 de novo, útil pra arquivo grande ou usado várias vezes; Code Execution é um server-side tool (schema pronto, sem precisar implementar) — Claude roda Python isolado num container Docker, sem acesso a rede, pode executar código várias vezes numa mesma conversa, resultado é interpretado por Claude na resposta final; combinação dos dois: como o container não tem rede, o Files API é o jeito principal de entrada/saída de dados — fluxo típico é upload do CSV → bloco `{"type": "container_upload", "file_id": ...}` na mensagem → Claude escreve e roda código → pode gerar arquivos (ex: gráficos) pra download; resposta com code execution tem 3 tipos de bloco (text, server tool use = código rodado, code execution tool result = output); arquivos gerados por Claude aparecem em blocos `code_execution_output` com um file_id, baixados via Files API; útil além de análise de dados — processamento de imagem, parsing de documento, cálculos matemáticos, geração de relatórios

### Conteúdo da Seção 8 (concluída) — para referência

1. Introducing MCP — MCP (Model Context Protocol) = camada de comunicação que dá a Claude contexto e tools sem precisar escrever código de integração tedioso; desloca o trabalho de definir e executar tools do seu servidor pra servidores MCP especializados; arquitetura básica: MCP Client (seu servidor) conecta em um ou mais MCP Servers, cada um empacotando Tools, Prompts e Resources, servindo de interface pra um serviço externo; exemplo do GitHub — sem MCP seria preciso escrever schema + função pra cada funcionalidade (get_repos, list_repos, create_repos, search_issues, update_issue, create_issue, get_issue, create_file...), muito código pra escrever/testar/manter; com MCP, esse trabalho já vem pronto dentro do MCP Server, que funciona como wrapper do serviço externo; qualquer um pode criar um MCP server, geralmente o próprio provedor do serviço lança a implementação oficial (ex: AWS); MCP vs. chamar a API direto — MCP já vem com os schemas + funções prontos, chamando direto você que autora tudo; MCP não é a mesma coisa que tool use — MCP é sobre QUEM escreve e mantém as tools (alguém já escreveu, empacotado dentro do MCP server), tool use é o mecanismo que usa essas tools
2. MCP Clients — o MCP client é a ponte de comunicação entre seu servidor e os MCP servers, cuida de toda a troca de mensagens/protocolo; transport agnostic — client e server podem se comunicar por métodos diferentes (Standard IO é o mais comum quando rodam na mesma máquina, mas também HTTP, WebSockets etc.) sem mudar o que é trocado; tipos de mensagem principais da spec MCP: `ListToolsRequest`/`ListToolsResult` (cliente pergunta quais tools o server oferece) e `CallToolRequest`/`CallToolResult` (cliente pede pra rodar uma tool específica com argumentos e recebe o resultado); fluxo completo de exemplo (pergunta "What repositories do I have?"): user → server → MCP client pede lista de tools (ListToolsRequest/Result) → server manda pergunta + tools pro Claude → Claude decide usar uma tool → server pede pro MCP client executar (CallToolRequest ao MCP server, que chama o Github de verdade) → resultado volta como CallToolResult → server manda resultado pro Claude → resposta final formatada volta pro usuário; muitos passos, mas cada componente tem responsabilidade clara, o MCP client abstrai a complexidade da comunicação
3. Project Setup — início do projeto prático: chatbot CLI que interage com uma coleção de documentos, com dois componentes (MCP client cuidando da interação com o usuário + MCP server customizado gerenciando operações de documento — tool de ler e tool de atualizar), documentos guardados em memória (sem banco de dados); nota importante — em projetos reais normalmente se implementa OU um MCP client OU um MCP server, não os dois; este projeto implementa os dois só para fins didáticos, pra entender como se comunicam; setup — baixar `cli_project.zip`, extrair, abrir no editor; README com 3 passos (adicionar a Anthropic API key no `.env`, instalar dependências via UV ou pip, rodar a aplicação inicial pra verificar); arquivos principais `main.py`, `mcp_client.py`, `mcp_server.py`; rodar com `uv run main.py` ou `python main.py`; testar com uma pergunta simples ("what's 1+1?") pra confirmar que o setup básico funciona antes de implementar as features de MCP
4. Defining Tools with MCP — construir um MCP server fica muito mais simples com o SDK Python oficial: em vez de escrever schemas JSON manualmente, o SDK gera tudo a partir de decorators e type hints; `FastMCP("DocumentMCP", log_level="ERROR")` cria o server em uma linha; documentos guardados num dicionário Python simples (`docs = {...}`, ID → conteúdo); tool `read_doc_contents` (decorada com `@mcp.tool`, parâmetro `doc_id: str = Field(description=...)`) lê um documento pelo ID, levanta `ValueError` se o ID não existir; tool `edit_document` faz find-and-replace com `docs[doc_id].replace(old_str, new_str)`, parâmetros `doc_id`/`old_str`/`new_str` via `Field`; `Field` do Pydantic fornece as descrições de parâmetro que ajudam o Claude a entender cada argumento; benefícios do SDK — schema JSON automático a partir de type hints, código limpo, validação de parâmetro via Pydantic, menos boilerplate que escrever schema à mão, type safety/suporte de IDE
5. The Server Inspector — testar um MCP server sem precisar conectar numa aplicação completa; o SDK Python inclui um inspector embutido, baseado em browser, pra debugar/testar o server em tempo real; comando `mcp dev mcp_server.py` sobe um dev server na porta 6277 e dá uma URL local pra abrir no browser (interface do inspector pode mudar entre versões, mas a funcionalidade central de testar tools/resources/prompts se mantém); fluxo — clicar "Connect" pra iniciar o server, ir em Tools → "List Tools" → selecionar uma tool → preencher parâmetros → "Run Tool"; exemplo prático — testar leitura de documento com um ID (ex: "deposition.md"), depois encadear com edição + nova leitura pra confirmar que a mudança foi aplicada; workflow de desenvolvimento (loop: mudar código → testar tool isolada → verificar resultado sem precisar de app completo → debugar isolado) elimina a necessidade de plugar o server no Claude só pra testar funcionalidade básica
6. Implementing a Client — construir o lado client depois do server pronto; arquitetura em 2 componentes: MCP Client (classe custom que a gente escreve pra facilitar o uso da session) + Client Session (a conexão de verdade com o server, parte do SDK); a Client Session precisa de cleanup de recurso, por isso é embrulhada na classe MCP Client (cleanup automático); CLI precisa de 2 coisas do server — listar tools disponíveis pra mandar pro Claude, e executar tools quando o Claude pede; método `list_tools()` chama `self.session().list_tools()` e retorna `result.tools`; método `call_tool(tool_name, tool_input)` chama `self.session().call_tool(tool_name, tool_input)` passando nome + input (vindos do Claude); testagem via harness (`async with MCPClient(command="uv", args=["run", "mcp_server.py"]) as client:`) chamando `list_tools()` diretamente; fluxo completo (código pega tools → tools vão pro Claude junto com a pergunta → Claude decide usar `read_doc_contents` → código executa via client → resultado volta pro Claude → resposta final pro usuário); client é a ponte entre a lógica da aplicação e o MCP server, escondendo os detalhes de conexão
7. Defining Resources — resources deixam o MCP Server expor dados pro client, parecido com GET handlers de HTTP; servem pra buscar informação, não pra executar ação; exemplo motivador — feature de menção de documento (`@document_name`), precisa de 2 operações: listar todos os documentos disponíveis (autocomplete) e buscar o conteúdo de um documento específico quando mencionado; padrão request-response — client manda `ReadResourceRequest` com uma URI, server responde com o dado; 2 tipos — Direct Resources (URI estática, ex: `docs://documents`) e Templated Resources (URI com parâmetro, ex: `docs://documents/{doc_id}`, o SDK Python faz parse do parâmetro da URI e passa como argumento pra função); implementação com decorator `@mcp.resource(uri, mime_type=...)`: `list_docs()` (direct, retorna `list(docs.keys())`) e `fetch_doc(doc_id: str)` (templated, retorna `docs[doc_id]` ou levanta `ValueError`); `mime_type` dá uma dica ao client do tipo de dado retornado (`application/json`, `text/plain`, etc.), SDK serializa automaticamente sem precisar converter pra string JSON manualmente; testagem via MCP Inspector (`uv run mcp dev mcp_server.py`), aba Resources lista as diretas, aba Resource Templates mostra as com parâmetro; pontos-chave — resources expõem dados, tools executam ações; nome dos parâmetros na URI templated vira argumento da função
8. Accessing Resources — resources deixam o server expor dado incluído direto no prompt, sem precisar de tool call, mais eficiente pra dar contexto ao Claude; client precisa de uma função `read_resource(uri)` que chama `self.session().read_resource(AnyUrl(uri))` e pega `result.contents[0]` (primeiro elemento da lista `contents`, com o dado + metadado tipo MIME); parsing por tipo de conteúdo — checar `isinstance(resource, types.TextResourceContents)`, se `mimeType == "application/json"` usar `json.loads(resource.text)`, senão retornar `resource.text` puro; imports necessários — `import json` e `from pydantic import AnyUrl`; teste via CLI — digitar "@report.pdf" mostra autocomplete de resources, seleciona um, busca o conteúdo automaticamente e injeta no prompt pro Claude, sem tool call; `read_resource` vira um building block reutilizado por outras partes da aplicação (listar resources, buscar conteúdo, montar prompt) — separação de responsabilidades: MCP client cuida da comunicação com o server, lógica da aplicação cuida de como usar o dado
9. Defining Prompts — prompts do MCP server são templates pré-prontos, de alta qualidade, que o client usa em vez de escrever o próprio prompt do zero; exemplo motivador — reformatar documento pra markdown: usuário digitando "convert report.pdf to markdown" funciona, mas um prompt bem testado (com instruções específicas de formatação/estrutura/output) dá resultado bem melhor; prompts definem uma lista de mensagens user/assistant que o client usa direto — quando o client pede um prompt, o server devolve essa lista de mensagens prontas pra mandar pro Claude; estrutura básica — decorator `@mcp.prompt()`, com `name` e `description`, função retorna `list[base.Message]`; exemplo `format_document(doc_id)` — importa `from mcp.server.fastmcp import base`, monta uma f-string com instruções detalhadas de reformatação incluindo o `doc_id`, retorna `[base.UserMessage(prompt)]`; testagem via MCP Inspector, aba Prompts, selecionando o prompt e preenchendo parâmetros pra ver as mensagens geradas antes de usar em produção; boas práticas — focar em tarefas centrais ao propósito do server, instruções detalhadas e específicas (não vagas), testar com inputs variados, descrições claras, pensar em como o prompt interage com tools/resources do próprio server; prompts devem representar a expertise do autor do MCP server no domínio, dando valor que o usuário não conseguiria sozinho
10. Prompts in the Client — lado client pra listar e buscar os prompts definidos no server; método `list_prompts()` chama `self.session().list_prompts()` e retorna `result.prompts`; método `get_prompt(prompt_name, args)` chama `self.session().get_prompt(prompt_name, args)` e retorna `result.messages` (conversa pronta pra mandar direto pro Claude); como os argumentos funcionam — uma prompt function no server pode aceitar parâmetros (ex: `doc_id`), o dict `args` passado pelo client precisa ter as chaves esperadas, o MCP server passa como keyword arguments pra função; teste via CLI — digitar "/" mostra os prompts disponíveis como comandos, selecionar um (ex: "format") pode pedir opções (ex: qual documento), aí o prompt completo (já interpolado) é mandado pro Claude, que pode usar tools pra buscar dado extra e completar a tarefa; boas práticas — relevância ao propósito do server, testar bem, instruções claras/específicas, desenhar pra funcionar bem com as tools disponíveis, pensar nos argumentos que o usuário vai precisar fornecer; prompts fazem a ponte entre funcionalidade pré-definida e necessidade dinâmica do usuário, dando ponto de partida estruturado mas flexível via parametrização
11. MCP Review — aula de fechamento comparando os 3 primitives do MCP server lado a lado: **Tools** (model-controlled — Claude decide quando chamar, Claude usa o resultado; usado pra dar funcionalidade extra ao Claude), **Resources** (app-controlled — nosso app decide quando chamar, o resultado é usado principalmente pelo nosso app; usado pra trazer dado pro app e adicionar contexto às mensagens), **Prompts** (user-controlled — o usuário decide quando usar; usado pra workflows disparados por input do usuário, tipo slash command, clique de botão ou opção de menu); resumo do projeto da seção — server expondo `read_doc_contents`/`edit_document` como tools, `list_docs`/`fetch_doc` como resources direto/templated, e um prompt `format` via `base.UserMessage`; client embrulhando a Client Session pra listar/chamar tools, ler resources por URI, e listar/pegar prompts com argumentos interpolados — tudo testado no MCP Inspector antes de entrar na aplicação CLI

---

## 📊 Sistema de tracking (pontos fracos)

- Existe um arquivo **`weak_topics_tracking.xlsx`** que acumula: notas por aula, questões erradas, áreas fracas e status.
- Quando eu envio respostas de um quiz, **reanexo esse arquivo**; o assistente atualiza as 3 abas (Scores, Weak Topics, Summary by Area).
- Quando uma área fraca acumula erros, gerar uma **rodada de reforço** focada nela.

### Status do Curso 1 (Agent Skills) — CONCLUÍDO

- Lesson 1: 9/10 · Lesson 2: 10/10 · Lesson 3: 9/10 · Lesson 4: 10/10 · Lesson 5: 9/10 · Lesson 6: 10/10
- Reinforcement Round: 12/12
- **Áreas fracas (todas já reforçadas):** estrutura de arquivos/sintaxe; comportamento de loading (main vs subagent)

### Status do Curso 2 — Seção 2 (Accessing Claude with the API) — CONCLUÍDA

**Questões de treino (do meu material): 33/35 — 94%**

- Lesson 1: 4/5 · Lesson 2: 5/5 · Lesson 3: 5/5 · Lesson 4: 4/5 · Lesson 5: 5/5 · Lesson 6: 5/5 · Lesson 7: 5/5

**Quiz oficial do curso: 8/8 — 100%**

**Os 2 erros do treino:**

- Lesson 1, Q2 — campos do *request* vs. campos da *response* (Stop Reason é da response). Resolvido: o quiz oficial confirmou a mesma perspectiva.
- Lesson 4, Q3 — não li a palavra "PREVENT" no enunciado.

**⚠️ Área fraca em aberto — LEITURA DE ENUNCIADOS NEGATIVOS**
Meus dois únicos erros foram em questões com formulação negativa (**NOT**, **EXCEPT**, **PREVENT**, **LEAST**). Nos dois casos marquei uma alternativa *verdadeira sobre o assunto*, mas que não respondia ao que foi pedido. **Não é falta de conhecimento — é pressa na leitura.**

- Hábito a treinar: ao ver NOT/EXCEPT/PREVENT/LEAST, marcar a palavra e ler as alternativas perguntando "esta é a exceção?" em vez de "esta é verdadeira?".
- É um ponto **transversal**: afeta qualquer módulo, não um conteúdo específico.
- O quiz oficial da Seção 2 não tinha nenhuma questão negativa, então esse ponto **ainda não foi testado de verdade**.

**Pendência de tracking:** o `weak_topics_tracking.xlsx` **ainda não foi atualizado** com os resultados da Seção 2. Decidi juntar mais conteúdo antes de fazer a rodada de reforço. Nada de conteúdo a reforçar no Módulo 2 — só o item de leitura de enunciados.

### Status do Curso 2 — Seção 3 (Prompt Evaluation) — CONCLUÍDA (conteúdo); questões pendentes

- Documento fechado com 6 aulas (Lessons 1 a 6, incluindo Code Based Grading).
- As questões das Lessons 1 a 6 **ainda não foram respondidas**. Quando eu enviar as respostas, corrigir e registrar aqui.

### Status do Curso 2 — Seção 4 (Prompt Engineering Techniques) — CONCLUÍDA (conteúdo); questões pendentes

- Documento fechado com 5 aulas (Lessons 1 a 5). Resumos reescritos uma vez no meio do caminho para ficarem mais enxutos/dinâmicos (ver nota na seção de formato acima) — todo o documento já está no padrão final.
- As questões das Lessons 1 a 5 **ainda não foram respondidas**. Quando eu enviar as respostas, corrigir e registrar aqui.

### Status do Curso 2 — Seção 5 (Tool Use with Claude) — CONCLUÍDA (conteúdo); questões pendentes

- Documento fechado com 6 aulas (Introducing Tool Use; Project Overview: Reminder Tool; Tool Function; Tool Schemas; Handling Message Blocks; Sending Tool Results).
- As questões das Lessons 1-6 **ainda não foram respondidas**. Quando eu enviar as respostas, corrigir e registrar aqui.

### Status do Curso 2 — Seção 6 (RAG and Agentic Search) — CONCLUÍDA (conteúdo); questões pendentes

- Documento fechado com 7 aulas (Introducing Retrieval Augmented Generation; Text Chunking Strategies; Text Embeddings; The Full RAG Flow; Implementing the RAG Flow; BM25 Lexical Search; A Multi-Index RAG Pipeline).
- As questões das Lessons 1-7 **ainda não foram respondidas**. Quando eu enviar as respostas, corrigir e registrar aqui.

### Status do Curso 2 — Seção 7 (Features of Claude) — CONCLUÍDA (conteúdo); questões pendentes

- Documento fechado com 8 aulas (Extended Thinking; Image Support; PDF Support; Citations; Prompt Caching; Rules of Prompt Caching; Prompt Caching in Action; Code Execution and Files API).
- As questões das Lessons 1-8 **ainda não foram respondidas**. Quando eu enviar as respostas, corrigir e registrar aqui.

### Status do Curso 2 — Seção 8 (Model Context Protocol) — CONCLUÍDA (conteúdo); questões pendentes

- Documento fechado com 11 aulas (Introducing MCP; MCP Clients; Project Setup; Defining Tools with MCP; The Server Inspector; Implementing a Client; Defining Resources; Accessing Resources; Defining Prompts; Prompts in the Client; MCP Review) — 44 páginas.
- As questões das Lessons 1-11 **ainda não foram respondidas**. Quando eu enviar as respostas, corrigir e registrar aqui.

---

## 🐍 Dúvidas de Python já esclarecidas (não preciso de reexplicação)

Sou novo em algumas construções de Python. Já entendi, com explicação dada nesta preparação:

- **`with open(...) as f:`** — context manager; fecha o arquivo automaticamente ao fim do bloco, inclusive em caso de erro. Substitui o `f.close()` manual.
- **`json.dump` vs `json.dumps`** — `dump` escreve num arquivo, `dumps` (com s) retorna string. Mesma lógica para `json.load` (lê de arquivo) vs `json.loads` (lê de string).
- **Modos de arquivo** — `"r"` leitura, `"w"` escreve apagando tudo, `"a"` append, `"x"` cria se não existir, `"r+"` leitura e escrita. Para editar JSON o padrão é **ler com `"r"` → modificar o objeto Python → regravar tudo com `"w"`**; `"a"` quebra o JSON.
- **Docstring** (`"""..."""` abaixo do `def`) é documentação, não executa. **`pass`** é corpo vazio válido.
- **prompt / test case input / prompt completo** — o prompt é o template com o buraco (`{question}`, `{task}`); o test case input é o que preenche o buraco; os dois juntos formam o **prompt completo**, que viaja como `content` da user message. "Template" descreve a *forma* (molde reutilizável), o conteúdo dele por acaso é instrução.
- **O merge é vertical, não horizontal** — `run_prompt` recebe **um** test case e junta template + 1 pergunta. Nunca junta as perguntas entre si; se juntasse, haveria uma nota só e o diagnóstico por caso se perderia.

---

## 🛠️ Onde estou agora na prática (setup técnico)

Estou fazendo os exercícios práticos do curso em **VS Code + Jupyter Notebook** (arquivo `.ipynb`), no **Windows**.

- Extensões Python + Jupyter: instaladas ✅
- Rodei `%pip install anthropic python-dotenv`
- Uso arquivo `.env` com `ANTHROPIC_API_KEY` para a chave (nunca no código)

### Problema resolvido: `AuthenticationError: API key is invalid` (401)

- A chave estava correta (formato correto, carregando certo).
- **Causa real:** minha conta estava no plano **"Evaluation access"** SEM billing configurado. Sem billing/crédito, a API recusa a chave mesmo válida.
- **Solução:** configurar billing no console (console.anthropic.com), com crédito pré-pago pequeno (~US$ 5), auto-reload desligado.
- Custo de estudar é simbólico (centavos). Para o curso, usar **Haiku** (modelo mais barato).
- **Pendência:** trocar `claude-sonnet-4-0` (deprecated) por ID atual, ex: `claude-haiku-4-5-20251001`.

### Autocomplete do VS Code

Quero escrever o código sozinho, sem sugestão inline entregando a resposta. Desativar em `Ctrl+,` → `editor.inlineSuggest.enabled` = false (ou o comando "Toggle Inline Suggestion"). Se for Copilot/IntelliCode, desativar a extensão também.

### 🔄 Repositório GitHub (em andamento)

Criei um **repositório privado** no GitHub para centralizar a pasta do curso e acessar pelo Linux via VS Code.

- Raiz do repositório: **`C:\Users\Mateus-pc\OneDrive\Claude_Curso`** (a pasta do curso inteiro, não a de um módulo)
- Feito: `git config` de nome/email, `.gitignore` criado, `git init`, `git branch -M main`, `git add .`
- **Falta:** `git commit`, instalar o GitHub CLI (`winget install --id GitHub.cli -e`), `gh auth login`, `git remote add origin`, `git push -u origin main`
- Erro já resolvido: `Permission denied` ao dar `git add` — era o `.docx` aberto no Word. Fechar o Word resolve.
- Warnings de `LF will be replaced by CRLF`: normais no Windows, ignorar.
- **Atenção OneDrive:** a pasta está dentro do OneDrive, o que pode causar erros de `index.lock` / arquivo travado durante sincronização. Se acontecer, pausar a sincronização do OneDrive. Vale considerar mover para fora (ex: `C:\Dev\Claude_Curso`) já que o GitHub passa a ser o backup.
- **Uso no Linux depois do push:** `git clone` do repositório, e trabalhar com `git pull` antes de começar / `git push` ao terminar.

### ⚠️ Segurança

- **NUNCA colar a API key** (nem em prints, nem no chat). Já expus duas vezes sem querer — as duas foram revogadas e criei outra.
- **Existe um arquivo `Key_API_Anthropic_Mateus.md`** na pasta `2. Building with the Claude API/Jupyter_Notebook/` com chave dentro. Ele está no `.gitignore` (`Key_API_Anthropic_Mateus.md` e `*Key_API*`) e foi retirado do staging com `git rm --cached`. **Nunca deixar esse arquivo entrar em commit.** O ideal é migrar o conteúdo para `.env` e apagar o `.md`.
- Comando útil para auditar antes de commitar: `findstr /s /i /c:"sk-ant" *.ipynb *.md *.py`
- O `.gitignore` já cobre: `.env`, `.env.*`, `*.key`, `*Key_API*`, `__pycache__/`, `venv/`, `.ipynb_checkpoints/`, `~$*.docx`, `~$*.xlsx`, `desktop.ini`
- O assistente deve me alertar se eu expuser credenciais.

---

## 💡 Motivo de trocar de chat

Conversas longas consomem mais tokens (todo o histórico é reprocessado). Estou no plano **Pro**. Estratégia: **começar chat novo a cada seção**, levando este briefing + os arquivos-mãe + o tracking. O assistente pode gerar direto sem revisar cada página visualmente toda vez (o formato já está definido).

---

## ▶️ Próximo passo

**Seção 8 (Model Context Protocol) está concluída** (11 aulas, 44 páginas). Começar a **Seção 9 — Anthropic Apps: Claude Code and Computer Use** quando eu colar a primeira aula (texto + imagens); o assistente cria um documento-mãe novo `Modulo2_09_...docx` seguindo o mesmo padrão.

**Também em aberto:**

- Responder as questões das Lessons 1 a 6 da Seção 3, Lessons 1 a 5 da Seção 4, Lessons 1-6 da Seção 5, Lessons 1-7 da Seção 6, Lessons 1-8 da Seção 7 e Lessons 1-11 da Seção 8, e mandar para correção.
- Atualizar o `weak_topics_tracking.xlsx` (juntando Seção 2 + Seção 3 + Seção 4 + Seção 5 + Seção 6 + Seção 7 + Seção 8) e fazer a rodada de reforço — o único item de conteúdo em aberto é a leitura de enunciados negativos.
- Terminar o push do repositório GitHub (ver seção do repositório acima).
