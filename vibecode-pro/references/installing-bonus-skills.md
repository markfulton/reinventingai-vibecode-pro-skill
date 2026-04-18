# Installing Bonus Skills in the Vibecode App Virtual Container Agent

This reference is for the moment when your **local** OpenClaw or Claude Code agent is preparing instructions for the **Vibecode App virtual container agent**.

The goal is not to install `vibecode-pro` in the container.

The goal is to tell the Vibecode App which **helpful bonus skills or reference repos** should be set up **before building**, based on the project.

## Always review this file first

Before telling the Vibecode App agent to install any bonus skills, review this file and reuse the exact commands from here.

Do **not** tell the build agent only:
- install landing-page-generator
- install ai-seo
- install frontend-design

That is too vague.

Instead, give the build agent the **exact shell commands** to run in a fenced `bash` block, then tell it how to use what was installed or cloned.

## When to add bonus-skill instructions

Add these instructions when the project needs:
- premium UI polish
- stronger landing page structure
- SEO-aware content or programmatic SEO strategy
- better copy and messaging
- a more deliberate design system
- reusable operating rules across multiple prompts

## Recommended 7-skill marketing and design bundle

Start with these 7 skill folders from the public repo:
- Repo: `https://github.com/alirezarezvani/claude-skills`
- Skill folders:
  1. `product-team/landing-page-generator`
  2. `product-team/ui-design-system`
  3. `marketing-skill/ai-seo`
  4. `marketing-skill/seo-audit`
  5. `marketing-skill/programmatic-seo`
  6. `marketing-skill/copywriting`
  7. `marketing-skill/marketing-psychology`

These are strong early additions for Vibecode App builds involving landing pages, SaaS marketing sites, content-heavy apps, and conversion-sensitive flows.

## 1) Exact install block for those 7 skills

Use this exact setup block in the Vibecode App brief when those skills are relevant:

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/alirezarezvani/claude-skills.git /tmp/alirezarezvani-claude-skills
cp -r /tmp/alirezarezvani-claude-skills/product-team/landing-page-generator ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/product-team/ui-design-system ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/marketing-skill/ai-seo ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/marketing-skill/seo-audit ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/marketing-skill/programmatic-seo ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/marketing-skill/copywriting ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/marketing-skill/marketing-psychology ~/.claude/skills/
```

Then add instructions like:

> After running the commands above, use only the skills that materially help this build. Prioritize `landing-page-generator`, `ui-design-system`, `copywriting`, and `marketing-psychology` for premium landing pages or conversion-sensitive marketing sites. Add `ai-seo`, `seo-audit`, and `programmatic-seo` when the app or page needs stronger search visibility, structured content planning, or SEO-aware architecture.

## 2) What each of the 7 skills is best for

### `landing-page-generator`
Use when:
- the app needs a stronger landing page
- the user wants more conversion structure
- the first pass needs better sections, hierarchy, CTA flow, and messaging layout

### `ui-design-system`
Use when:
- the project needs more visual consistency
- the app should feel more premium and systemized
- spacing, typography, color decisions, and component consistency matter

### `ai-seo`
Use when:
- the page or app should be more citeable in AI search tools
- the user cares about ChatGPT, Perplexity, Google AI Overviews, or GEO-style visibility

### `seo-audit`
Use when:
- the project needs a more traditional SEO pass
- the landing page, blog, or content hub should be easier to optimize structurally

### `programmatic-seo`
Use when:
- the build includes scale content pages
- the app should support content expansion, topic clusters, location pages, or repeatable SEO page generation

### `copywriting`
Use when:
- the page needs stronger headlines and body copy
- the app needs clearer value communication
- the first pass feels generic, flat, or under-convincing

### `marketing-psychology`
Use when:
- the project is conversion-sensitive
- the app needs stronger framing, trust, positioning, objection handling, or CTA logic

## 3) Copy-paste example prompt block for the Vibecode App brief

````text
Before building, run these setup commands:

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/alirezarezvani/claude-skills.git /tmp/alirezarezvani-claude-skills
cp -r /tmp/alirezarezvani-claude-skills/product-team/landing-page-generator ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/product-team/ui-design-system ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/marketing-skill/copywriting ~/.claude/skills/
cp -r /tmp/alirezarezvani-claude-skills/marketing-skill/marketing-psychology ~/.claude/skills/
```

Then:
- use `landing-page-generator` to improve page composition, sections, CTA flow, and conversion structure
- use `ui-design-system` to improve consistency, spacing, typography, and premium UI quality
- use `copywriting` and `marketing-psychology` to sharpen headlines, value communication, trust, and call-to-action logic
- build in sandbox first, not yolo
````

## 4) Claude Code frontend-design skill

Use when:
- the user wants a more polished frontend
- the app needs stronger hierarchy and spacing
- the first pass needs to feel more premium

Use this exact setup block in the Vibecode App brief:

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/anthropics/skills.git /tmp/anthropic-skills
cp -r /tmp/anthropic-skills/skills/frontend-design ~/.claude/skills/
```

Then add this instruction below the commands:

> After running the commands above, use the `frontend-design` skill to improve hierarchy, spacing, clarity, premium UI quality, responsive polish, and visual consistency.

## 5) Cinematic site components

Use when:
- the user wants a cinematic landing page
- the brand needs more editorial or premium SaaS feel
- the page needs richer components or visual storytelling

Important: the public `robonuggets/cinematic-site-components` repo is best treated as a **reference repo / component library** unless you know a packaged Claude skill folder is present in the environment.

Use this exact setup block in the Vibecode App brief:

```bash
git clone https://github.com/robonuggets/cinematic-site-components.git /tmp/cinematic-site-components
```

Then add this instruction below the commands:

> After cloning the repo above, use `/tmp/cinematic-site-components` as a reference library for premium landing page sections, richer composition, motion ideas, visual storytelling, and high-end SaaS/editorial polish.

If the environment already contains a packaged `cinematic-site-components` skill folder, you may instead add:

```bash
mkdir -p ~/.claude/skills
cp -r /path/to/cinematic-site-components ~/.claude/skills/
```

and then explicitly tell the agent to use that installed skill.

## 6) skill-creator

This skill is often already installed by default in Claude Code environments.

Use it when:
- the project has repeatable rules
- the app will be refined across many prompts
- domain context should persist
- the same output format keeps coming up

Add this instruction to the Vibecode App brief:

> If `skill-creator` is available in the environment, use it to create a project-specific skill for this app's recurring workflow, domain context, and output structure before continuing.

## Notes

- Install or clone only the assets that clearly help the project
- For client-facing premium work, prefer sandbox iteration after setup
- If a skill adds persistent value across many prompts, creating a project-specific skill is usually worth it
- `vibecode-pro` is the local helper skill, not the container skill to install
