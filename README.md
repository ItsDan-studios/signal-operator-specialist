# Signal Operator - A Folder-Based AI Specialist

A drop-in Claude specialist that helps solo CEOs and founders decide what actually deserves attention right now. It turns a crowded pile of priorities into a live signal-vs-noise board, keeps the active signal set small, and protects focus from productive-looking drift.

## Quick start

1. Clone this repo or download the `signal-operator/` folder.
2. Drop `signal-operator/` into a Claude Project.
3. Start with: **"Be my Signal Operator and run onboarding."**
4. Phase 1 builds your user context.
5. Phase 2 builds your first signal board under `signal-state/`.

Full usage instructions live in [`signal-operator/README.md`](signal-operator/README.md).

## What the folder does

The specialist is packaged as five ICM files:

| File | Job |
|---|---|
| `identity.md` | Who the operator is and what it is for |
| `rules.md` | Short behavioral policy and read order |
| `examples.md` | What good interaction looks like |
| `reference/` | Protocols, doctrine, templates, and ranking logic |
| `README.md` | Cold-start instructions for the end user |

The operator keeps mutable user state separate from the specialist itself:

```text
signal-state/
|- user-context.md
|- signals/
|- noise/
|- completed/
`- archived/
```

## Built for

Solo CEOs and founders juggling too many active fronts, too many good ideas competing at once, and not enough clarity on what actually moves the mission forward today. It is for people who need a sharper focus filter, not a coach, not a planner, and not a generic productivity bot.

## Methodology

Built using Interpretable Context Methodology (ICM): the specialist stays reusable, the user state stays explicit, and the read path stays interpretable.

## License

MIT.
