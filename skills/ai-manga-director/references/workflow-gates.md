# Workflow Gates

Use this reference for project setup, task routing, gates, asset status, and next-step control.

## Status Labels

- `DRAFT`: idea, plan, or prompt draft. Not approved.
- `REVIEW`: generated or revised output awaits user review.
- `APPROVED`: user approved for current purpose.
- `MASTER`: approved reusable source asset.
- `MODEL_REFERENCE_READY`: approved and optimized for video model reference.
- `BLOCKED`: cannot safely continue until missing item is provided.

## Project Fact Rules

- Current visible files and user-approved statements are facts.
- Old chat memory is not a fact unless restated or supplied.
- Prompt text does not become project canon.
- Generated assets do not become canon until approved.
- Never claim a local file, custom knowledge file, or project file was read unless it is visible in the current environment.

## Project Runtime Pattern

For each project, expect:

1. project facts / premise
2. script or episode outline
3. character bible
4. visual and sound bible
5. asset gate list
6. continuity ledger

If a project only has a script, run writing-to-production handoff first.

## Production Gate Order

1. Confirm script segment and original dialogue.
2. Confirm main characters and necessary scenes.
3. Confirm approved character reference boards.
4. Confirm necessary scene masters.
5. Confirm key props / monsters / vehicles.
6. Run director blocking and time feasibility.
7. Decide minimum necessary control images.
8. Generate or review assets.
9. Only then produce final video prompt.

## Next-Step Menu

Always end production replies with one clear menu:

- continue asset planning
- generate next asset prompt
- review generated image
- run director blocking
- write video prompt
- review sample video
- rework preserving current sample

Only include options that are allowed by the gate.
