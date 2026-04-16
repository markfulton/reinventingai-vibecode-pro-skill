# Vibecode Pro Skill

<div align="center">

**A local helper skill for OpenClaw or Claude Code users building with the Vibecode App**

*Sharper build briefs. Better planning. Better results from the Vibecode App builder.*

[Get free Vibecode App credits](https://www.vibecodeapp.com/sign-up?code=ref-3ckyb6h3dwal) • [Training landing page](https://agentappbuilder.reinventing.ai/) • [Clone this repo](https://github.com/markfulton/vibecode-pro-skill)

</div>

---

## Overview

This repo is specifically for people using:
- **OpenClaw + Vibecode App CLI**
- **Claude Code + Vibecode App CLI**

The **Vibecode App** is available for **web, iOS, Android, and now CLI**.

It builds **mobile apps or web apps** using a hosted Claude Code agent running in a virtual container.

This repo gives you a **local helper skill** you install on **your own OpenClaw or Claude Code setup** so your local agent can send stronger instructions into the Vibecode App workflow.

## Important: how this skill is meant to work

This skill is designed to be used **alongside** the Vibecode App skill, not instead of it.

### Dependency

Use this with the **Vibecode App / `vibecode-cli` skill**.

What that means:
- your **local agent** uses `vibecode-pro`
- `vibecode-pro` improves the project brief and plan
- that improved brief can tell the **Vibecode App virtual container agent** which bonus skills to install before building
- the Vibecode App then builds from a stronger plan

So this skill does **not** exist to install itself inside the Vibecode App container.

It exists to make the prompts and build plans you send to the Vibecode App smarter.

## Get started with Vibecode App

If you need an account, use Mark Fulton’s referral link to sign up and **claim free credits**:

### [Claim your free Vibecode App credits here](https://www.vibecodeapp.com/sign-up?code=ref-3ckyb6h3dwal)

## Training

Want the full workflow behind this skill?

### [See the training session landing page](https://agentappbuilder.reinventing.ai/)

## What Vibecode Pro actually does

Vibecode Pro helps your local OpenClaw or Claude Code agent:
- write better project briefs for the Vibecode App
- decide when to use `yolo` vs sandbox iteration
- add bonus-skill installation instructions to the Vibecode App build brief when useful
- suggest project-specific skill creation for recurring workflows
- improve first-pass build quality for premium or business-critical apps

## Why this matters

A lot of weak Vibecode App builds come from weak prompts.

Not bad code.
Bad setup.

This skill improves the setup.

It gives your local agent better judgment about:
- what to tell the Vibecode App to build
- how to structure the build request
- when the Vibecode App container should install extra skills first
- when a project needs a reusable custom skill

## Best use cases

Use this when building:
- premium landing pages
- cinematic marketing sites
- polished SaaS frontends
- internal tools
- client apps
- micro-SaaS MVPs
- projects with reusable workflows or domain context

## Repo contents

```text
vibecode-pro/
├── SKILL.md
└── references/
    ├── brief-template.md
    └── installing-bonus-skills.md
```

## Installation

### 1) Clone this repo

```bash
git clone https://github.com/markfulton/vibecode-pro-skill.git
cd vibecode-pro-skill
```

### 2) Copy the skill into your local Claude Code skills folder

```bash
cp -r vibecode-pro ~/.claude/skills/
```

If you are using OpenClaw with Claude Code-oriented local skills, use the same folder.

## How to use it

Once installed, ask your **local** agent to use Vibecode Pro while building through the Vibecode App.

Examples:

- "Use Vibecode Pro to create a better build brief for this app before sending it to the Vibecode App."
- "Use Vibecode Pro and tell the Vibecode App to install the frontend-design skill before building."
- "Use Vibecode Pro, keep this in sandbox first, and only deploy after review."
- "Use Vibecode Pro and create a project-specific skill for this recurring workflow."

## Bonus skill support

This repo includes guidance for telling the Vibecode App virtual container agent to install helpful skills such as:
- **Anthropic frontend-design**
- **Robonuggets cinematic-site-components**
- **skill-creator** for recurring project-specific context

That means your local agent can pass along build instructions like:
- install a design skill first
- install a cinematic landing-page skill first
- create a custom skill for repeatable domain logic before continuing

## Recommended workflow

1. Install `vibecode-pro` locally
2. Make sure your local setup also has the Vibecode App / `vibecode-cli` skill available
3. Ask your local agent to write a stronger brief with Vibecode Pro
4. Let Vibecode Pro decide whether this should be `yolo` or sandbox-first
5. If useful, let Vibecode Pro add instructions telling the Vibecode App container agent which bonus skills to install before building
6. Send the improved brief to the Vibecode App

## Example outcome

Instead of a vague prompt like:

> Build me a premium SaaS landing page

Your local agent can turn it into something more useful, like:

> Build a premium SaaS landing page for founders evaluating agentic workflows. Before building, install the frontend-design skill and use it to improve hierarchy, spacing, clarity, and premium UI quality. Build in sandbox first, not yolo. Keep the layout mobile-polished and conversion-focused.

That is the difference this skill is meant to create.

## Who this helps most

This is especially useful for:
- founders who want better first-pass output
- operators building internal tools
- agencies shipping faster client work
- marketers building polished pages
- builders who want more leverage from OpenClaw + the Vibecode App

## Quick links

- [Claim free Vibecode App credits](https://www.vibecodeapp.com/sign-up?code=ref-3ckyb6h3dwal)
- [See the training landing page](https://agentappbuilder.reinventing.ai/)
- [Clone this repo](https://github.com/markfulton/vibecode-pro-skill)

## License

MIT
