# Quickstart

This guide shows how to use AI Manga Director with any capable agent.

## 1. Load The Pack

If your platform supports knowledge files, upload:

```text
skills/ai-manga-director/SKILL.md
skills/ai-manga-director/references/*.md
```

If your platform only supports one instruction field, paste:

```text
UNIVERSAL_AGENT_PROMPT.md
```

## 2. Start In Compact Mode

Use:

```text
Use AI Manga Director in compact mode. First identify my task type, current gate, missing required assets, and the next allowed action. Do not write a final video prompt until gates pass.
```

Compact mode should return:

```text
Status:
Gate:
Main issue:
Next action:
```

## 3. Give It A Script Or Project

For a new story:

```text
Here is my 1-minute script. Run writing-to-production handoff. Do not generate images yet.
```

For an existing project:

```text
Continue this project from the approved assets. First check gates and missing assets.
```

## 4. Ask For Asset Planning

```text
Run minimum necessary asset planning. List main characters, required scenes, key props, sound anchors, and control images. Mark must-have, optional, and not needed.
```

Expected output:

```text
Asset:
Type:
Purpose:
Needed now:
Model-facing:
Reason:
Risk if missing:
Status:
```

## 5. Ask For Director Blocking

```text
Run director blocking preview for this 15-second segment. Include timing, shot size, camera movement, action beat, micro-expression, environmental motion, transition, sound bridge, and ending state.
```

Do not ask for the final video prompt until the blocking and asset gates pass.

## 6. Ask For A Video Prompt

```text
Generate a Seedance-style 15-second image-to-video prompt. First check reference responsibilities, original dialogue, timing feasibility, and raw sound rules.
```

The output should include:

```text
Reference responsibilities:
Timing / blocking:
Sound:
Color and light:
Ending:
Forbidden:
```

## 7. Review A Result

```text
Review this sample video. Suggest the smallest rework that preserves the current shot.
```

Expected output:

```text
Pass / fail:
Main failure:
Keep unchanged:
Change only:
Revised prompt fragment:
Next test:
```

## Common Mistakes

- Asking for a final video prompt before the main character reference exists.
- Uploading many references without saying what each one controls.
- Treating a storyboard or control diagram as a final visual asset.
- Letting a generated prompt create new project facts.
- Adding background music to raw video generation when the model should only generate dialogue, ambience, and effects.
- Rewriting the whole prompt after a near-good sample instead of fixing one highest-risk issue.
