# Troubleshooting

| Message | What to do |
| --- | --- |
| `node` is not recognized | Install Node.js LTS from https://nodejs.org, then reopen the terminal |
| The window closes instantly | Run `Lancer-Makefun.bat` from a terminal, or keep the `pause` line |
| `tar` is not recognized | Windows 10+ has it; otherwise extract with 7-Zip |
| `~/.makefun/credentials is not a makefun credentials file` | Move that file away, then sign in again |
| `makefun bundle: no session of <repo> was found` | The agent never worked inside that folder. Start it there, or submit with `--recording` |
| `check` fails on `license_osi` | Add a `LICENSE` file at the root (MIT is fine) |
| `check` fails on `entrypoint` | Read `RULES.txt`: the expected entry file is named there |
| `check` fails on `transcripts_present` | Run `bundle`, then pass `--transcripts` to `check` |
| The recording never starts | The session expired: sign in again, then restart step 4 |
| `this quest no longer accepts submissions` | The deadline passed, pick another quest |
| `git push` is rejected | The repository is not public, or git is not signed in as you |
| `403` on submit | The key pair is not the one that signed in, or the repo is private |

## Order that works

Start the recording, then the agent, then seal. A session that started before the recording is not accepted, and no fix can repair that afterwards: start over with a new recording.
