# Dependency Summary

Generated: 2026-06-05T19:48:16.475Z

## Python Ecosystem (pip)

| Package | Used By | Purpose |
|---------|---------|---------|
| `openai` | aider, crewAI, autogen, MetaGPT, langchain, SWE-agent, haystack, dify, litellm | OpenAI API client |
| `anthropic` | aider, crewAI, langchain, haystack, litellm | Anthropic API client |
| `langchain-core` | langchain, langgraph, crewAI, haystack, dify | LLM abstraction layer |
| `pydantic` | crewAI, MetaGPT, langchain, haystack, dify, litellm, autogen | Data validation |
| `fastapi` | haystack, dify, litellm | API server |
| `tiktoken` | aider, langchain, autogen, MetaGPT | Token counting |
| `tenacity` | langchain, crewAI, autogen | Retry logic |
| `httpx` | litellm, dify, haystack | Async HTTP |
| `rich` | aider, crewAI, SWE-agent, plandex | Terminal formatting |
| `docker` | SWE-agent, OpenHands, MetaGPT | Container management |
| `faiss-cpu` | langchain, haystack, autogen | Vector similarity |
| `chromadb` | langchain, haystack, crewAI | Vector store |

## Go Ecosystem (go mod)

| Package | Used By | Purpose |
|---------|---------|---------|
| `charmbracelet/bubbletea` | glow, crush, lazygit | TUI framework |
| `charmbracelet/lipgloss` | glow, k9s, crush, lazygit, lazydocker | TUI styling |
| `charmbracelet/bubbles` | glow, crush | TUI components |
| `spf13/cobra` | k9s, lazygit, cli/cli | CLI framework |
| `spf13/viper` | k9s, lazygit, cli/cli | Config management |
| `ollama/ollama` (internal) | LocalAI-compatible | Local inference |

## TypeScript/Node.js Ecosystem (npm)

| Package | Used By | Purpose |
|---------|---------|---------|
| `@anthropic-ai/sdk` | cline, mastra, LibreChat | Anthropic client |
| `openai` | cline, mastra, LibreChat, chatbot-ui, lobe-chat | OpenAI client |
| `@modelcontextprotocol/sdk` | servers, cline, mastra | MCP integration |
| `langchain` (npm) | mastra | LangChain TypeScript |
| `ai` (Vercel AI SDK) | chatbot-ui, mastra | Streaming AI responses |
| `next` | chatbot-ui, lobe-chat, LibreChat (partially) | React framework |
| `zod` | cline, mastra, LibreChat | Schema validation |

## Rust Ecosystem (cargo)

| Crate | Used By | Purpose |
|-------|---------|---------|
| `clap` | ripgrep, bat, fd, eza, yazi | CLI argument parsing |
| `tokio` | yazi, bat | Async runtime |
| `ratatui` | yazi | TUI rendering |
| `syntect` | bat | Syntax highlighting |
| `ignore` | ripgrep, fd | .gitignore handling |

## Common DevOps / Infrastructure

| Tool | Repos Using It |
|------|---------------|
| Docker | OpenHands, SWE-agent, dify, LocalAI, open-webui, LibreChat |
| Docker Compose | dify, LibreChat, open-webui |
| Kubernetes/Helm | semantic-kernel (docs), k9s (monitors), dify |
| GitHub Actions | All (CI/CD) |
| PostgreSQL | dify, LibreChat, open-webui |
| Redis | dify, LibreChat, open-webui |
| Nginx | dify, LibreChat, open-webui |
