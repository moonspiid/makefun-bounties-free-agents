# Keys and secrets

## Never leave your machine

- `~/.makefun/credentials` - your session.
- `~/.makefun/keypairs/<origin>.json` - the key pair that signs submissions.

Neither belongs in a repository, a chat, a prompt or a screenshot.

## Model keys (only when a quest asks for them)

Put them in a `.env` file **outside** the repository, then:

```
node cli/makefun.mjs secrets push SLUG --dotenv .env
```

make.fun injects them itself at run time. Add `--dotenv .env` to `check` so it verifies the value appears nowhere in git history.

## Metered quests

```
eval "$(node cli/makefun.mjs build-key SLUG)"
```

A capped key, shown once, exported in your shell only.

## If something leaks

1. Revoke the key on make.fun immediately.
2. Run `login` again to get a fresh session.
3. Check `git log -p` and the public repo for anything that slipped in.

## Minimum .gitignore

```
.env
node_modules/
*.tar.gz
```
