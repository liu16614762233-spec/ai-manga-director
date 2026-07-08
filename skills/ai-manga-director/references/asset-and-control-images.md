# Asset And Control Images

Use this reference when planning images, reference uploads, and control diagrams for image-to-video models.

## Principle

Separate **production assets** from **director control images**.

Production assets lock appearance:

- character reference board
- scene master
- prop / monster / vehicle design
- costume / equipment breakdown
- color / light reference

Control images explain execution:

- storyboard strip
- start / middle / end frame
- spatial blocking map
- camera movement guide
- action pose sequence
- effect region / forbidden-zone map
- composition guide
- lighting diagram

## High-Frequency Control Decision

Check in this order:

1. Character / prop / monster / vehicle design: required when identity or structure matters.
2. Scene master: required when location, geography, or continuity matters.
3. Color / light / mood: prompt-only for simple cases; image reference for strong style continuity.
4. Storyboard strip: use for shot order or 15-second segment rhythm.
5. Spatial blocking map: use when 3+ key objects or directions may confuse the model.
6. Action path / pose sequence: use for walk, chase, fall, fight, creature motion.
7. Camera movement guide or video reference: use for complex moving camera.
8. Effect region / forbidden-zone map: use for smoke, fire, fog, blood, magic, water, dust, explosion, or spread control.
9. Start / middle / end frames: use when exact visual states matter.

Low-frequency controls such as axis diagrams, nine-grid exploration, transition reference, or recovery frames are optional. Mention them only when a specific risk triggers them.

## Model-Facing Or Internal

For each control image state:

- `MODEL_REFERENCE`: upload to the video model.
- `PLAN_ONLY`: use only to explain decisions to the user or GPT.
- `NOT_NEEDED`: skip.

Do not ask the user to upload plan-only diagrams to the model.

## Asset List Format

```text
Asset:
Type:
Purpose:
Needed now: yes/no
Model-facing: yes/no
Reason:
Risk if missing:
Status:
```

## Key Gate

If main characters or necessary scenes appear, do not generate dependent control images first. Generate or approve the character reference board and scene master before formal storyboards, blocking maps, keyframes, or video prompts.
