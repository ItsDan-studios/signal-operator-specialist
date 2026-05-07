# Signal Operator — A Folder-Based AI Specialist

A drop-in Claude specialist that turns Claude into a triage operator for solo CEOs and founders juggling priorities. Built using Interpretable Context Methodology (ICM).

## What this is

The `signal-operator/` folder in this repo is a complete AI specialist. Drop it into a Claude project (claude.ai/projects) and Claude becomes the Signal Operator — a triage specialist that keeps your operation organized into four buckets (signal, noise, completed, archived) and pushes back when items pretend to be priorities.

## Quick start

1. Clone this repo (or download the `signal-operator/` folder).
2. Drop the `signal-operator/` folder into a Claude project.
3. Start a chat with: **"Be my Signal Operator and run onboarding."**
4. Answer four onboarding questions.
5. The operator scaffolds your state folders, runs your first triage, and tells you what to do today.

Full usage instructions: [`signal-operator/README.md`](signal-operator/README.md).

## How it works

The specialist is a folder of markdown files. Each file does one job:

| File | Job |
|---|---|
| `identity.md` | Who the operator is and what it does/doesn't cover |
| `rules.md` | The behavioral policy (terse, points to detailed protocols) |
| `examples.md` | Three sample sessions showing the operator in action |
| `reference/` | Detailed protocols, methodology, templates, pushback patterns |
| `README.md` | One-paragraph cold-start for users |

Claude reads the folder, becomes the specialist, and operates against the rules.

User state (the four bucket folders) lives separately in the user's Claude project root, created and maintained by the operator automatically. State is never inside the specialist folder — clean separation between the immutable specialist and the user's evolving operating picture.

## Built for

Solo CEOs and founders who run too many fronts and need an operator-style triage partner — not a coach, not a productivity app, not a calendar tool. Triage and only triage.

## Methodology

Built using Interpretable Context Methodology (ICM): folders as architecture, each file does one job, structure tells you what's where. The specialist itself models ICM at the file level; the user's state folders extend the same pattern at the data level.

## License

MIT.
