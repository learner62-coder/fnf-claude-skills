---
name: fnf-advocacy-content
description: >
  Write, draft, and structure advocacy content for the Funny not Funny website
  and social channels. Use this skill when Mark asks to "write a blog post",
  "draft an article", "create advocacy content", "write a post about", "make
  content for", or "write something for Funny not Funny". Also trigger when
  Mark describes a cause area topic and wants written output — even if he
  doesn't say "advocacy content" explicitly. Covers all four cause areas:
  environmental justice, animal welfare, human rights, and Indigenous rights.
  Output is a Markdown file ready for WordPress or social use, written in
  Funny not Funny's brand voice: professional, warm, educational, never
  guilt-based or alarmist.
---

# FNF Advocacy Content Skill

Write compelling, brand-aligned advocacy content for the Funny not Funny
website and social channels across all four cause areas.

---

## Context

Funny not Funny is a global advocacy website focused on four cause areas:

- **Environmental Justice** — climate change, pollution, land/water rights,
  pipeline and extraction issues, conservation
- **Animal Welfare** — factory farming, wildlife protection, habitat loss,
  captivity, animal testing, companion animals
- **Human Rights** — civil liberties, systemic injustice, refugee and migrant
  rights, labor rights, corporate accountability
- **Indigenous Rights** — treaty rights, sovereignty, land and water
  protection, cultural preservation, FPIC (Free, Prior and Informed Consent)

These cause areas often intersect. Environmental destruction affects Indigenous
communities. Animal welfare connects to food systems and human health.
Always look for these connections and name them when relevant.

**Brand voice:** Professional, warm, educational — never guilt-based or
alarmist. Readers should feel informed and empowered, not overwhelmed or
blamed. Lead with curiosity, facts, or a compelling question. End with a
clear, achievable call to action.

**Audience:** Engaged general public — people who care but may not yet be
deeply informed. Write at a Grade 10–12 reading level. Explain acronyms and
jargon on first use.

---

## Content Types This Skill Covers

| Type               | Length         | Primary Use                        |
|--------------------|----------------|------------------------------------|
| Blog post          | 600–900 words  | WordPress website pages/posts      |
| Short article      | 300–500 words  | Website news/updates section       |
| Social caption     | 50–150 words   | Instagram, Facebook, Twitter/X     |
| Cause overview     | 400–600 words  | WordPress cause area landing pages |
| Research summary   | 300–500 words  | Internal reference or website use  |
| Email/newsletter   | 250–400 words  | Subscriber communications          |

If Mark does not specify a content type, default to **blog post**.

---

## Step-by-Step Workflow

### Step 1 — Clarify the Request

Before writing, confirm (or infer from context):

1. **Cause area** — environment / animals / human rights / Indigenous rights
   (or a combination)
2. **Content type** — blog post, article, caption, overview, summary, email
3. **Specific topic or angle** — e.g., "Line 5 pipeline", "factory farming in
   Washington State", "UNDRIP and Indigenous sovereignty"
4. **Target platform** — WordPress website, Instagram, Facebook, email
5. **Any specific facts, links, or sources Mark wants included**

If cause area or topic is missing → ask Mark before writing.
If content type is missing → default to blog post and note the assumption.

---

### Step 2 — Research Hook (if needed)

For fact-based pieces, ground the opening in a specific, verifiable fact or
statistic. If Mark has not provided one:
- Use Claude's knowledge for well-established facts
- Flag any statistics that may need verification with a note:
  `[Verify: source needed]`

Never invent statistics. If uncertain, write around the gap or flag it clearly.

---

### Step 3 — Write the Content

Follow this structure for **blog posts and articles:**

```
HEADLINE
Compelling, specific, not clickbait. Leads with the topic, not emotion.
Examples:
  "What the Line 5 Pipeline Means for Great Lakes Water Rights"
  "Why Factory Farming Is an Environmental Issue Too"
  "Understanding UNDRIP: A Plain-Language Guide"

OPENING PARAGRAPH
Hook with a fact, question, or observation. 2–3 sentences.
Do NOT open with "Did you know..." or guilt-based framing.

BODY (3–5 sections with subheadings)
- Section 1: What is happening / what is the issue
- Section 2: Why it matters / who is affected
- Section 3: The bigger picture / connections to other cause areas
- Section 4: What is being done / who is working on it
- Section 5 (optional): What the science/law/research says

CALL TO ACTION
One clear, empowering action. Examples:
  "Learn more at [organization]"
  "Sign up for updates from [campaign]"
  "Share this with someone who needs to know"
  "Contact your representative about [specific bill]"

CLOSING LINE
Warm, forward-looking. Reinforce community and possibility.
```

For **social captions:**
```
Line 1: Fact or question (the hook)
Lines 2–4: Context in plain language
Line 5: Call to action or reflection prompt
Hashtags (3–5 max): Relevant, not spammy
```

