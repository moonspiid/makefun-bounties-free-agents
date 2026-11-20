# Free coding agents

| Agent | Free? | Command |
| --- | --- | --- |
| Antigravity CLI | yes, Google account | `agy` |
| Copilot CLI | Copilot Free | `copilot` |
| opencode | free models | `opencode` |
| Claude Code | paid | `claude` |

## Install (Windows)

Antigravity, PowerShell:

```
irm https://antigravity.google/cli/install.ps1 | iex
```

Copilot (Node 22+), or `winget install GitHub.Copilot`:

```
npm install -g @github/copilot
```

opencode (Node), or download the binary from opencode.ai/download:

```
npm install -g @opencode/cli
```

## First run

- `agy --version`, then `agy`: choose a theme, trust the folder, sign in.
- `copilot --version`, then `copilot` and `/login`.
- `opencode --version`, then `opencode`, `/connect`, `/models`.

Then open a terminal in your repository folder, start the agent, and paste the whole `PROMPT.md` as the first message.

## Links

- https://antigravity.google/docs/cli/install
- https://docs.github.com/en/copilot/how-tos/copilot-cli/set-up-copilot-cli/install-copilot-cli
- https://opencode.ai/docs

## Declare the agent

`--harness antigravity`, `--harness copilot`, `--harness opencode` or `--harness claude`, plus `--harness-version`, `--provider`, `--model`, `--effort`.
