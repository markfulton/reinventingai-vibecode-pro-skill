# Vibecode Pro Brief Template

Use this template when converting a user request into a stronger Vibecode App build prompt.

The **Vibecode App** is available for **web, iOS, Android, and now CLI** and is used to build **mobile apps or web apps**.

## Template

```text
Build a [web app / mobile app] called [APP NAME].

It is for [TARGET USER].

Its job is to [CORE OUTCOME].

The user should be able to:
- [CAPABILITY 1]
- [CAPABILITY 2]
- [CAPABILITY 3]
- [CAPABILITY 4 if needed]
- [CAPABILITY 5 if needed]

The interface should feel:
- [DESIGN DIRECTION]
- [BRAND / VISUAL MOOD]
- [MOBILE / RESPONSIVE EXPECTATIONS]

Important build requirements:
- [SERVER-SIDE OR SECURITY NEEDS]
- [INTEGRATIONS]
- [DATA / AUTH / STORAGE REQUIREMENTS]
- [ANY NON-NEGOTIABLE UX OR BUSINESS LOGIC]

Workflow:
- [Use yolo now] OR [build in sandbox first, do not deploy yet]

Before building:
- [install frontend-design skill if needed]
- [install cinematic-site-components if needed]
- [create a project-specific skill if needed]
```

## Good brief example

```text
Build a web app called BriefForge.

It is for marketers and founders who want better app build briefs.

Its job is to help a user turn a rough idea into a stronger project brief, build prompt, and iteration checklist.

The user should be able to:
- describe the offer and audience
- define the business goal
- choose app type and design style
- list key features and integrations
- generate a structured brief and prompt output

The interface should feel:
- premium and fast
- dark, minimal, and polished
- excellent on mobile and desktop

Important build requirements:
- provider secrets stay server-side
- OpenRouter calls must run through a backend route
- fall back gracefully if provider key is missing
- output should be especially useful for OpenClaw or Claude Code workflows

Workflow:
- build in sandbox first, do not deploy yet

Before building:
- install frontend-design skill
```

## Guidance

Keep the prompt specific about the product and user value.

Do not bloat it with:
- file-by-file instructions
- framework micromanagement
- CSS micromanagement
- component implementation trivia

The goal is a sharper product brief, not a hand-written spec for every line of code.
