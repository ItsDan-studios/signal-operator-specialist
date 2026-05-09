# Signal Operator - A Folder-Based AI Specialist

Signal Operator is a drop-in Claude specialist for solo CEOs and founders who need a sharper signal-vs-noise filter. It helps you decide what actually deserves attention right now, turns a crowded pile of priorities into a live board, and protects focus from productive-looking drift.

This is not a generic productivity assistant. It is a folder-based operator built around one idea: signal is the few things that actually move the mission forward. Everything else is noise until the signal is handled.

## The problem it solves

Most founders do not lose because they have nothing to do. They lose because too many things feel important at once.

Client work, outreach, internal systems, new tools, follow-up ideas, and low-grade urgency all compete for the same attention. The result is motion without clarity.

Signal Operator exists to answer one question cleanly:

`What actually deserves my attention right now?`

## What's in here

The actual deliverable is the `signal-operator/` folder.

```text
signal-operator/
├── README.md                  ← start here
├── identity.md                ← who the operator is and how it sees signal vs noise
├── rules.md                   ← read order, output contract, and operating constraints
├── examples.md                ← example onboarding, triage, pushback, and future sessions
└── reference/                 ← the operating doctrine behind the specialist
    ├── triage-method.md         ← what earns signal vs what falls to noise
    ├── onboarding-protocol.md   ← Phase 1 and Phase 2 onboarding flow
    ├── daily-triage-protocol.md ← how later sessions update the live board
    ├── pushback-patterns.md     ← structured challenge patterns for weak signal candidates
    ├── signal-ranking.md        ← how the operator orders active signals
    ├── brief-template.md        ← structure for each item brief
    ├── index-template.md        ← structure for bucket indexes
    ├── file-ops-conventions.md  ← how state is created, moved, and maintained
    ├── user-context-template.md ← structure for the durable user profile
    └── common-noise-patterns.md ← common productive-looking traps to watch for
```

This is what gives the specialist depth. It is not one prompt file pretending to be a system. It is a portable operator with explicit identity, rules, examples, and reference doctrine.

## What Claude creates during use

The specialist stays reusable. The user state is created separately under `signal-state/`.

```text
signal-state/
├── user-context.md                       ← durable profile built in Phase 1
├── signals/
│   ├── index.md                          ← ranked active signals for the current board
│   ├── cold-outbound-campaign-launch/
│   │   └── brief.md                      ← live signal example
│   └── skool-competition-submission/
│       └── brief.md                      ← another active signal example
├── noise/
│   ├── index.md                          ← real work that does not deserve a slot right now
│   └── godspeed-integration/
│       └── brief.md                      ← productive-looking drift example
├── completed/
│   ├── index.md                          ← finished work
│   └── warm-lead-ranking/
│       └── brief.md                      ← completed item example
└── archived/
    ├── index.md                          ← intentionally dead or dropped work
    └── old-offer-angle/
        └── brief.md                      ← archived item example
```

That separation is the point:

- `signal-operator/` is the reusable operating system
- `signal-state/` is the live board created for the current user

## How it works

Signal Operator works in three stages:

### 1. Phase 1: Build User Context

The operator builds a durable profile of how the user works:

- what kind of business or work they run
- what work streams compete for attention
- what usually counts as signal
- what usually becomes noise
- what tradeoffs should usually win

This becomes `signal-state/user-context.md`.

### 2. Phase 2: Build First Signal Board

The operator takes the current work inventory, asks what the user thinks deserves signal, pushes back on weak candidates, and creates the first live board.

That means:

- up to 3 active signals
- everything else routed to noise, completed, or archived
- ranked active signals
- a clear first move

### 3. Future sessions: Update the board

Future sessions do not restart from scratch.

The operator reads the existing `user-context.md`, active signals, noise, completed, and archived items, then compares that state against whatever is new today.

That means later sessions can:

- close finished signals
- demote blocked work to noise
- promote new signal candidates
- challenge productive-looking drift
- update the board without losing continuity

The result is not just onboarding. It is an ongoing signal-vs-noise operating system.

## What you get back

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
