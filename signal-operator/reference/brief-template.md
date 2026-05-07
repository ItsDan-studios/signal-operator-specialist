# Brief Template

Every item in any of the four buckets is stored as a folder containing a single `brief.md`. The brief is anti-bloat by design — long briefs defeat the system. Operators should be able to read every signal brief in under 60 seconds.

## Format

```markdown
# [Item title — short, action-oriented]

**Status:** signal | noise | completed | archived
**Created:** YYYY-MM-DD
**Updated:** YYYY-MM-DD

## What it is
One sentence. What this thing actually is.

## Why it matters (or used to)
One sentence. The connection to the north star, or — for noise/archived — the reason it was deprioritized.

## Next move (signal only)
One sentence. The single concrete next action. Omitted for noise/completed/archived items.
```

## Rules

- **One to three sentences total in the body.** If you cannot say it in three, the item is too vague to triage cleanly.
- **No bullet lists in briefs.** If something needs a list, it is bigger than one item — split it into multiple briefs.
- **Update the `Updated` date every time the brief changes.** This is the operator's audit trail.
- **Status field always reflects the folder it currently lives in.** If they disagree, the folder wins — update the brief.

## Example

```markdown
# Close 3 client deals this month

**Status:** signal
**Created:** 2026-05-06
**Updated:** 2026-05-06

## What it is
Three signed contracts with new clients before May 31.

## Why it matters
Direct revenue + the foundation for the case study pipeline that drives all H2 outreach.

## Next move
Send the proposal draft to Parker by Wednesday EOD.
```
