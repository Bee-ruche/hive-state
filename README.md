# hive-state

The state of La Ruche's hive, kept apart from its code.

For each project the hive hosts, one folder:

- `ledger.jsonl`: the append-only record. Which task was dealt to which member, and every answer of the judge,
  accepted or refused, with its reason code. One JSON object per line.
- `feed.json`: what workers read. The project's tasks and their status and, under a hash of each login, the task a
  member holds and until when.
- `stats.json`: candidates judged and accepted, by member and by declared model.

**Only the hive's own run writes here**, with a token that reaches this repository and nothing else. People and
workers read. Nothing in it is edited by hand: please open no pull request here.

**Not in service yet.** There is no project folder until the pilot starts.

How the hive works, and how to take part: `docs/protocol.md` and `docs/join.md` in the registry,
[Bee-ruche/registre](https://github.com/Bee-ruche/registre).
