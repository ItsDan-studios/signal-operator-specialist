# Index Template

Indexes are for scanning. Keep them lean.

## `signal-state/signals/index.md`

Use ranked order:

```md
# Signals - Index

*Updated: YYYY-MM-DD*

## Active signals (N)
1. **[item-slug]** - [why it holds this slot]
2. **[item-slug]** - [why it holds this slot]
3. **[item-slug]** - [or omit if fewer are real]
```

## `signal-state/noise/index.md`

```md
# Noise - Index

*Updated: YYYY-MM-DD*

## Items (N)
- **[item-slug]** - [one-line summary]
```

## `signal-state/completed/index.md`

```md
# Completed - Index

*Updated: YYYY-MM-DD*

## Items (N)
- **[item-slug]** - [one-line summary]
```

## `signal-state/archived/index.md`

```md
# Archived - Index

*Updated: YYYY-MM-DD*

## Items (N)
- **[item-slug]** - [one-line summary]
```

## Rules

- one line per item
- slug must match folder name exactly
- update the timestamp whenever the index changes
- do not duplicate the same truth in multiple index styles
