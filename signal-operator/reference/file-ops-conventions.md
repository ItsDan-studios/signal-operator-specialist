# File Operations Conventions

The operator owns file operations. The user should not have to manage the board manually.

## Mutable state layout

All mutable state lives under:

```text
signal-state/
├── user-context.md
├── signals/
│   ├── [item-slug]/
│   │   └── brief.md
│   └── index.md
├── noise/
│   ├── [item-slug]/
│   │   └── brief.md
│   └── index.md
├── completed/
│   ├── [item-slug]/
│   │   └── brief.md
│   └── index.md
└── archived/
    ├── [item-slug]/
    │   └── brief.md
    └── index.md
```

## Slug rules

Use lowercase `kebab-case`.

Prefer:

- action-oriented wording
- enough specificity to be scannable in an index

Good:

- `cold-outbound-campaign-launch`
- `warm-lead-ranking`
- `email-campaign-audit-optimization`

Bad:

- `campaign`
- `new-idea`
- `thing-to-fix`

## Movement rules

Move the whole folder, not just the brief.

Common moves:

- `signal-state/signals/` -> `signal-state/completed/`
- `signal-state/signals/` -> `signal-state/noise/`
- `signal-state/noise/` -> `signal-state/signals/`
- `signal-state/noise/` -> `signal-state/archived/`
- `signal-state/completed/` -> `signal-state/archived/` only when intentionally clearing old history

Blocked or non-actionable work should move out of `signal-state/signals/` and into `signal-state/noise/`.

## Update rule

Whenever an item changes:

- folder location must match status
- brief status must match folder
- brief `Updated` date must change
- source index must change
- destination index must change

Never leave state half-updated.

## Delete rule

Default to archive over delete.

If the user asks to remove something, confirm whether they mean:

- move to `signal-state/archived/`
- permanently delete

The operator should not initiate permanent deletion on its own.
