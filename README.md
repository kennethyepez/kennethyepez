# Kenneth Yepez

**Applied AI Engineering · AI Agents · LLM Applications**

I turn product requirements into AI workflows and direct coding agents through implementation, integration and validation. I use AI to write the code under my direction. My work covers the problem, architecture, delivery constraints and decisions about what the evidence establishes.

## Selected projects

| Project | What to inspect | Evidence |
| --- | --- | --- |
| [Fish Free MCP](https://github.com/kennethyepez/fish-free-mcp) | Passkey-protected Gemini integration, scoped OAuth, idempotent speech jobs and private audio delivery. | [Architecture](https://github.com/kennethyepez/fish-free-mcp/blob/main/docs/ARCHITECTURE.md), [21-test CI](https://github.com/kennethyepez/fish-free-mcp/actions/runs/45053439926) and [desktop/mobile screenshots](https://github.com/kennethyepez/fish-free-mcp#screenshots). |
| [Content Engine V2](https://github.com/m8appz-dotcom/content-engine-v2) | Evidence-backed scripts, revision-bound approval and native storyboard planning. | [Case](https://github.com/m8appz-dotcom/content-engine-v2/blob/main/docs/CASE-STUDY.md): actual offline artifacts, current screens and workspace recording. |
| [M8 Live Voice Assistant](https://github.com/m8appz-dotcom/m8-live-voice-assistant-public) | Expo and a private ASR → streaming LLM → English speech relay. | [Case](https://github.com/m8appz-dotcom/m8-live-voice-assistant-public/blob/main/docs/CASE-STUDY.md): original service audio, development measurements and remaining acceptance. |

The content and voice-assistant cases are maintained under [M8 Apps](https://github.com/m8appz-dotcom). The voice assistant's default pathway uses private inference; Gemini is an explicit legacy rollback option.

## Supporting work

- [JEV Contact Center QA](https://github.com/m8appz-dotcom/jev-contact-center-qa): redaction, rubric scoring and reviewer workflows. Its small synthetic evaluation exposes weak failure recall; the next evaluation needs independent labels.
- [Visual Development Toolkit](https://github.com/m8appz-dotcom/visual-development-toolkit): portable MCP workflows, original-byte verification and tool provenance. Integrated engines retain upstream authorship.
- [Longform Video Engine](https://github.com/m8appz-dotcom/longform-video-engine): script contracts and staged production. Its connected preview is a silent excerpt; a finished narrated film needs separate acceptance.

## Decisions I can explain

- Why evidence references, editorial truth and approval require separate checks.
- Why the relay streams complete phrases and keeps account tools outside audio transport.
- How to validate a migration in an isolated copy while preserving services, data and rollback.
- How to distinguish authored examples, automated checks, service captures and physical user acceptance.

The cases connect those decisions to source, outputs and limitations. They do not imply customer adoption, independent human review or a multi-person team.

## Delivery

Real issue → focused commits → PR → relevant checks and identified automated review → protected integration. Recovery history stays intact. Dependency migrations, shared infrastructure and product changes should remain independently reviewable.

See [workflow and repository evidence](docs/ENGINEERING-WORKFLOW.md). I welcome a technical discussion of a failure, a tradeoff and the test that changed the implementation.
