# Technology Stack Map

Generated: 2026-06-05T19:48:16.474Z

## Language Distribution

| Language | Repos | % | Key Repositories |
|----------|-------|---|-----------------|
| Go | 15 | 30.6% | ollama, fzf, lazygit |
| Python | 13 | 26.5% | AutoGPT, markitdown, open-webui |
| TypeScript | 9 | 18.4% | dify, servers, cline |
| Rust | 7 | 14.3% | codex, ripgrep, bat |
| Markdown | 1 | 2.0% | tldr |
| C# | 1 | 2.0% | semantic-kernel |
| MDX | 1 | 2.0% | haystack |
| C | 1 | 2.0% | fastfetch |
| Unknown | 1 | 2.0% | awesome-tuis |

## AI Provider Coverage

| Provider | Coding Agents | Frameworks | Routers/UIs |
|----------|--------------|------------|-------------|
| **OpenAI** | aider, opencode, codex, SWE-agent | langchain, autogen, crewAI, MetaGPT, mastra | litellm, LibreChat, lobe-chat, open-webui |
| **Anthropic Claude** | aider, opencode, claude-code, cline | langchain, autogen, semantic-kernel | litellm, LibreChat, lobe-chat |
| **Google Gemini** | aider | langchain, autogen | litellm, LibreChat |
| **Local / Ollama** | aider, continue | langchain, haystack, dify | ollama, LocalAI, open-webui |
| **Mistral** | aider, continue | langchain, haystack | litellm, aichat |
| **Groq** | aider | langchain | litellm, aichat |
| **Azure OpenAI** | aider, cline | autogen, semantic-kernel | litellm, LibreChat |

## Architecture Patterns by Category

### agents/ — Single-Agent Coding
- Runtime: Python (aider, SWE-agent, plandex) · TypeScript/Node (cline, continue, opencode) · Go (crush) · Rust (codex)
- LLM I/O: Direct API calls (openai/anthropic SDK) · litellm for multi-provider
- Tool use: File I/O, shell, git, code execution
- Distribution: pip, npm, cargo, brew

### frameworks/ — Multi-Agent Orchestration
- Python dominant: langchain, langgraph, crewAI, autogen, MetaGPT, haystack, OpenHands
- TypeScript: mastra, dify (frontend)
- C#/Java/Python: semantic-kernel
- Patterns: DAG (langgraph), roles/crews (crewAI), conversation (autogen), NLP pipeline (haystack)

### routers/ — LLM Gateways & Chat UIs  
- Gateway/proxy: litellm (Python/FastAPI), gateway (Portkey, TypeScript)
- Chat UIs: LibreChat (Node.js), chatbot-ui (Next.js), lobe-chat (Next.js), open-webui (SvelteKit)
- Local inference: ollama (Go), LocalAI (Go), aichat (Rust)

### tui-frameworks/ — Terminal UI Libraries
- Go: bubbletea (Elm architecture), lipgloss (styling), bubbles (components), glamour (markdown)
- Python: rich (formatting), textual (reactive TUI)
- Rust: ratatui (immediate-mode TUI)
- TypeScript: opentui

### tui-apps/ — Terminal Applications
- Go: lazygit, lazydocker, k9s, glow, cli/cli
- Rust: yazi, ripgrep, bat, eza, fd
- C: fzf, fastfetch
