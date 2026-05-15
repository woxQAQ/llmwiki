---
domain: wiki-maintenance
---

# Wiki Log

Append-only operational history for the wiki.

## [2026-05-10] bootstrap | initialize llm-wiki scaffold
- files: `README.md`, `AGENTS.md`, `wiki/index.md`, `wiki/log.md`, `wiki/meta/overview.md`
- notes: created the base directory structure and agent schema
- notes: added starter templates and placeholder category docs

## [2026-05-10] schema | localize readmes and add obsidian defaults
- files: `README.md`, `raw/README.md`, `wiki/sources/README.md`, `wiki/entities/README.md`, `wiki/concepts/README.md`, `wiki/analyses/README.md`, `wiki/meta/obsidian-home.md`, `.obsidian/app.json`, `.obsidian/core-plugins.json`, `.obsidian/templates.json`, `AGENTS.md`
- notes: translated all README-style guidance files into Chinese
- notes: added Obsidian-friendly defaults for attachments, templates, links, and navigation

## [2026-05-10] schema | localize templates and add frontmatter
- files: `templates/source-page-template.md`, `templates/entity-page-template.md`, `templates/concept-page-template.md`, `templates/analysis-page-template.md`
- notes: translated all templates into Chinese
- notes: added unified YAML frontmatter fields for Obsidian and Dataview compatibility

## [2026-05-10] ingest | Recursive Language Models
- files: `wiki/sources/2025-recursive-language-models.md`, `wiki/concepts/recursive-language-models.md`, `wiki/concepts/context-rot.md`, `wiki/concepts/inference-time-scaling.md`, `wiki/concepts/long-context-reasoning.md`, `wiki/entities/oolong-benchmark.md`, `wiki/entities/browsecomp-plus.md`, `wiki/index.md`, `wiki/meta/overview.md`, `wiki/meta/obsidian-home.md`
- notes: ingested `raw/assets/rlm.md` into one source page and six durable concept or entity pages
- notes: established the wiki's first content cluster around long-context reasoning and recursive inference

## [2026-05-10] query | RLM、ReAct 与 RAG 的对比
- files: `wiki/analyses/rlm-vs-react-vs-rag.md`, `wiki/index.md`, `wiki/meta/overview.md`, `wiki/meta/obsidian-home.md`
- notes: saved a durable comparison analysis contrasting RLM, ReAct, and RAG
- notes: updated navigation so the new analysis is visible from the index and Obsidian home

## [2026-05-10] query | RLM、总结式上下文管理与记忆系统的对比
- files: `wiki/analyses/rlm-vs-summarization-vs-memory-systems.md`, `wiki/index.md`, `wiki/meta/obsidian-home.md`
- notes: saved a durable comparison analysis contrasting RLM, summarization-based context management, and memory systems
- notes: positioned the three approaches by time scale, compression strategy, and fit for long-context tasks

## [2026-05-10] ingest | 工程技术：在智能体优先的世界中利用 Codex
- files: `wiki/sources/2026-harness-engineering-with-codex.md`, `wiki/entities/codex.md`, `wiki/concepts/agent-first-engineering.md`, `wiki/concepts/inference-time-scaling.md`, `wiki/index.md`, `wiki/meta/overview.md`, `wiki/meta/obsidian-home.md`
- notes: ingested `raw/assets/工程技术：在智能体优先的世界中利用 Codex.md` into one source page plus Codex and agent-first engineering pages
- notes: expanded the wiki from long-context reasoning into coding agents, repository-as-record-system, and harness design themes

## [2026-05-10] ingest | EWD 667: On the foolishness of "natural language programming"
- files: `wiki/sources/dijkstra-natural-language-programming.md`, `wiki/entities/edsger-dijkstra.md`, `wiki/concepts/natural-language-programming.md`, `wiki/concepts/agent-first-engineering.md`, `wiki/index.md`
- notes: ingested Dijkstra's EWD 667 into a source page, entity page for Dijkstra, and concept page for natural language programming
- notes: linked Dijkstra's narrow-interface argument to agent-first engineering's emphasis on structured constraints and mechanical verification
- notes: framed the LLM-era tension around prompt programming, precision vs. accessibility, and whether Dijkstra's critique is obsolete or more relevant than ever

## [2026-05-10] ingest | Evolution of HTTP
- files: `wiki/sources/evolution-of-http.md`, `wiki/concepts/http.md`, `wiki/entities/tim-berners-lee.md`, `wiki/index.md`
- notes: ingested `raw/assets/Evolution of HTTP.md` (MDN) into a source page, an HTTP evolution concept page, and a Tim Berners-Lee entity page
- notes: introduced the `web-fundamentals` domain to the wiki taxonomy
- notes: covered HTTP versions 0.9 through 3, TLS/SSL, REST, WebDAV, CORS/CSP, and the evolving solutions to head-of-line blocking

## [2026-05-10] schema | add domain property to wiki documents
- files: `wiki/index.md`, `wiki/log.md`, `wiki/meta/overview.md`, `wiki/meta/obsidian-home.md`, `wiki/sources/README.md`, `wiki/sources/2025-recursive-language-models.md`, `wiki/sources/2026-harness-engineering-with-codex.md`, `wiki/entities/README.md`, `wiki/entities/oolong-benchmark.md`, `wiki/entities/browsecomp-plus.md`, `wiki/entities/codex.md`, `wiki/concepts/README.md`, `wiki/concepts/context-rot.md`, `wiki/concepts/long-context-reasoning.md`, `wiki/concepts/recursive-language-models.md`, `wiki/concepts/inference-time-scaling.md`, `wiki/concepts/agent-first-engineering.md`, `wiki/analyses/README.md`, `wiki/analyses/rlm-vs-react-vs-rag.md`, `wiki/analyses/rlm-vs-summarization-vs-memory-systems.md`
- notes: added a `domain` frontmatter property to every markdown document under `wiki/`
- notes: used `wiki-maintenance`, `long-context-reasoning`, `llm-inference`, and `agentic-software-engineering` as the initial domain taxonomy

## [2026-05-12] ingest | 使用 Claude Code：HTML 的不可思议的有效性
- files: `wiki/sources/using-claude-code-html-effectiveness.md`, `wiki/concepts/html-artifacts.md`, `wiki/entities/claude-code.md`, `wiki/concepts/agent-first-engineering.md`, `wiki/index.md`, `wiki/meta/overview.md`, `wiki/meta/obsidian-home.md`, `wiki/log.md`
- notes: ingested the Claude Code HTML-artifacts post into one source page plus durable concept and entity pages
- notes: expanded the agentic engineering cluster toward human-readable review surfaces, interactive artifacts, and HTML-based output workflows

## [2026-05-15] schema | rename invalid raw asset path for portability
- files: `raw/assets/e-w-dijkstra-on-the-foolishness-of-natural-language-programming-ewd-667.md`, `wiki/sources/dijkstra-natural-language-programming.md`, `wiki/entities/edsger-dijkstra.md`, `wiki/concepts/natural-language-programming.md`, `wiki/log.md`
- notes: renamed the EWD 667 raw asset to a filesystem-safe kebab-case path without double quotes
- notes: updated all wiki `source_files` references so Git checkouts on Windows-compatible filesystems no longer fail
