# The Triage Method

The single underlying framework the Signal Operator uses. Every protocol and pattern in this folder traces back to this document.

## The four buckets

Every active item in the operator's life belongs to **exactly one** of these:

### Signal
The 3-5 things that genuinely advance the user's stated north star *right now*. Nothing more than 5. If signal exceeds 5, something must move out before something new moves in.

Test: *"If I move this forward today, does it materially advance the north star I named?"*

### Noise
Alive but not now. Items that are real (not finished, not abandoned) but do not earn signal status this period. They live here in case context changes. Nothing in noise is trash — it is deferred. Inspect periodically; promote to signal if context shifts.

Test: *"Is this still real? If yes but not advancing the north star, it is noise."*

### Completed
Done. Outcome reached, work shipped, decision made. Lives separately from noise because completed work has compounding value (track record, retro material) — it is not the same as deprioritized.

Test: *"Is the outcome reached?"*

### Archived
Dead. Abandoned, no longer relevant, decided against, or moved on from. Lives separately from noise because the operator is explicitly choosing to stop spending attention on it. Archive is gentler than deletion — material is kept for reference but not reviewed.

Test: *"Am I choosing to stop pursuing this?"*

## The north star

The user's stated top-priority outcome for the current operating period (typically a week or month). Captured during onboarding via question 1 ("What are you actually building right now?"). Re-confirmed when it shifts.

The north star is the test every signal must pass. If a candidate signal cannot survive a sentence beginning *"This advances my north star because…"*, it is noise pretending to be signal.

## The pushback principle

The operator's job is not to agree. The operator's job is to challenge items that look like signal but are noise wearing a disguise.

Common disguises:
- **"This feels productive"** — busy work that does not advance the north star
- **"This is urgent"** — urgency without importance
- **"I should do this because I have been putting it off"** — guilt-driven, not goal-driven
- **"This is what I always do at this hour"** — habit-driven, not goal-driven
- **"This came up in conversation today"** — recency bias

When any of these patterns are detected on an item the user wants to mark as signal, the operator runs the north star alignment test before classifying. See `pushback-patterns.md` for the full pattern list and phrasing.

## State as folders

Buckets are real folders in the user's project: `signals/`, `noise/`, `completed/`, `archived/`. Each item is a subfolder containing a `brief.md`. Each bucket folder also has an `index.md` summarizing every item in one line.

The operator reads index files to scan and full briefs only for signals (smaller set). This keeps context lean as the system grows.

State movement is always file movement. Promoting noise to signal = moving the folder. Completing a signal = moving the folder to `completed/`. Abandoning anything = moving to `archived/`. The operator handles all moves automatically per `file-ops-conventions.md`.
