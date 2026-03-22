---
name: mark-claude-skill
description: >
  Create, structure, and write Claude SKILL.md files for the Funny not Funny
  advocacy project and Mark's personal AI workflow. Use this skill whenever Mark
  asks to "make a skill", "create a skill file", "write a skill", "build a
  skill for Claude", or wants to automate a recurring task in his Claude
  workflow. Also trigger when Mark describes a repeatable process and says
  something like "can you remember how to do this?" or "make this reusable."
  This skill produces properly formatted SKILL.md files ready for use in
  Claude's available_skills system, pre-aligned with Mark's project context,
  brand standards, and file delivery preferences.
---

# Mark's Claude Skill Creator

A meta-skill for generating new SKILL.md files inside Mark's Funny not Funny
project and personal AI workflow. Every skill produced by this guide follows
the standard Claude skill format and is tailored to Mark's tools, goals,
and delivery constraints.

---

## Who This Skill Serves

**Project:** Funny not Funny — global advocacy site (WordPress.com, Superb
Themes Non Profit theme)
**Focus areas:** Environmental justice · Animal welfare · Human rights ·
Indigenous rights
**Mark's tools:** WordPress.com · Canva · Google Drive · Google Sheets ·
TailScale · Anthropic API · Claude AI Services plugin
**Brand voice:** Professional, warm, educational — never guilt-based or alarmist
**Brand colors:** Forest Green `#1a4d2e` · Ocean Blue `#0f4c75` · Warm Orange `#f4a259`
**Typography:** Playfair Display (headings) · Work Sans (body)
**File delivery rule:** All output files must be download-ready for manual import.
Claude cannot write directly to Google Drive — always use `present_files`.

---

## When to Build a Skill vs. When Not To

**Build a skill when:**
- Mark performs the same multi-step task more than twice
- A task requires specific brand, tone, or structural rules every time
- A workflow spans multiple tools (e.g., Canva + WordPress + Google Sheets)
- Mark says "remember how to do this" or "make this repeatable"

**Don't build a skill when:**
- The task is a one-off or highly situational
- Claude can handle it cleanly with no special instructions
- The task is a single tool call with no judgement required

---

## Skill File Anatomy

Every skill is a single Markdown file with this structure:

```
---
name: skill-identifier          # kebab-case, short, descriptive
description: >
  One paragraph. Covers WHAT the skill does AND WHEN to trigger it.
  Be slightly "pushy" — list the phrases or contexts that should fire it.
  All triggering logic lives here, not in the body.
---

# Skill Title

One-sentence purpose statement.

---

## Context / Background (optional)
Background the model needs before acting.

## Step-by-Step Workflow
Numbered steps. Be explicit. Assume nothing.

## Output Rules
Format, length, file type, naming conventions, delivery method.

## Examples (optional but recommended)
Input → Output pairs that illustrate correct behavior.

## Edge Cases
What to do when input is ambiguous or incomplete.
```

---

## Step-by-Step: How to Create a Skill for Mark

### Step 1 — Understand the Request

Ask (or infer from context):

