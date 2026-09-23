# mintlify-docs comms: Worklog (hivemind)

> **What this is.** One continuously-growing shared log for how this repo talks to its humans on Discord. The shared brain for every agent/session that touches this work.
>
> **Protocol for agents (read this):**
> 1. **On pickup**: read **`north-stars.md`** first (the truth you're checked against; skip only before P-0 has authored it, or for a non-epic/incident pickup), then **Living Status** below + the last 1-2 dated entries. That's enough to start.
> 2. **While working**: when you *decide* something not written in code/spec, also log it in `undocumented-decisions.md` (same folder). When you *learn* or *do* something, it goes here.
> 3. **On wrap**: append a dated `### YYYY-MM-DD: <who/what>: <title>` entry at the **bottom**, and edit **Living Status** in place so it's always true *right now*.
> 4. **Be honest**: log what failed, what's unverified, what's an assumption. A wrong "all green" costs the next agent hours.

---

## Living Status  _(keep current; last updated 2026-09-23)_

- Channel: **#mintlify-docs** (1552406185750175796) in guild SF // HANGAR (1468303388591783999). Bot: VEDA (1477953062533595218).
- Owners (whose reply or tap counts): vikram (1385074958656606302), Khoa (290734274825551872).
- Resolution order `dsc` uses: env `HARNESS_COMMS_*` -> this repo's `AGENTS.md` `comms_*` -> `~/.config/discord-comm/repos/` -> `default.json`. The AGENTS.md keys are what make the mapping travel with a clone.
- Check it: `dsc probe` from this repo prints tier 2 and the channel above.
- OPEN: the `AGENTS.md` `## Communicate` block is written but not committed on this repo's main line yet.

---

## Worklog entries

### 2026-09-23: vikram (Claude Code): repo owns its Discord channel
**Did**
- Wired **#mintlify-docs** (1552406185750175796) as this repo's own Discord channel, under the "Repos" category of SF // HANGAR, via `dsc wire --write --plugin`.
- That wrote `comms_bundle`, `comms_guild`, `comms_channel` and `comms_owners` into this repo's `AGENTS.md`, proved one send and one read in the channel, confirmed MESSAGE CONTENT intent, and opted the channel into the Discord channel plugin.

**Learned / decided**
- The repo owns the mapping, not the machine: `dsc` resolves env `HARNESS_COMMS_*`, then `AGENTS.md` `comms_*`, then `~/.config/discord-comm/repos/*.json`, then `default.json`. The AGENTS.md keys outrank any machine config, so a clone on another box resolves the same channel with no local setup.
- Owners are both operators of the treehouse box, so either can answer a ruling and neither is a single point of failure.
- HONEST: the `AGENTS.md` block is written but **not committed** yet. Until it lands on this repo's main line, the only working copy is `~/.config/discord-comm/repos/` on vikram's account, and a fresh clone resolves nothing. The channel itself, and the send/read proof, are real.

**Next**
- Commit the `AGENTS.md` `## Communicate` block through this repo's normal flow (a PR where the repo's contract requires one), so the mapping ships with the repo rather than living on one machine.
