---
name: vibecode-pro
description: "A local helper skill for OpenClaw or Claude Code users who build with Vibecode. Use it alongside the `vibecode-cli` skill to improve the project brief, choose between `yolo` and sandbox iteration, and add instructions telling the Vibecode virtual container agent which bonus skills to install before building. Best for premium landing pages, SaaS apps, internal tools, client apps, and any build that benefits from better planning, stronger frontend polish, or reusable project context."
---

# Vibecode Pro

This is a **local helper skill**.

Use it on your own OpenClaw or Claude Code installation when you are building through Vibecode.

## Dependency

This skill is meant to work **with** the `vibecode-cli` skill.

- `vibecode-cli` handles the actual Vibecode build workflow
- `vibecode-pro` improves the brief, planning, and pre-build instructions you send into that workflow

Do not treat this skill as a replacement for the Vibecode app skill.

## Core idea

The purpose of this skill is to help your **local agent** send better instructions to the **Vibecode virtual container agent**.

That means this skill should:
1. improve the build brief
2. choose the right build mode
3. include bonus-skill installation instructions only when useful
4. suggest project-specific skill creation when repetition justifies it

It should **not** try to install itself inside the Vibecode container.

## What this skill does

1. Turns rough requests into a cleaner Vibecode-compatible brief
2. Chooses between `yolo` and sandbox iteration
3. Adds instructions for bonus skill installation when useful
4. Suggests project-specific skill creation when the build has repeatable patterns

## Default workflow

### 1) Build the brief first

Before building, turn the request into a short product-manager-style brief with:
- app name
- target user
- core problem
- 3 to 5 key capabilities
- design direction
- integrations or backend needs
- deploy now vs iterate first

Do **not** over-specify frameworks, file paths, or implementation trivia unless the user explicitly wants that level of control.

## 2) Choose the right Vibecode path

### Use `yolo` when:
- the user wants speed
- the app is straightforward
- a first pass is enough
- immediate deployment is part of the goal

### Use sandbox iteration when:
- the build is design-sensitive
- the app needs premium polish
- there are API/security requirements
- the user wants review before deploy
- the build includes bonus skill setup

If uncertain, prefer sandbox iteration for premium or client-facing work.

## 3) Add bonus-skill instructions when needed

If the build needs stronger visual polish or reusable operating context, tell the Vibecode virtual container agent to install the right skill before building.

Read `references/installing-bonus-skills.md` when:
- the user wants premium frontend design
- the user wants cinematic or editorial landing page polish
- the project would benefit from a custom ongoing skill

## 4) Create a project-specific skill when repetition is likely

If the same domain rules, workflows, or output format will matter across multiple prompts, instruct the build process to create a project-specific skill.

Good triggers:
- repeated industry-specific constraints
- repeated output structure
- repeated brand/design system guidance
- repeated workflow rules
- repeated API or integration handling patterns

Use the already-installed `skill-creator` skill for that step when available in the Claude Code environment.

## Brief pattern to send into Vibecode

Use this structure when drafting the prompt for the build agent:

- what the app is
- who it is for
- what users can do
- what the UI should feel like
- what must be secure or server-side
- whether to deploy immediately or stay in sandbox
- which bonus skills to install first, if any

Read `references/brief-template.md` for a reusable template.

## Important Vibecode notes

- Prefer server-side routes for private API keys
- Put secrets in backend environment, not frontend env
- Verify generated provider model choices, especially for OpenRouter
- Share the live URL quickly after success
- For premium work, review before deploy

## Example instructions to include in a build prompt

### Premium landing page build

> Before building, install the frontend-design skill and use it to improve hierarchy, spacing, clarity, and premium UI quality. Then build this in sandbox first, not yolo.

### Cinematic marketing page

> Before building, install the cinematic site components skill and use it for premium landing page sections, motion ideas, and richer page composition. Build in sandbox first and refine before deploy.

### Project-specific repeatable workflow

> Before continuing, use the skill-creator skill to create a small project-specific skill for this app's recurring workflow and domain context. Then continue building with that skill available.

## Outcome target

A good Vibecode Pro build should produce:
- a clearer first pass
- fewer vague outputs
- stronger UI quality
- better security instructions
- smarter deployment decisions
- better reuse across future prompts