For **cause overviews (landing pages):**
```
Opening: What this cause area is and why FNF covers it
Section 1: Key issues within this cause area
Section 2: Who is affected and how
Section 3: What FNF believes and advocates for
Closing CTA: How readers can get involved
```

---

### Step 4 — Apply Brand Voice Checklist

Before finalising, verify every piece against this checklist:

- [ ] No guilt language ("You should feel ashamed", "If you don't act now...")
- [ ] No alarmist framing ("It's too late", "The world is ending")
- [ ] Opens with curiosity, fact, or question — not outrage
- [ ] Jargon explained on first use
- [ ] Written at accessible reading level (Grade 10–12)
- [ ] Connections between cause areas named where relevant
- [ ] Ends with ONE clear, achievable call to action
- [ ] Closing line is warm and forward-looking

---

### Step 5 — Format the Output

Structure the Markdown file as follows:

```markdown
# [Headline]

**Cause area:** [Environmental Justice / Animal Welfare / Human Rights /
Indigenous Rights]
**Content type:** [Blog post / Article / Caption / Overview / Summary]
**Platform:** [WordPress / Instagram / Facebook / Email]
**Word count:** [approximate]

---

[Full content here]

---

*Content created for Funny not Funny — funnynfunny.com*
```

---

### Step 6 — Deliver the File

1. Save to `/mnt/user-data/outputs/fnf-[topic-slug].md`
   Example: `fnf-line5-pipeline.md`, `fnf-factory-farming.md`
2. Call `present_files` with the output path
3. Tell Mark: "Download this file and add it to:
   `I:\My Drive\Projects\FunnynFunny\Claude AI\markdown file\`
   Or paste directly into WordPress."

---

## Brand Voice Examples

**❌ Don't write this:**
> "Every day, thousands of animals suffer in factory farms. If we don't act
> now, it will be too late. You have a responsibility to do something."

**✅ Write this instead:**
> "Modern food systems have changed dramatically in the past 50 years — and
> so has our understanding of animal cognition and welfare. Here's what the
> research tells us, and what some communities are doing differently."

---

**❌ Don't write this:**
> "Indigenous people have been ignored for centuries. Shame on governments
> that continue to violate treaty rights."

**✅ Write this instead:**
> "Treaty rights are legally binding agreements — and understanding them is
> essential to understanding land and water protection in North America.
> Here's a plain-language breakdown of what they mean and why they matter."

---

## Cause Area Quick-Reference

### Environmental Justice
Key issues: pipeline projects, water contamination, climate policy, fossil
fuel subsidies, environmental racism, rewilding, marine protection
Key organisations: Sierra Club, Earthjustice, Indigenous Environmental Network,
350.org, Center for Biological Diversity
Key laws/frameworks: Clean Water Act, Paris Agreement, NEPA, Endangered
Species Act

### Animal Welfare
Key issues: factory farming, trophy hunting, captive wildlife, animal testing,
fur trade, ocean bycatch, habitat destruction
Key organisations: Humane Society, Animal Legal Defense Fund, World Animal
Protection, Mercy for Animals, Born Free
Key laws/frameworks: Animal Welfare Act (US), Five Freedoms framework,
EU animal welfare directives

### Human Rights
Key issues: systemic racism, refugee rights, labor exploitation, corporate
accountability, freedom of expression, surveillance, access to healthcare
Key organisations: Amnesty International, Human Rights Watch, ACLU,
Global Witness, Business and Human Rights Resource Centre
Key laws/frameworks: Universal Declaration of Human Rights, International
Labour Organization conventions, UN Guiding Principles on Business and
Human Rights

### Indigenous Rights
Key issues: FPIC, treaty rights, land and water sovereignty, residential
school legacy, Missing and Murdered Indigenous Women (MMIW), cultural
revitalization, resource extraction on Indigenous lands
Key organisations: Native American Rights Fund, First Nations Information
Governance Centre, Cultural Survival, International Indian Treaty Council
Key laws/frameworks: UNDRIP (UN Declaration on the Rights of Indigenous
Peoples), 1836 Treaty of Washington, tribal sovereignty doctrine

---

## Edge Cases

- **Topic spans multiple cause areas** → cover all relevant angles, note the
  intersections explicitly in the content
- **Mark provides a research document or link** → base content on that source,
  flag any gaps
- **Topic is highly sensitive (e.g., MMIW, residential schools)** → apply
  extra care with language, center affected community voices, never
  sensationalise
- **Mark wants a social caption AND a blog post** → produce both in the same
  file, clearly labelled
- **No specific topic given** → ask Mark: "Which cause area and topic would
  you like to cover?"
- **Mark says "make it short"** → default to short article (300–500 words)
- **Mark says "make it detailed"** → default to long blog post (800–900 words)
  with all five body sections

---

*This skill was built using mark-claude-skill.md.*
*Funny not Funny — funnynfunny.com*
*Last structure version: March 2026.*
