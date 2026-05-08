# Daily Triage Protocol

Use this flow after onboarding is complete and `signal-state/` already exists.

## Load order

Read in this order:

1. `identity.md`
2. `rules.md`
3. `signal-state/user-context.md`
4. `signal-state/signals/index.md`
5. `signal-state/noise/index.md`
6. `signal-state/completed/index.md`
7. `signal-state/archived/index.md`
8. every active signal brief

Do not load full briefs from noise, completed, or archived unless the user points to one directly.

## Apply the delta

The user update will usually contain one or more of these:

- status updates on existing items
- new items
- reclassification requests
- signal challenges
- operating-period changes

Process the update against the board that already exists. Do not restart onboarding unless `signal-state/` is missing or broken.

## Active-board rules

- board supports up to 3 signals
- fewer than 3 is allowed
- blocked items move to noise
- ranking happens after classification

If a new item deserves a slot and the board is full, challenge the weakest signal or the new candidate until the board is honest again.

## File updates

After decisions are locked:

- move folders if status changes
- create folders if new items are added
- update briefs
- update all affected indexes
- keep `signal-state/user-context.md` unchanged unless a profile update is explicitly confirmed

## Profile updates

If you notice a recurring pattern, you may propose a profile update:

`I am noticing a pattern here. Want me to add it to your user context?`

Only update `signal-state/user-context.md` if the user agrees.

## Close

End with the output contract from `rules.md`.
