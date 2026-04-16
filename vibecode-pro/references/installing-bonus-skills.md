# Installing Bonus Skills in the Vibecode App Virtual Container Agent

This reference is for the moment when your **local** OpenClaw or Claude Code agent is preparing instructions for the **Vibecode App virtual container agent**.

The goal is not to install `vibecode-pro` in the container.

The goal is to tell the Vibecode App which **helpful bonus skills or reference repos** should be set up **before building**, based on the project.

## Core rule

Do **not** tell the Vibecode App agent only:
- install frontend-design
- install cinematic-site-components

That is incomplete.

Instead, give the build agent the **exact shell commands** to run, in a fenced `bash` block, and then tell it how to use the installed skill or cloned reference repo.

## When to add bonus-skill instructions

Add these instructions when the project needs:
- premium UI polish
- better landing page composition
- repeatable domain-specific context
- richer design systems
- reusable operating rules across multiple prompts

## 1) Claude Code frontend-design skill

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

## 2) Cinematic site components

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

## 3) skill-creator

This skill is often already installed by default in Claude Code environments.

Use it when:
- the project has repeatable rules
- the app will be refined across many prompts
- domain context should persist
- the same output format keeps coming up

Add this instruction to the Vibecode App brief:

> If `skill-creator` is available in the environment, use it to create a project-specific skill for this app's recurring workflow, domain context, and output structure before continuing.

## Copy-paste example block for the Vibecode App brief

````text
Before building, run these setup commands:

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/anthropics/skills.git /tmp/anthropic-skills
cp -r /tmp/anthropic-skills/skills/frontend-design ~/.claude/skills/
git clone https://github.com/robonuggets/cinematic-site-components.git /tmp/cinematic-site-components
```

Then:
- use the `frontend-design` skill for hierarchy, spacing, clarity, and premium UI polish
- use `/tmp/cinematic-site-components` as a reference library for cinematic sections, richer composition, and premium visual storytelling
- build in sandbox first, not yolo
````

## Notes

- Install or clone only the assets that clearly help the project
- For client-facing premium work, prefer sandbox iteration after setup
- If a skill adds persistent value across many prompts, creating a project-specific skill is usually worth it
- `vibecode-pro` is the local helper skill, not the container skill to install
