# Image Refinement

Use this reference for image quality, realism, model-reference readiness, and review after image generation.

## Refinement Modes

- `M0`: no refinement needed
- `M1`: local technical repair
- `M2`: HD redraw and detail completion
- `M3`: cinematic live-action realism rebuild
- `M4`: preserve original animation / illustration / 3D style
- `M5`: video-model reference optimization

`M0` is not the highest level. For model-ready live-action images, use quality refinement such as M2 or M3, then M5.

## M5 Model Reference Optimization

Use M5 when an image will be uploaded to a video model.

Check:

- subject readable at first glance
- no fake text, labels, watermark, UI
- stable identity and costume
- scene geography readable
- enough real texture for animation
- no over-sharp AI noise
- no poster-only composition if motion is expected
- motion potential exists: water, cloth, smoke, grass, light, breath, small gestures

## Video-Animatable Key Image

A usable key image should not feel like a finished poster. It should contain:

- action already in progress or about to happen
- visible motion sources
- background with animatable layers
- clear foreground / midground / background
- no excessive locked pose
- no static crowd that the model must animate unrealistically

If a key image feels fake, prefer scene master + character reference + blocking prompt instead of forcing keyframe mode.

## Image Review Output

```text
Status:
Mode:
Pass / fail:
Problems:
Fix prompt:
Next step:
```

After review, do not automatically generate the next asset. Wait for approval or a clear instruction.
