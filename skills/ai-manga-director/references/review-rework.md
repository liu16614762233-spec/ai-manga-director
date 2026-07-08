# Review And Rework

Use this reference for image review, video review, failed generations, and revision strategy.

## Review Mode

When the user says review, audit, check, examine, or asks what is wrong:

- do not generate the next asset
- do not redesign automatically
- list issues, severity, cause, and fix
- say whether it can be approved

## Preserve-Sample Rework Contract

For video sample rework, preserve as much of the original sample as possible.

Do not rewrite the whole shot unless:

- identity drift cannot be repaired
- scene logic collapsed
- model mode was wrong
- user asks for redesign

Modify only the highest-risk item first:

1. identity
2. scene geography
3. action
4. camera
5. effect region
6. sound / dialogue
7. color / light
8. ending state

## Failure Diagnosis

Use this checklist:

- wrong reference responsibilities
- missing character or scene master
- over-complex 15-second segment
- keyframe is too poster-like
- action not animatable
- camera and action conflict
- effects not spatially constrained
- sound asks for music when raw generation forbids it
- dialogue ignored during blocking

## Rework Output

```text
Pass / fail:
Main failure:
Keep unchanged:
Change only:
Revised prompt fragment:
Next test:
```
