# File Operations Conventions

How the Signal Operator names, creates, moves, and archives files in the user's project. The operator handles all of this automatically — the user never manages files manually.

## Folder layout

The operator maintains four bucket folders in the user's project root (NOT inside the `signal-operator/` folder):

```
signals/
├── [item-slug]/brief.md
└── index.md

noise/
├── [item-slug]/brief.md
└── index.md

completed/
├── [item-slug]/brief.md
└── index.md

archived/
├── [item-slug]/brief.md
└── index.md
```

## Naming convention

**Folder slugs:** `kebab-case`, lowercase, action-oriented when possible.

- ✅ `close-3-client-deals`
- ✅ `ship-signal-operator-comp`
- ✅ `finalize-bakery-sms-flow`
- ❌ `Close 3 Client Deals` (spaces, capitals)
- ❌ `client_deals` (underscore, vague)
- ❌ `parker-deal` (vague — what about it)

Slugs should be specific enough that scanning the index gives the operator full context without opening the brief.

## Movement rules

When an item changes status, the operator moves the **entire folder** (not just the brief). This keeps the file structure as the single source of truth for state.

| From | To | Trigger |
|---|---|---|
| signals → completed | User reports the outcome was reached |
| signals → noise | Triage decided this no longer earns signal status this period |
| signals → archived | User decides to abandon the pursuit |
| noise → signals | Context changed; this now advances the north star |
| noise → completed | User completed it without it ever being a signal |
| noise → archived | Periodic review found it is no longer relevant |
| completed → archived | Cleanup of old completed items (rare; usually leave them) |

After every move, the operator updates BOTH the source bucket's `index.md` (remove entry) AND the destination bucket's `index.md` (add entry).

## Index update rule

ANY change to a bucket triggers an `index.md` rewrite for that bucket:

- New item created → add line to index
- Item renamed → update line in index
- Item moved out → remove line from index
- Item brief updated → may update the index line if the summary changes

The operator never leaves an index out of sync. If the operator detects mismatch (folder exists, no index entry, or vice versa), the operator surfaces this to the user and offers to reconcile.

## Archive vs delete

The operator **defaults to archive over delete** — always. If the user asks to "delete" something, the operator confirms: *"Move to archived/ (recoverable) or permanently delete (gone)?"* before acting.

The user can manually delete the `archived/` folder contents anytime they want a clean slate. The operator does not initiate deletions.

## Renaming

Item renames change the folder name AND the brief title AND the index line. All three update together. The operator never leaves a partial rename.

## Conflict handling

If the user provides input that creates ambiguity (e.g., "move the Parker thing to completed" when there are two items with "parker" in the slug), the operator asks one clarifying question before acting. No silent assumptions on file moves.
