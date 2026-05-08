# The Triage Method

This is the operator's core framework. Everything else in `reference/` should agree with this file.

## The board

The board supports up to 3 active signals.

A signal slot is for work that deserves protected attention right now.

Do not fill the board just to fill it. Empty slots are better than fake signals.

## The four states

### Signal

Signal is one of the few active, actionable items that deserves protected attention right now because it moves the mission, serves a real deadline, removes a real bottleneck, or unlocks execution.

Tests:

- Does this deserve one of the limited active slots right now?
- Can the user actually move it now?
- If it moves today, does something meaningful advance?

### Noise

Noise is real work that does not deserve one of the active slots right now.

Noise is not fake. It is simply not current signal.

Common reasons:

- wrong operating period
- blocked or waiting
- separate track, not current leverage
- productive-looking drift
- planning before execution needs it

### Completed

Completed means the work is done and no longer belongs on the active board.

### Archived

Archived means the work is explicitly dead, abandoned, or intentionally dropped.

Archive is not the default answer for normal triage tension. Most disputes are signal vs noise.

## Operating-period logic

The user-context file defines the current operating period and the tradeoffs that matter for this user.

That file matters because not everything that is important in general is signal right now.

## Actionability rule

If something is blocked, waiting, or not actionable now, it should not occupy a signal slot. It belongs in noise until it becomes workable again.

## Ranking comes after classification

First choose the active signals. Then rank them.

Use `signal-ranking.md` for ordering the signals once the board is chosen.

## State as folders

Mutable state lives in:

```text
signal-state/
├── user-context.md
├── signals/
├── noise/
├── completed/
└── archived/
```

The specialist stays separate. The user state is what changes over time.
