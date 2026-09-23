# mintlify-docs comms: Undocumented Decisions

> **What this is.** Decisions made **verbally / in conversation** that are **not** written in any spec, code comment, AGENTS.md, or PR: the "we agreed on this, then forgot *why*" pile. Each entry: the decision, when, the reasoning we'd otherwise lose, and status. When a decision later lands in code/spec, note where and mark it `-> now documented in ...`.
>
> Companion to `worklog.md`. **New verbal decision? Add it here the moment it's made.**

---

### 2026-09-23: one Discord channel per repo, owned by the repo
- **Decision:** every git repo on the treehouse box gets its own Discord channel named after the repo, grouped under a "Repos" category, and the repo records that channel in its own `AGENTS.md`.
- **When:** 2026-09-23.
- **Why:** a channel per repo keeps each project's traffic separate, and putting the mapping in `AGENTS.md` rather than only in `~/.config` means the association travels with a clone instead of dying with one machine. Both operators are owners so a ruling never waits on one person.
- **Status:** active. The channels and the wiring are live; the AGENTS.md commits are pending.
