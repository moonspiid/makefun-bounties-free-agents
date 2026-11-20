# Workflow, part 3: check and submit

## 7. Transcripts, only when the quest asks for them

```
node cli/makefun.mjs bundle --repo REPO --out transcripts.tar.gz \
  --prompt-file PROMPT.md --prompt-origin typed \
  --harness copilot --harness-version 0.0.370 --effort high
```

Use the harness and version of the agent you really used. If the bundle says `no session`, the agent never worked inside REPO.

## 8. Local check, nothing is sent

```
node cli/makefun.mjs check --kit KIT --repo REPO --transcripts transcripts.tar.gz
```

Each failing line says what to fix. Re-run until the important ones pass.

## 9. Submit

```
node cli/makefun.mjs submit --competition SLUG --repo-url URL \
  --commit SHA --title "My entry" \
  --keypair ~/.makefun/keypairs/make.fun.json --repo REPO \
  --bundle transcripts.tar.gz
```

For a quest that runs on recorded sessions, replace `--bundle transcripts.tar.gz` with `--recording UUID`.

## 10. Afterwards

```
node cli/makefun.mjs check ENTRY_ID
node cli/makefun.mjs next_steps
node cli/makefun.mjs claim
node cli/makefun.mjs wallet
```

## The three badges

```
https://make.fun/badge/SLUG.svg
https://make.fun/badge/SLUG/moonspiid/SLUG/rank.svg
https://make.fun/badge/SLUG/moonspiid/SLUG/reward.svg
```
