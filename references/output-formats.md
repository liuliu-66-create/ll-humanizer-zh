# Output Formats

Choose the output format based on the user's request.

## Mode A: Inspect Only

Use when the user says:

- 检查一下
- 看看哪里有 AI 味
- 先别改全文
- 只诊断

Output:

```text
Overall judgment:

Most obvious AI tone:

Punctuation issues:
- Quotation marks:
- Rhetorical dashes:

Problem 1:
- Original:
- Type:
- Why it feels off:
- Suggested rewrite:

Problem 2:
...

Priority:
1. ...
2. ...
```

## Mode B: Inspect + Partial Rewrite

Use when the user wants concrete edits but does not ask for a full version.

Output:

```text
Overall judgment:

Main issues:

Punctuation issues to fix:
- Quotation marks:
- Rhetorical dashes:

Partial rewrites:

1. Original:
   Rewrite:
   Why:

2. Original:
   Rewrite:
   Why:

Parts I would keep:

Next step:
```

## Mode C: Full Rewrite

Use when the user says:

- 给我完整版本
- 直接改一版
- 帮我去 AI 味后的全文
- full rewrite

Output:

```text
I rewrote this by reducing quotation marks, rhetorical dashes, reader-mind-reading, correction framing, and teacher-like tone. I preserved the core point.

[Full revised version]

Main changes:
1. Removed quotation marks and rhetorical dashes from the article body.
2. Made the language more spoken and less packaged.
3. Reduced reader-mind-reading, correction framing, and teacher-like tone.
```

## Mode D: Profile Setup

Use when the user asks to save their style or make future rewrites sound like them.

Ask for:

```markdown
## Personal Style Profile

- Who I am:
- My audience:
- My writing style:
- Preserve:
- Avoid:
```

After receiving it, save it to `profiles/user-style-profile.local.md` if the environment allows file writes. If not, return the profile content and tell the user where it should be saved.

## First-time Generic Mode Note

If no profile was provided and no saved profile exists, finish with a short note:

```text
I used the generic style this time: clear, natural, equal, specific, and not preachy. If you want future rewrites to sound more like you, you can provide a personal style profile and save it locally.
```

Keep this note short. Do not force the user to configure a profile before they get value.
