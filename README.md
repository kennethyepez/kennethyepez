# Kenneth Yepez

**Applied AI Engineering · AI Agents · LLM Applications**

I design and build AI applications, from product requirements and architecture through integration, testing, and deployment. I use AI coding agents to write the implementation under my direction.

My work focuses on connecting models to useful workflows: voice assistants, quality assurance, evidence-backed content production, and tools that agents can operate.

## Selected projects

These projects are maintained under [M8 Apps](https://github.com/m8appz-dotcom). My role covers product definition, architecture, technical direction, integration, validation, and deployment.

| Project | What it does | Engineering focus |
| --- | --- | --- |
| [Content Engine V2](https://github.com/m8appz-dotcom/content-engine-v2) | Builds content drafts from evidence with human approval gates. | Structured outputs, evidence mapping, job state, evaluation, and auditability. |
| [JEV Contact Center QA](https://github.com/m8appz-dotcom/jev-contact-center-qa) | Scores Spanish support transcripts and routes uncertain cases to reviewers. | Redaction, resumable batches, rubric scoring, and comparison with human labels. |
| [Visual Development Toolkit](https://github.com/m8appz-dotcom/visual-development-toolkit) | Connects AI agents to visual-development and analysis tools through MCP. | Runtime adapters, reproducible tool configuration, integration checks, and upstream provenance. |
| [M8 Live Voice Assistant](https://github.com/m8appz-dotcom/m8-live-voice-assistant-public) | Connects an Expo voice client, Gemini Live, and explicit OpenClaw-backed tools. | Realtime audio, backend bridging, sessions, and browser passkey integration. |
| [Longform Video Engine](https://github.com/m8appz-dotcom/longform-video-engine) | Orchestrates voice, media, rendering, and QA from an approved script. | Input contracts, stage orchestration, provenance, and gated video output. |

Each repository documents its setup, implementation scope, and known limitations. M8 Live is a sanitized public source snapshot; its earlier development history remains private.

## How I work

- Define the problem, constraints, and acceptance criteria before implementation.
- Direct AI coding agents through scoped changes and review their output against the intended behavior.
- Use issues with acceptance criteria, focused commits, and PRs with verification and recovery evidence.
- Require CI and the configured automated reviews before merging into protected application branches.
- Check integrations and failure paths, preserve recovery points, and distinguish test fixtures from real-provider results.
- Document what was verified and what still needs validation.

A [measured JEV workflow case](https://github.com/m8appz-dotcom/jev-contact-center-qa/blob/mvp-qa/docs/CASE-STUDY.md) shows the problem, implementation responsibility, all campaign outputs, actual local timings, and the limits of an offline test.

See [engineering workflow and repository evidence](docs/ENGINEERING-WORKFLOW.md) for concrete commits, evaluation artifacts, and examples of these decisions.

## Technical areas

AI agents and tool calling · MCP integrations · TypeScript and Python applications · Realtime voice · Structured generation · Evaluation workflows · Multimodal production
