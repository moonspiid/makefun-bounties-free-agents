# How to enter make.fun bounties with free coding agents

A plain-language guide to taking part in [make.fun](https://make.fun) bounties ("quests") using **free** coding agents. You build with an agent, you keep control of every submission.

Not affiliated with make.fun. Nothing here submits anything without you saying yes.

## Documents

| File | What it covers |
| --- | --- |
| [docs/AGENTS.md](docs/AGENTS.md) | The free agents: install, sign-in, links, cost |
| [docs/WORKFLOW.md](docs/WORKFLOW.md) | Every command, in order |
| [docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) | Each error we hit and its fix |
| [docs/SECURITY.md](docs/SECURITY.md) | Keys, secrets, what never to paste |

Companion repo **makefun-lanceur** holds `makefun.zip`: a Windows launcher that automates the steps below.

## What you need

- A [make.fun](https://make.fun) account, linked to a GitHub account.
- GitHub: a **public** repository for the entry.
- Node.js 18+ (LTS): https://nodejs.org
- git: https://git-scm.com
- One free coding agent (see docs/AGENTS.md).

## The six steps

1. **Pick the quest.** The slug is the last part of its URL: `https://make.fun/bounty/tiny-chess-01` -> `tiny-chess-01`.
2. **Download the official kit** for that quest: `https://make.fun/c/<slug>/kit`. Extract it. Its `RULES.txt` is the authority.
3. **Sign in** to make.fun from the kit: `node cli/makefun.mjs login --origin https://make.fun`
4. **Start the recording BEFORE the agent**: `node cli/makefun.mjs record --competition <slug> --source <repo-path>`
5. **Build with the agent** in your repo folder, then push to a public GitHub repo.
6. **Seal, check, submit**: finish the recording, run `check`, then `submit`.

## Rules that get entries rejected

- The repository must be **public**, with an **OSI license** (`LICENSE` at the root, MIT is fine).
- `README.md` at the root with the **three make.fun badges** for that repo.
- Repository **About** filled in, with the topic `makefun`.
- Commits under **your own** git identity, not the agent's.
- The recording must start **before** the agent's first message. A session started earlier does not count.
- Five declarations are required, real values only: `--harness`, `--harness-version`, `--provider`, `--model`, `--effort`.
- Some quests require `STRATEGY.md`; some require the recorded session instead of a transcript bundle. Check `RULES.txt` and the quest page.

## Free agents at a glance

| Agent | Command | Cost |
| --- | --- | --- |
| Google Antigravity CLI | `agy` | Free with a Google account |
| GitHub Copilot CLI | `copilot` | Copilot Free plan |
| opencode | `opencode` | Free models included |
| Claude Code | `claude` | Paid |

Install commands, sign-in and what to declare: [docs/AGENTS.md](docs/AGENTS.md).

## Cost

Every tool listed as free is free at the account level. The only thing you spend is time, plus electricity.
