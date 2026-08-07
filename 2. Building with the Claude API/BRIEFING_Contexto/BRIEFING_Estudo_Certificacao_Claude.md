# 📋 Briefing — Preparação Certificação Anthropic (Claude)

> **Como usar:** anexe este arquivo no início de um novo chat e diga "Leia o briefing, vamos continuar". Isso dá ao assistente todo o contexto do que estamos fazendo.
>
> *Última atualização: 06/08/2026 — ao concluir a Seção 2 e iniciar a Seção 3.*

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
- **Estrutura do resumo (enxuto, mas com profundidade onde importa):**
  - **Core idea** — 1-2 frases com a ideia central
  - **Key points** — bullets curtos com termos-chave em **destaque**
  - **Conceitos essenciais** — parágrafo desenvolvido para cada (NÃO enxugar os principais)
  - **Diagramas** — recriar os que eu enviar na conversa, no estilo visual da Anthropic, com legenda
  - **Tabelas** — para conteúdo comparativo/listável
- **Perguntas:** **5 questões** de múltipla escolha, alternativas **A a E**, SEM gabarito no documento
- **Gabarito:** só quando eu enviar minhas respostas → aí corrige, explica cada erro e registra no tracking

### Organização em documentos-mãe por SEÇÃO
- **1 documento por seção do curso** (não 1 por aula). Cada aula vira uma subseção dentro do documento-mãe, com índice (Contents) no topo.
- Quando eu adicionar uma aula a uma seção existente, **eu reanexo o .docx da seção** e o assistente adiciona a nova aula no fim + atualiza o índice.

### Seções do Curso 2 (Building with the Claude API) — 10 no total:
1. Anthropic Overview → `Modulo2_01_Anthropic_Overview.docx` ✅ **concluída**
2. Accessing Claude with the API → `Modulo2_02_Accessing_Claude_with_the_API.docx` ✅ **concluída (7 aulas, 39 páginas)**
3. **Prompt Evaluation** ⬅️ *seção atual — documento ainda não criado*
4. Prompt Engineering Techniques
5. Tool Use with Claude
6. RAG and Agentic Search
7. Features of Claude
8. Model Context Protocol
9. Anthropic Apps — Claude Code and Computer Use
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
Iniciar a **Seção 3 — Prompt Evaluation**. Vou colar o texto + imagens de cada aula; o assistente cria o `Modulo2_03_Prompt_Evaluation.docx` na primeira aula e vai acrescentando as demais + atualizando o índice.

**Também em aberto (fora do estudo):** terminar o push do repositório GitHub (ver seção do repositório acima).
