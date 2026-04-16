# 🚀 Vibecode Pro Skill

> **A Reinventing.AI helper skill for Vibecode CLI users who want stronger results from the Vibecode app builder.**

## ⚠️ Important: who this is for

This repo is specifically for people using:
- **OpenClaw + Vibecode CLI**, or
- **Claude Code + Vibecode CLI**

This is a **local helper skill** you install on **your own OpenClaw or Claude Code setup**.

It works **with** the Vibecode app skill, not instead of it.

### Dependency

This skill is designed to be used alongside the **Vibecode app / `vibecode-cli` skill**.

What it does is simple:
- your **local agent** uses `vibecode-pro`
- `vibecode-pro` helps your local agent craft a better Vibecode-compatible brief
- that brief can include instructions for the **Vibecode virtual container agent** to install useful bonus skills **before building**
- Vibecode then builds from a stronger plan

So this skill does **not** exist to install itself inside the Vibecode container.

It exists to make the prompts and build plans you send to Vibecode smarter.

## 🎁 New to Vibecode?

Use Mark Fulton’s referral link to sign up and **get free credits**:

### 👉 [Get started with Vibecode and claim free credits](https://www.vibecodeapp.com/sign-up?code=ref-3ckyb6h3dwal)

## 🎓 Training session

Want the full workflow behind this?

### 👉 [See the training session landing page](https://agentappbuilder.reinventing.ai/)

---

## ✨ What Vibecode Pro actually does

Vibecode Pro helps your local OpenClaw or Claude Code agent:
- write better project briefs for Vibecode
- decide when to use `yolo` vs sandbox iteration
- add bonus-skill installation instructions to the Vibecode build brief when useful
- suggest project-specific skill creation for recurring workflows
- improve first-pass build quality for premium or business-critical apps

## 🧠 Why this matters

A lot of weak Vibecode builds come from weak prompts.

Not bad code.
Bad setup.

This skill improves the setup.

It gives your local agent better judgment about:
- what to tell Vibecode to build
- how to structure the build request
- when the Vibecode container should install extra skills first
- when a project needs a reusable custom skill

## ✅ Best use cases

Use this when building:
- premium landing pages
- cinematic marketing sites
- polished SaaS frontends
- internal tools
- client apps
- micro-SaaS MVPs
- projects with reusable workflows or domain context

## 📦 Repo contents

```text
vibecode-pro/
├── SKILL.md
└── references/
    ├── brief-template.md
    └── installing-bonus-skills.md
```

## 🔧 Installation

### 1) Clone this repo

```bash
git clone https://github.com/markfulton/reinventingai-vibecode-pro-skill.git
cd reinventingai-vibecode-pro-skill
```

### 2) Copy the skill into your local Claude Code skills folder

```bash
cp -r vibecode-pro ~/.claude/skills/
```

If you are using OpenClaw with Claude Code-oriented local skills, use the same folder.

## 🪄 How to use it

Once installed, ask your **local** agent to use Vibecode Pro while building through Vibecode.

Examples:

- "Use Vibecode Pro to create a better build brief for this app before sending it to Vibecode."
- "Use Vibecode Pro and tell Vibecode to install the frontend-design skill before building."
- "Use Vibecode Pro, keep this in sandbox first, and only deploy after review."
- "Use Vibecode Pro and create a project-specific skill for this recurring workflow."

## 🔌 Bonus skill support

This repo includes guidance for telling the Vibecode virtual container agent to install helpful skills such as:
- **Anthropic frontend-design**
- **Robonuggets cinematic-site-components**
- **skill-creator** for recurring project-specific context

That means your local agent can pass along build instructions like:
- install a design skill first
- install a cinematic landing-page skill first
- create a custom skill for repeatable domain logic before continuing

## 🧭 Recommended workflow

1. Install `vibecode-pro` locally
2. Make sure your local setup also has the Vibecode app / `vibecode-cli` skill available
3. Ask your local agent to write a stronger brief with Vibecode Pro
4. Let Vibecode Pro decide whether this should be `yolo` or sandbox-first
5. If useful, let Vibecode Pro add instructions telling the Vibecode container agent which bonus skills to install before building
6. Send the improved brief to Vibecode

## 🏗️ Example outcome

Instead of a vague prompt like:

> Build me a premium SaaS landing page

Your local agent can turn it into something more useful, like:

> Build a premium SaaS landing page for founders evaluating agentic workflows. Before building, install the frontend-design skill and use it to improve hierarchy, spacing, clarity, and premium UI quality. Build in sandbox first, not yolo. Keep the layout mobile-polished and conversion-focused.

That is the difference this skill is meant to create.

## 👥 Who this helps most

This is especially useful for:
- founders who want better first-pass output
- operators building internal tools
- agencies shipping faster client work
- marketers building polished pages
- builders who want more leverage from OpenClaw + Vibecode

## 🔗 Quick links

- [Get free Vibecode credits with the referral link](https://www.vibecodeapp.com/sign-up?code=ref-3ckyb6h3dwal)
- [See the Reinventing.AI training landing page](https://agentappbuilder.reinventing.ai/)
- [Clone this repo](https://github.com/markfulton/reinventingai-vibecode-pro-skill)

## 📄 License

MIT
