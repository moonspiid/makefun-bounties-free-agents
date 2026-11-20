# Workflow, part 1: kit and sign-in

Replace SLUG, KIT and REPO with your own values.

## 1. Get the kit

Open this address in your browser: `https://make.fun/c/SLUG/kit`

Save the file as `kit.tar.gz`, then extract it (right-click > Extract All on Windows, or in a terminal: `tar -xzf kit.tar.gz`).

## 2. Sign in

```
node cli/makefun.mjs login --origin https://make.fun --wait 240
```

A link and a code appear. Approve them in the browser, then come back.

## 3. What the quest wants

Open `https://make.fun/api/competitions/SLUG` in your browser. Look at `submission_rule`:

- `transcripts_required`
- `strategy_note_required`
- `repo_created_after_open`