1. **What does this skill help Claude do?**
   (e.g., "write advocacy blog posts", "generate Canva post briefs", "create
   Google Sheets content calendar rows")

2. **When should it fire?**
   List 3–5 trigger phrases Mark might use naturally.

3. **What is the expected output?**
   File type · format · length · naming convention · delivery method

4. **Does it involve Mark's brand?**
   If yes, apply brand colors, typography, and voice (see Brand section below).

5. **Does it touch a specific tool?**
   WordPress · Canva · Google Sheets · Google Drive · Anthropic API

If any of the above are unclear, ask Mark before writing.

---

### Step 2 — Draft the Frontmatter

```markdown
---
name: [kebab-case-name]
description: >
  [What it does.] Use this skill when Mark asks to [trigger phrases].
  Also trigger when [secondary context]. Output is [file/format].
---
```

**Frontmatter rules:**
- `name` must be unique and kebab-case
- `description` must include both capability AND trigger signals
- Keep description under ~120 words — it's always in Claude's context window
- Use natural language Mark would actually say

---

### Step 3 — Write the Skill Body

Follow this checklist for the body:

- [ ] One-sentence purpose at the top
- [ ] Context section if domain knowledge is needed (advocacy law, WordPress
  settings, Canva workflow, etc.)
- [ ] Step-by-step workflow — numbered, explicit, no assumed knowledge
- [ ] Output rules — what to produce, what format, how to deliver
- [ ] Brand alignment section if visual/written content is produced
- [ ] At least one concrete example
- [ ] Edge cases (missing input, ambiguous request, multiple valid paths)

**Length target:** 150–400 lines. Use sub-headers liberally.
If the skill body exceeds 500 lines, split long sections into reference files
and point to them from the body.

---

### Step 4 — Apply Mark's Brand Standards (if applicable)

When the skill produces written content (blog posts, social captions, emails,
advocacy copy):

**Voice rules:**
- Professional, warm, educational
- Never guilt-based, never alarmist
- Lead with curiosity or facts, not outrage
- Use plain language — no jargon without explanation
- End pieces with a clear, empowering call to action

**Color palette (for visual briefs or Canva instructions):**

| Role      | Name         | Hex       |
|-----------|--------------|-----------|
| Primary   | Forest Green | `#1a4d2e` |
| Secondary | Ocean Blue   | `#0f4c75` |
| Accent    | Warm Orange  | `#f4a259` |

**Typography:**
- Headings: Playfair Display
- Body: Work Sans

---

### Step 5 — File Delivery

Claude cannot write directly to Google Drive. Always:

1. Save the file to `/mnt/user-data/outputs/[skill-name].md`
2. Call `present_files` with the output path
3. Tell Mark: "Download this file and place it at:
   `I:\My Drive\Projects\FunnynFunny\Claude AI\markdown file\[filename].md`"

Never attempt to write to `I:\` directly — it will fail silently.

---

### Step 6 — Test the Skill (Optional but Recommended)

After drafting, do a quick self-test:

1. Read the skill's SKILL.md as if encountering it fresh
2. Try the most common trigger prompt Mark would use
3. Verify output matches the Output Rules section
4. Check brand voice if content was generated
5. Ask Mark: "Does this match what you had in mind? Anything to adjust?"

Iterate until Mark is satisfied, then present the final file.

---

## Skill Naming Conventions for This Project

Use descriptive, project-aware names:

| Purpose                         | Suggested Name             |
|---------------------------------|----------------------------|
| Writing advocacy blog posts     | `fnf-blog-post`            |
| Canva social media briefs       | `fnf-canva-brief`          |
| WordPress page drafts           | `fnf-wp-page`              |
| Google Sheets content calendar  | `fnf-content-calendar-row` |
| Email / newsletter copy         | `fnf-newsletter`           |
| Research summaries              | `fnf-research-summary`     |
| Cause area deep-dives           | `fnf-cause-research`       |
| General Claude skill creation   | `mark-claude-skill`        |

Prefix advocacy project skills with `fnf-` so they group together.

---

## Quick-Start Templates

### Minimal Skill (simple task)

```markdown
---
name: fnf-example
description: >
  [Short capability statement.] Use when Mark asks to [trigger phrase].
  Output is [format/file type].
---

# Example Skill

[One sentence purpose.]

## Workflow

1. [Step one]
2. [Step two]
3. [Step three — deliver output]

## Output Rules

- Format: [Markdown / DOCX / plain text / etc.]
- Delivery: Save to `/mnt/user-data/outputs/[filename]` and call `present_files`
```

---

### Full Advocacy Content Skill

```markdown
---
name: fnf-[content-type]
description: >
  [Capability]. Use when Mark asks to [trigger phrases]. Also trigger for
  [secondary contexts]. Output is [format].
---

# FNF [Content Type] Skill

[One sentence.]

---

## Context

[Domain background Claude needs. Cause area specifics. Relevant laws,
organizations, or history if applicable.]

## Workflow

1. Clarify cause area if not specified (environment / animals / human rights /
   Indigenous rights)
2. [Step 2]
3. Apply brand voice: professional, warm, educational — never guilt or alarm
4. Apply brand colors and typography if visual output
5. Save to `/mnt/user-data/outputs/[filename]` and call `present_files`

## Output Rules

- Length: [target word count or line count]
- Format: [Markdown / plain text / DOCX]
- Tone: Professional, warm, educational
- CTA: End with one empowering action the reader can take

## Brand Voice Checklist

- [ ] No guilt language
- [ ] No alarmist framing
- [ ] Leads with curiosity or fact
- [ ] Plain language throughout
- [ ] Clear empowering CTA at end

## Example

**Input:** "Write a blog post about [topic]"
**Output:** [Brief description of what a correct output looks like]

## Edge Cases

- If cause area is ambiguous → ask Mark before writing
- If brand voice conflicts with urgency of topic → default to educational framing
```

---

## Common Pitfalls to Avoid

| Pitfall                                  | Fix                                                    |
|------------------------------------------|--------------------------------------------------------|
| Skill description too vague              | Add 3–5 specific trigger phrases                       |
| Skill body too long (>500 lines)         | Split into SKILL.md + reference files                  |
| No delivery instructions                 | Always end with `present_files` step                   |
| Brand voice missing from content skills  | Add voice checklist to every content skill             |
| Trying to write directly to Google Drive | Always use `/mnt/user-data/outputs/` + `present_files` |
| Skill name conflicts with existing skill | Check `/mnt/skills/` before naming                     |

---

## Reference: Mark's Project File Paths

| Location             | Path                                                         |
|----------------------|--------------------------------------------------------------|
| Skills output folder | `I:\My Drive\Projects\FunnynFunny\Claude AI\markdown file\` |
| Google Drive root    | `I:\My Drive\`                                               |
| FNF project root     | `I:\My Drive\Projects\FunnynFunny\`                          |
| WordPress admin      | `wpadmin@funnynfunny.com`                                    |
| Personal Claude acct | `iammark1900@gmail.com`                                      |

---

*This skill was created for Mark's Funny not Funny advocacy project.*
*Last structure version: March 2026.*
