# Security Notes

Generated: 2026-06-05

## Applied Hardening Measures

| Measure | Applied | Description |
|---------|---------|-------------|
| Shallow clone | ✓ | `--depth=1 --single-branch --no-tags` — no full history |
| Git metadata removed | ✓ | All inner `.git/` dirs recursively deleted |
| Submodule refs removed | ✓ | `.gitmodules` deleted from all repos |
| Git attributes removed | ✓ | `.gitattributes` deleted |
| Token never stored | ✓ | GITHUB_TOKEN used only via env var, never committed |
| Single git root | ✓ | Only `Mix-max-repos/.git` remains |

## High-Attention Repositories

| Repository | Risk Level | Concern | Recommendation |
|------------|-----------|---------|----------------|
| OpenHands | 🔴 High | Executes agent-generated code in Docker sandboxes | Use only in isolated Docker; never run as root |
| SWE-agent | 🔴 High | LLM writes & runs arbitrary code via Docker API | Require Docker socket access controls |
| AutoGPT | 🟠 Medium | Goal-driven autonomous agent with tool execution | Sandbox all tool calls; restrict file system access |
| dify | 🟠 Medium | Multi-user platform with DB credentials in configs | Review `.env`, never expose admin API publicly |
| LibreChat | 🟠 Medium | Multi-user chat storing API keys per user | Configure proper auth; use secrets manager |
| open-webui | 🟠 Medium | Web UI with user auth and model access | Bind to localhost or configure proper TLS |
| LocalAI | 🟡 Low | Local ML inference server | Bind to 127.0.0.1 by default; large GPU footprint |
| ollama | 🟡 Low | Local model server | Never expose port 11434 to internet |

## Archived Repositories
None detected — all acquired repositories are actively maintained.

## Supply Chain Notes
- All repos cloned from verified GitHub URLs — no third-party mirrors
- Shallow clones reduce exposure to historical credential leaks in git history
- Review `requirements.txt`, `package.json`, `go.mod`, `Cargo.toml` before running any repo
