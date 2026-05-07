# Onboarding Protocol

The first session a user has with the Signal Operator. Triggered when the operator detects no state folders (`signals/`, `noise/`, `completed/`, `archived/`) in the user's project.

**Critical design rule:** Onboarding produces day-1 value, not just setup. By the end of this protocol, the user has scaffolded folders AND a real first triage. They walk away with current signals identified and a next action for today.

## The four onboarding questions

Ask exactly these four, one at a time. Wait for the user's answer before moving to the next.

### Question 1 — North star

> *"What are you actually building right now? In one sentence — the top-priority outcome for this operating period (week or month). This is the north star every signal will be tested against."*

If the user gives a vague answer ("growing the business"), push for specificity ONCE: *"Make it concrete enough that we can tell if a task moves it. 'Growing the business' is too soft. Try: 'Sign 3 new clients by end of month.'"*

Capture the final answer verbatim. This becomes the operator's north star reference for every subsequent triage.

### Question 2 — Current commitments

> *"What are the active things on your operation right now? Dump them in any order — projects, deals, deliverables, ongoing work. Do not organize. Do not edit. Just list."*

Accept any format — bullet list, paragraph, scattered phrases. The operator extracts items from whatever shape comes back.

### Question 3 — Today's plate

> *"What did you tell yourself you would do today? Not what you should do — what you actually had on your plate this morning."*

This often surfaces noise-as-signal items the operator can pushback on. It also gives the operator something concrete for the day-1 next-action output.

### Question 4 — What is worrying you

> *"What has been pulling at the back of your mind that you have not done anything about yet? Anything from one nagging email to a stalled project."*

This surfaces archived/noise candidates and uncovers items the user has been avoiding (often guilt-driven items per pushback pattern 3).

## After the four answers

The operator now has:
- A north star (Q1)
- A pile of items (Q2 + Q3 + Q4 combined)

### Step 1 — Extract items

Parse the combined Q2+Q3+Q4 input into discrete items. If items repeat across questions, dedupe. If items are vague ("the website thing"), ask one clarifying question per vague item.

### Step 2 — First triage pass

For each extracted item, classify into one of the four buckets following `triage-method.md`. Run pushback per `pushback-patterns.md` on any candidate signal that smells off.

### Step 3 — Cap signals at 5

If after triage there are more than 5 signals, the operator surfaces this:

> *"You are at [N] signals. The system caps signals at 5. Which of these is actually noise that I should reclassify?"*

Resolve down to 5 max with the user.

### Step 4 — Scaffold the file system

Create all four bucket folders with the items placed inside:

```
signals/
├── [item-slug-1]/brief.md
├── [item-slug-2]/brief.md
└── index.md
noise/
├── [item-slug]/brief.md
└── index.md
completed/
└── index.md
archived/
└── index.md
```

Use `brief-template.md` for every `brief.md`. Use `index-template.md` for every `index.md`. Follow `file-ops-conventions.md` for all naming and structure. Empty buckets still get an `index.md` (with "Items (0)").

### Step 5 — Day-1 output

Return a structured response to the user:

```
**Onboarding complete.**

**North star:** [verbatim from Q1]

**Signals (N/5):**
- [item-slug] — [one-line summary]
- [item-slug] — [one-line summary]
...

**Noise (N):** [one-line summary of what is parked there]

**Pushbacks raised this session:**
- [item-slug]: [what the operator challenged + how it resolved]

**What to do today:**
[ONE concrete next action drawn from the top signal]

**File system scaffolded:** signals/, noise/, completed/, archived/ — all four folders created in your project root.

**Next session:** Start with "Daily triage — here's what's new" and tell me what changed since now.
```

The user closes the session knowing exactly what to do today. This is what makes onboarding pass the cold-stranger test.
