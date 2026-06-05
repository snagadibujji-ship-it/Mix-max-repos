# Agent Ecosystem Map

Generated: 2026-06-05T19:48:16.475Z

## Ecosystem Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                    LLM PROVIDERS                                 │
│  OpenAI · Anthropic · Google · Mistral · Local (Ollama)         │
└────────────────────┬────────────────────────────────────────────┘
                     │
        ┌────────────┼────────────────┐
        ▼            ▼                ▼
┌──────────────┐ ┌──────────┐ ┌──────────────────┐
│   ROUTERS    │ │   MCP    │ │    FRAMEWORKS     │
│  litellm     │ │ servers  │ │ langchain/graph   │
│  gateway     │ │          │ │ crewAI · autogen  │
│  ollama      │ └──────────┘ │ MetaGPT · mastra  │
│  open-webui  │              │ semantic-kernel   │
└──────────────┘              │ OpenHands · dify  │
                              └──────────────────┘
                                       │
                     ┌─────────────────┼──────────────────┐
                     ▼                 ▼                   ▼
              ┌────────────┐  ┌──────────────┐   ┌─────────────┐
              │  AGENTS    │  │  TUI APPS    │   │ AWESOME     │
              │ aider      │  │ lazygit      │   │ LISTS       │
              │ cline      │  │ fzf · bat    │   │ awesome-tuis│
              │ opencode   │  │ ripgrep      │   │ tldr-pages  │
              │ SWE-agent  │  │ k9s · yazi   │   │             │
              └────────────┘  └──────────────┘   └─────────────┘
```

## Coding Agent Comparison

| Agent | Interface | Language | Autonomous | Git-aware | Multi-file | Strengths |
|-------|-----------|----------|-----------|-----------|-----------|-----------|
| aider | TUI/CLI | Python | ✓ | ✓ (native) | ✓ | Best git integration, many models |
| opencode | TUI | Go/TS | ✓ | ✓ | ✓ | Fast, clean TUI |
| cline | VSCode ext | TypeScript | ✓ | ✓ | ✓ | IDE integration, tool-use loop |
| continue | VSCode/JB | TypeScript | ✗ | ✓ | ✓ | Autocomplete + chat |
| SWE-agent | CLI | Python | ✓ | ✓ (GitHub) | ✓ | Issue resolution from GitHub |
| claude-code | CLI | ? | ✓ | ✓ | ✓ | Anthropic native |
| codex | CLI | Rust | ✓ | ✓ | ✓ | OpenAI native |
| plandex | CLI | Go | ✓ | ✓ | ✓ | Long-horizon planning |
| crush | TUI | Go | ✓ | ✓ | ✓ | Charm-native TUI |

## Framework Architecture Patterns

| Framework | Pattern | State | Parallelism | Best For |
|-----------|---------|-------|------------|---------|
| langgraph | DAG/State machine | Persistent | Branching | Complex workflows |
| crewAI | Role-based crews | Shared memory | Sequential/Parallel | Collaborative tasks |
| autogen | Conversation | Message history | Multi-turn | Dialogue-driven agents |
| MetaGPT | Software company | Role assignments | Pipelined | Software dev simulation |
| mastra | Typed workflows | Durable | Steps | TypeScript-native pipelines |
| OpenHands | Sandboxed exec | Docker | Task-based | Safe code execution |
| semantic-kernel | Plugin/Skill | Memory stores | Function calling | Enterprise .NET/Python |
| haystack | NLP Pipeline | Component state | Parallel nodes | RAG/search |
| dify | Visual builder | DB-backed | Parallel | No-code LLM apps |
| AutoGPT | Goal-driven loop | Task queue | Sequential | Autonomous goals |

## Integration Opportunities

| Combination | Integration Value |
|-------------|-----------------|
| aider + litellm | Route aider through litellm for cost tracking and model fallbacks |
| crewAI + langgraph | Use langgraph as the state machine backing crewAI crews |
| SWE-agent + OpenHands | OpenHands provides safer Docker sandboxing for SWE-agent |
| continue + ollama | Fully local IDE autocomplete and chat |
| MCP servers + claude-code/cline | Standardized tool protocol for any agent |
| dify + litellm | Enterprise LLM routing under a no-code UI |
| aichat + ratatui | Rust-native TUI frontend for LLM CLI access |
| bubbletea + litellm | Custom Go TUI for model routing |
| k9s pattern + autogen | Terminal-native UI pattern for agent monitoring |
