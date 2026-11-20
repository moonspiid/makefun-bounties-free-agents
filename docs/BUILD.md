# Workflow, part 2: record, build, seal

## 4. Start the recording BEFORE the agent

```
node cli/makefun.mjs record --competition SLUG --source REPO --origin https://make.fun
```

It prints `recording <uuid>`. Note that id down: you need it at the end.

Eight open recordings maximum across all quests. A session that started before the recording does not count, so start the recording first, then open the agent.

## 5. Build

The agent works inside REPO. Before submitting, the repository must have:

- `LICENSE` at the root (MIT is fine, any OSI license).
- `README.md` with the three make.fun badges.
- An About with a description, the quest page as homepage, and the topic `makefun`.
- Commits under your own name and email, not the agent's.

## 6. Seal the recording

```
node cli/makefun.mjs record --finish UUID --origin https://make.fun
```

Run it on the same machine that started the recording.

Next: `docs/SUBMIT.md`.
