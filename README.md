# How to enter make.fun bounties with free coding agents

![makefun](https://img.shields.io/badge/makefun-bounties-orange?style=flat-square)
![agents](https://img.shields.io/badge/agents-free-brightgreen?style=flat-square)
![price](https://img.shields.io/badge/price-free-brightgreen?style=flat-square)
![license](https://img.shields.io/badge/license-MIT-blue?style=flat-square)
![language](https://img.shields.io/badge/guide-English-informational?style=flat-square)

A plain-language guide to taking part in [make.fun](https://make.fun) bounties ("quests") using **free** coding agents. You build with an agent, and you decide when an entry is submitted.

Not affiliated with make.fun. Nothing here submits anything without your say-so.

## Where to start

Create your make.fun account with my invite link: **https://make.fun/r/ew2tc6sm**

Then come back here and follow the six steps below.

## Read in this order

| File | What it covers |
| --- | --- |
| [docs/AGENTS.md](docs/AGENTS.md) | The free agents: install, sign-in, links, cost |
| [docs/WORKFLOW.md](docs/WORKFLOW.md) | Kit and sign-in |
| [docs/BUILD.md](docs/BUILD.md) | Recording, building, sealing |
| [docs/SUBMIT.md](docs/SUBMIT.md) | Bundle, check, submit, badges |
| [docs/TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) | Every error we hit, and the fix |
| [docs/SECURITY.md](docs/SECURITY.md) | Keys, secrets, what never to paste |

The companion repository **makefun-lanceur** holds `makefun.zip`, a Windows launcher that does the steps below for you. You only type the quest name.

## What you need

- A [make.fun](https://make.fun/r/ew2tc6sm) account linked to GitHub.
- GitHub: a **public** repository for the entry.
- Node.js 18+ (LTS): https://nodejs.org
- git: https://git-scm.com
- One free coding agent.

## The six steps

1. **Pick the quest.** The slug is the end of its address: `https://make.fun/bounty/tiny-chess-01` gives `tiny-chess-01`.
2. **Get the kit** for that quest and read its `RULES.txt`. That file wins over everything written here.
3. **Sign in** to make.fun from the kit.
4. **Start the recording before the agent.** A session started earlier does not count.
5. **Build with the agent** inside your repository folder, then push it to a public GitHub repo.
6. **Seal the recording, run `check`, then `submit`.**

## Rules that get entries rejected

- Repository **public**, with an **OSI license** (`LICENSE` at the root, MIT is fine).
- `README.md` at the root carrying the **three badges** for that repo.
- Repository **About** filled in, with the topic `makefun`.
- Commits under **your** git identity, not the agent's.
- **Five declarations**, real values only: `--harness`, `--harness-version`, `--provider`, `--model`, `--effort`.
- Some quests want a `STRATEGY.md`; some accept only the recorded session instead of a transcript bundle.

## Free agents at a glance

| Agent | Command | Cost |
| --- | --- | --- |
| Google Antigravity CLI | `agy` | Free with a Google account |
| GitHub Copilot CLI | `copilot` | Copilot Free plan |
| opencode | `opencode` | Free models included |
| Claude Code | `claude` | Paid |

## Cost

Everything listed as free is free at the account level. What you spend is time.
