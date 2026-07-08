# Video Prompts

Use this reference for Seedance-style all-reference video prompts and other image-to-video tools.

## Output Structure

Use this structure by default:

```text
Reference responsibilities:
Timing / blocking:
Sound:
Color and light:
Ending:
Forbidden:
```

For compact mode keep it under the user's requested limit. If no limit is given, prefer concise but complete.

## Reference Responsibilities

For every uploaded image, say:

- what it controls
- what it does not control
- whether it is appearance, scene, blocking, lighting, motion, effect region, or endpoint

Example:

```text
Image 1 controls the character face, hair, costume, body proportion, and identity. It does not control scene layout or camera movement.
```

Do not write fake `Image 1` labels unless the user or target platform uses them. If the user will upload manually, describe the reference by filename or role.

## All-Reference Mode

Do not force first-frame / last-frame / keyframe generation. Decide:

- no frame needed: simple scene or stable action
- start / end frame: exact beginning and ending states matter
- middle key image: one visual explosion or transformation must be locked
- storyboard strip: sequence order matters
- blocking/control diagram: spatial logic matters
- video reference: complex camera motion matters

## Raw Video Sound Rule

For raw generated video:

- allow dialogue, voice, sound effects, ambience, Foley
- forbid background music, BGM, score, drums, chanting, epic music bed

Final edit music is a separate post-production decision.

## Prompt Gate

Before outputting a final video prompt check:

- mode selected
- input references and responsibilities clear
- one main narrative task
- current action and ending state clear
- time feasible
- original dialogue checked
- voice consistency checked
- no background music in raw generation
- M5 reference readiness checked if using model references

If a check fails, output missing items instead of the prompt.
