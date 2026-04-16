# Installing Bonus Skills in the Vibecode Virtual Container Agent

This reference is for the moment when your **local** OpenClaw or Claude Code agent is preparing instructions for the **Vibecode virtual container agent**.

The goal is not to install `vibecode-pro` in the container.

The goal is to tell Vibecode which **helpful bonus skills** should be installed **before building**, based on the project.

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

Install with:

```bash
# From the skills repo (recommended)
git clone https://github.com/anthropics/skills.git
cp -r skills/skills/frontend-design ~/.claude/skills/
```

Add this kind of instruction to the Vibecode build brief:

> Before building, install the frontend-design skill and use it to improve hierarchy, spacing, clarity, premium UI quality, responsive polish, and visual consistency.

## 2) Cinematic site components skill

Use when:
- the user wants a cinematic landing page
- the brand needs more editorial or premium SaaS feel
- the page needs richer components or visual storytelling

Install with:

```bash
git clone https://github.com/robonuggets/cinematic-site-components.git
cd cinematic-site-components
```

If the Vibecode container needs the skill inside `~/.claude/skills`, add the copy step after cloning.

Add this kind of instruction to the Vibecode build brief:

> Before building, install the cinematic site components skill and use it for premium page sections, richer composition, visual storytelling, and high-end landing page polish.

## 3) skill-creator

This skill is often already installed by default in Claude Code environments.

Use it when:
- the project has repeatable rules
- the app will be refined across many prompts
- domain context should persist
- the same output format keeps coming up

Add this kind of instruction to the Vibecode build brief:

> Before continuing, use the skill-creator skill to create a project-specific skill for this app's recurring workflow, domain context, and output structure.

## How to pass this into the Vibecode build prompt

Add a short instruction block near the end of the build brief:

```text
Before building:
- install the frontend-design skill
- install any other required bonus skills
- create a project-specific skill if this app has repeated workflow or domain context
- then begin the build
```

## Notes

- Install only the skills that clearly help the project
- For client-facing premium work, prefer sandbox iteration after skill installation
- If a skill adds persistent value across many prompts, creating a project-specific skill is usually worth it
- `vibecode-pro` is the local helper skill, not the container skill to install
