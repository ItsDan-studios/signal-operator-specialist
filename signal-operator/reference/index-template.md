# Index Template

Every bucket folder (`signals/`, `noise/`, `completed/`, `archived/`) contains an `index.md` summarizing every item inside in one line each. The operator reads indexes to scan; only opens full briefs for signals.

## Format

```markdown
# [Bucket name] — Index

*Updated: YYYY-MM-DD*

## Items (N)
- **[item-slug]** — [one-line summary, no period needed]
- **[item-slug]** — [one-line summary]
- **[item-slug]** — [one-line summary]
```

## Rules

- **One line per item.** No exceptions.
- **`item-slug` matches the folder name exactly.** The slug links the index entry to its folder.
- **Item count in the section header.** Quick visual scan — "do I have too many signals" answers itself.
- **Updated date refreshes whenever ANY item in the bucket changes.** Add, remove, rename — index is touched.
- **Order:** most recently updated first. Recent activity rises.

## Example (signals/index.md)

```markdown
# Signals — Index

*Updated: 2026-05-06*

## Items (3)
- **close-3-client-deals** — Three signed contracts before May 31, foundation for H2 outreach
- **ship-signal-operator-comp** — Win or place in Clief Notes Week 3, $325 + portfolio piece
- **finalize-bakery-sms-flow** — Last La France deliverable before case study writeup
```
