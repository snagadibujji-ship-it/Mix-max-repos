# Deduplication Report

Generated: 2026-06-05

## Functional Overlap Analysis

### Chat UI / LLM Frontend (routers/)

| Repo | Interface | Backend | Distinguishing Feature |
|------|-----------|---------|----------------------|
| LibreChat | Web (React) | Node.js | Most features, plugin marketplace, multi-user |
| chatbot-ui | Web (Next.js) | Minimal | Simplest, Vercel-deployable |
| lobe-chat | Web (Next.js) | Node.js | Plugin system, PWA, polished UI |
| open-webui | Web (Svelte) | Python | Ollama-first, RAG built-in |

**Decision: Keep all.** Different deployment targets; each has a distinct user base and integration model.

### Local Inference Servers (routers/)

| Repo | Language | Format Support | Distinguishing Feature |
|------|---------|---------------|----------------------|
| ollama | Go | GGUF | Simplest UX, Modelfile system, most popular |
| LocalAI | Go | GGUF, ONNX, GPTQ | OpenAI API drop-in, more backends |

**Decision: Keep both.** Different API compatibility and backend support profiles.

### Agent Frameworks with Overlap

| Pair | Overlap | Difference |
|------|---------|-----------|
| OpenDevin + OpenHands | Same codebase | OpenHands is renamed current; OpenDevin is historical |
| autogen + semantic-kernel | Both Microsoft | autogen = agent conversations; sk = plugin/function kernel |
| langchain + langgraph | Same ecosystem | langgraph extends langchain with graph-based state machines |
| rich + textual | Same ecosystem | textual is built on rich; different abstraction level |
| bubbletea + bubbles | Same ecosystem | bubbles provides UI components for bubbletea apps |

### Documentation Overlap

| Pair | Overlap | Notes |
|------|---------|-------|
| tldr-pages + project READMEs | CLI usage docs | Different depth; tldr = quick reference, READMEs = full docs |
| awesome-tuis + awesome-cli-coding-agents | Tool listings | Different focus areas; some agent tools appear in both |
| AGENT_ECOSYSTEM_MAP.md + REPOSITORY_INDEX.md | Repo descriptions | Complementary; index = table, map = relationships |

## Truly Unique Repositories (no functional duplicates)

`aider` · `SWE-agent` · `plandex` · `litellm` · `gateway` · `MCP/servers` · `ratatui` · `fzf` · `ripgrep` · `bat` · `eza` · `fd` · `k9s` · `yazi` · `fastfetch` · `glow` · `lazygit` · `lazydocker` · `markitdown` · `crewAI` · `MetaGPT` · `mastra` · `haystack` · `dify` · `opentui`

## Duplicate Documentation / Prompts / Assets

No duplicate standalone prompts, assets, or template files detected. Each repository's internal assets are unique to that project.

## Decision Summary

**All 51 cloned repositories retained.** Even where functional overlap exists, each repo serves as a reference implementation with:
- Distinct APIs/interfaces worth studying independently
- Different deployment environments and constraints
- Unique architectural decisions and code patterns
- Independent community ecosystems and documentation
