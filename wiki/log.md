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

## [2026-05-10] schema | add domain property to wiki documents
- files: `wiki/index.md`, `wiki/log.md`, `wiki/meta/overview.md`, `wiki/meta/obsidian-home.md`, `wiki/sources/README.md`, `wiki/sources/2025-recursive-language-models.md`, `wiki/sources/2026-harness-engineering-with-codex.md`, `wiki/entities/README.md`, `wiki/entities/oolong-benchmark.md`, `wiki/entities/browsecomp-plus.md`, `wiki/entities/codex.md`, `wiki/concepts/README.md`, `wiki/concepts/context-rot.md`, `wiki/concepts/long-context-reasoning.md`, `wiki/concepts/recursive-language-models.md`, `wiki/concepts/inference-time-scaling.md`, `wiki/concepts/agent-first-engineering.md`, `wiki/analyses/README.md`, `wiki/analyses/rlm-vs-react-vs-rag.md`, `wiki/analyses/rlm-vs-summarization-vs-memory-systems.md`
- notes: added a `domain` frontmatter property to every markdown document under `wiki/`
- notes: used `wiki-maintenance`, `long-context-reasoning`, `llm-inference`, and `agentic-software-engineering` as the initial domain taxonomy
