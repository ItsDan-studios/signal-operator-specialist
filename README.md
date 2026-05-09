# Signal Operator - A Folder-Based AI Specialist

Signal Operator is a drop-in Claude specialist for solo CEOs and founders who need a sharper signal-vs-noise filter. It helps you decide what actually deserves attention right now, turns a crowded pile of priorities into a live board, and protects focus from productive-looking drift.

This is not a generic productivity assistant. It is a folder-based operator built around one idea: signal is the few things that actually move the mission forward. Everything else is noise until the signal is handled.

## The problem it solves

Most founders do not lose because they have nothing to do. They lose because too many things feel important at once.

Client work, outreach, internal systems, new tools, follow-up ideas, and low-grade urgency all compete for the same attention. The result is motion without clarity.

Signal Operator exists to answer one question cleanly:

`What actually deserves my attention right now?`

## What this repo contains

The actual deliverable is the `signal-operator/` folder.

```text
signal-operator/
|- identity.md
|- rules.md
|- examples.md
|- reference/
`- README.md
```

That folder contains the specialist itself:

- `identity.md` defines who the operator is and how it sees signal vs noise
- `rules.md` defines the read order, output contract, and operating constraints
- `examples.md` shows the operator's voice and decisions in practice
- `reference/` contains the doctrine, protocols, templates, and ranking logic
- `README.md` tells the end user exactly how to start

Inside `reference/`, the specialist has explicit operating doctrine instead of vague prompting:

```text
reference/
|- triage-method.md
|- onboarding-protocol.md
|- daily-triage-protocol.md
|- pushback-patterns.md
|- signal-ranking.md
|- brief-template.md
|- index-template.md
|- file-ops-conventions.md
|- user-context-template.md
`- common-noise-patterns.md
```

## What Claude creates during use

The specialist stays reusable. The user state is created separately under `signal-state/`:

```text
signal-state/
|- user-context.md
|- signals/
|- noise/
|- completed/
`- archived/
```

That separation is the point:

- the specialist folder is the reusable operating system
- the state folder is the live board for the current user

## How it works

Signal Operator runs in two phases:

1. `Phase 1: Build User Context`
It learns how the user works, what kinds of work compete for attention, what usually counts as signal, and what usually becomes noise.

2. `Phase 2: Build First Signal Board`
It takes the current work inventory, pushes back on weak signal candidates, and locks a board with up to 3 active signals.

After onboarding, future sessions read the existing context and board, update the files, and return a clear first move.

## What you get

When the specialist is working properly, the output is not a vague productivity conversation. It ends with a locked board and a direct instruction:

```md
**Board locked.**

**Active signals:**
1. [signal] - [why it holds this slot]
2. [signal] - [why it holds this slot]
3. [signal] - [or fewer if fewer are real]

**Dropped to noise:**
- [item] - [reason]

**Completed / archived changes:**
- [item] - [change]

**Work this first:**
[direct instruction]
```

In practice, that means the operator:

- keeps the active signal set small
- allows fewer than 3 signals when that is the honest board
- pushes blocked work out of signal
- pushes back on productive-looking drift
- separates live work from dead work
- maintains explicit state so future sessions do not have to guess

## Who it's for

Signal Operator is for:

- solo CEOs and founders juggling too many active fronts
- operators who need help separating leverage from distraction
- builders who are prone to productive-looking drift
- people who want a sharper focus system, not more motivational talk

It is especially useful when the problem is not laziness, but dilution:
too many good ideas, too many side quests, and not enough clarity on what actually moves the mission forward today.

## What it's not for

It is not a:

- coach
- planner
- journal
- calendar tool
- therapist
- generic productivity bot

If the need is emotional support, time blocking, or broad strategic brainstorming, this is the wrong specialist.

## Quick start

1. Clone this repo or download the `signal-operator/` folder.
2. Drop `signal-operator/` into a Claude Project.
3. Start with: **"Be my Signal Operator and run onboarding."**
4. Phase 1 builds the user context.
5. Phase 2 builds the first signal board under `signal-state/`.

Full usage instructions for the end user live in [`signal-operator/README.md`](signal-operator/README.md).

## Methodology

Built using Interpretable Context Methodology (ICM): the specialist stays reusable, the user state stays explicit, and the read path stays interpretable.

## License

MIT.
