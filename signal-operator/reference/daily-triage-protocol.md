# Daily Triage Protocol

The flow for every session AFTER onboarding. Triggered when the operator detects state folders already exist in the user's project.

The user starts each session with: *"Daily triage — here's what's new"* (or any natural variant). The operator runs this protocol.

## Step 1 — Load state

In this exact order:

1. Read `signal-operator/identity.md` (re-establish role)
2. Read `signal-operator/rules.md` (re-establish behavior)
3. Read all four `index.md` files (signals, noise, completed, archived) — scan only, no full briefs
4. Read every `brief.md` inside `signals/` — full content (smaller set, worth the context cost)
5. Do NOT read full briefs in noise/completed/archived unless the user references a specific item there

This loads enough state to triage intelligently without bloating context.

## Step 2 — Apply user input as delta

The user's input falls into one of these shapes (and may combine multiple):

### A — Status updates on existing items
*"Closed the Parker deal."* → Move `signals/parker-deal/` to `completed/parker-deal/`. Update both indexes. Update brief status field.

### B — New items
*"Got a new prospect from LinkedIn — Sarah from Acme."* → Triage as new item per `triage-method.md`. Create folder + brief in correct bucket. Update bucket index.

### C — Pushback / reclassification on existing items
*"The bakery SMS thing — kill it."* → Move folder to `archived/`. Update indexes.

### D — Promotions
*"The case study writeup — promote that to signal, it's blocking everything."* → Move from noise to signals (if signals < 5; if at 5, surface the cap and resolve).

### E — North star changes
*"Actually my focus this month shifted to launching the cold outreach product."* → Re-confirm new north star with user. Run a fast re-triage of current signals against the new north star. Anything that no longer advances the new north star moves to noise (with explanation).

## Step 3 — Pushback on suspicious new items

For every NEW signal candidate (not items already in signal being reaffirmed), check against `pushback-patterns.md`. Fire pushback when patterns trigger. Resolve per the pushback resolution rule.

## Step 4 — Maintain the cap

If signals > 5 after applying the delta, surface this and resolve with the user. Never silently let signals exceed 5.

## Step 5 — Update file system

Apply all decided file operations per `file-ops-conventions.md`:
- Create new folders + briefs for new items
- Move folders for status changes
- Update every affected `index.md`
- Update every affected brief's `Updated` date

The operator never leaves the file system half-updated. Every move, every rename, every status change cascades to brief and index in the same operation.

## Step 6 — Structured output

```
**Daily triage complete.**

**North star (unchanged | updated to: [new north star]):** [current north star]

**Signals (N/5):**
- [item-slug] — [one-line summary]
- ...

**Changes this session:**
- Moved: [item] from [bucket] to [bucket] — [reason]
- Created: [item] in [bucket] — [reason]
- Pushback resolved: [item] — [how]

**What to do today:**
[ONE concrete next action drawn from the top signal]
```

Every session closes the same way: a clear next action. The user never leaves a triage session uncertain about what to do.
