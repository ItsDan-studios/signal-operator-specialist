# Signal Operator

A folder-based AI specialist for solo CEOs and founders juggling priorities. Drop this folder into a Claude project and Claude becomes a triage operator that keeps your schedule organized by importance.

## How to use

1. Drop this `signal-operator/` folder into a Claude project (claude.ai/projects).
2. Start your first session with: **"Be my Signal Operator and run onboarding."**
3. Answer the four onboarding questions. The operator will ask one at a time.
4. The operator scaffolds your `signals/`, `noise/`, `completed/`, and `archived/` folders in your project root and hands you back your first triage with a clear next action for today.
5. Every session after that, start with: **"Daily triage — here's what's new"** and tell the operator what changed since your last session. The operator updates your state, pushes back on noise dressed as signal, and tells you what to do today.

## What you get

- A four-bucket triage system (signal / noise / completed / archived) maintained automatically as folders in your project
- A pushback discipline that challenges items pretending to be priorities
- A daily ritual that compounds — your operating picture gets sharper the more you use it
- A clear next action at the end of every session

## What this is NOT

Not a coach. Not a habit tracker. Not a calendar tool. Not a journaling prompt. The Signal Operator does one job — triage — and refuses everything else.

## File structure

```
signal-operator/
├── identity.md              ← Who the operator is
├── rules.md                 ← How the operator behaves
├── examples.md              ← Three sample interactions
├── reference/               ← Methodology, protocols, templates
│   ├── triage-method.md
│   ├── pushback-patterns.md
│   ├── onboarding-protocol.md
│   ├── daily-triage-protocol.md
│   ├── file-ops-conventions.md
│   ├── brief-template.md
│   └── index-template.md
└── README.md                ← This file
```

Built using Interpretable Context Methodology (ICM) — folders as architecture, each file does one job, structure tells you what's where.
