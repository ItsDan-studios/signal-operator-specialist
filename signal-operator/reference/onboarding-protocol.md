# Onboarding Protocol

Onboarding is a two-phase process. Do not skip Phase 1 and do not merge both phases into one loose exchange.

## Phase 1: Build User Context

Goal: create `signal-state/user-context.md` before any board is built.

Use `user-context-template.md` as the structure and `common-noise-patterns.md` when the user needs examples.

### Section flow

Walk the user through these sections:

1. role and business context
2. current operating period
3. recurring work streams
4. known bottlenecks
5. confirmed signal criteria
6. confirmed noise patterns
7. decision notes

Use guided prompts with examples. Do not force fake answers. If the user does not know, write `Not yet clear`.

Monthly and weekly goals are optional, not required.

### Draft and confirm

When enough context is gathered:

1. draft `signal-state/user-context.md`
2. show a concise summary
3. ask `confirm or revise?`
4. update the file if needed

Only after the user confirms does Phase 2 begin.

## Phase 2: Build First Signal Board

Goal: create the first live board under `signal-state/`.

### Ask for these inputs

1. active work inventory
2. real deadlines / hard clocks
3. what the user thinks the 3 signals are

The third question matters. The user should be forced to think before the operator locks the board.

### Classification rules

- board supports up to 3 active signals
- fewer than 3 is allowed
- everything else becomes noise unless already completed or explicitly dead
- blocked or non-actionable items belong in noise
- archive is not the normal pushback outcome

### Build the state

Create:

```text
signal-state/
├── user-context.md
├── signals/
├── noise/
├── completed/
└── archived/
```

Then:

- create `index.md` in each bucket
- create `brief.md` for each classified item
- rank the active signals using `signal-ranking.md`

### Close

End onboarding with the output contract from `rules.md`.
