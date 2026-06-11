# Style Profile Template

Personal style profiles are optional. They help the skill move from "less AI-like" to "more like this author."

## Template

```markdown
# User Style Profile

## Who I am

...

## My audience

...

## My writing style

...

## Preserve

- ...

## Avoid

- ...
```

## Compact Input Version

Users can also provide this shorter version:

```markdown
## Personal Style Profile

- Who I am:
- My audience:
- My writing style:
- Preserve:
- Avoid:
```

## Save Rules

- Save persistent personal profiles to `profiles/user-style-profile.local.md`.
- Keep `profiles/*.local.md` out of Git.
- Do not write private style details into `SKILL.md`, `README.md`, or public reference files.
- If the user provides a profile only for this task, do not save it unless they explicitly ask.
- If both a saved profile and a session profile exist, prefer the session profile for the current task.

## Generic Style Fallback

If no profile exists, use this default:

```text
Clear, natural, equal, specific, not preachy, not padded. Preserve useful details and the author's core point. Avoid speaking for the reader, generic praise, inflated claims, and teacher-like tone.
```
