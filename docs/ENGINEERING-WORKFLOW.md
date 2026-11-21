# Engineering workflow and evidence

This portfolio brings together projects directed by Kenneth Yepez and implemented with AI coding agents. Kenneth's responsibilities cover product requirements, architecture, technical direction, integration, testing, and deployment.

## From requirements to a traceable change

1. Define the behavior, constraints, and acceptance criteria.
2. Inspect the current repository, dependencies, and relevant runtime before changing implementation.
3. Scope a change around one problem and direct the coding agent with that context.
4. Review the result and verify the behavior with the checks appropriate to that change.
5. Commit a coherent change with a descriptive message, publish it, and verify the remote result.
6. Keep recovery history and document remaining limitations.

Documentation checks establish the published text, links, and change scope. Functional tests, provider evaluations, and deployment checks establish different properties and are reported separately.

## Recent commit organization

The portfolio documentation update used one focused commit per application repository. It changed seven Markdown files across five repositories, preserving the Spanish operating guides where applicable.

| Repository | Published change |
| --- | --- |
| [Content Engine V2](https://github.com/m8appz-dotcom/content-engine-v2/commit/7f098b2dfd4e50eb7c0281e83892358007dd2d52) | Architecture, review entry points, and the scope of recorded evaluation results. |
| [JEV Contact Center QA](https://github.com/m8appz-dotcom/jev-contact-center-qa/commit/59aae2d041d468f41ed42bdefe8f4163e853519b) | English project presentation with the original Spanish guide preserved. |
| [Visual Development Toolkit](https://github.com/m8appz-dotcom/visual-development-toolkit/commit/500683715263d01838e9003ed60ff0fee777626f) | MCP/runtime architecture, integration review paths, and upstream provenance. |
| [M8 Live Voice Assistant](https://github.com/m8appz-dotcom/m8-live-voice-assistant-public/commit/86edd14882dac7c7ad9fa9eb48a26d55c43e422b) | Client/bridge map, local build instructions, and implementation boundaries. |
| [Longform Video Engine](https://github.com/m8appz-dotcom/longform-video-engine/commit/67a243faaddf9cd9ca88b4bf9feb624df6476f8e) | English entry point and a correction explaining the artifacts required before the props stage. |

These commits preserve their parent history. The application code and recovery branches were unchanged by that documentation update. The update was verified against the remote file contents and complete repository trees.

## Evaluation and verification examples

### Content Engine V2: distinguish current CI from a stored report

The documentation commit has a [successful CI run](https://github.com/m8appz-dotcom/content-engine-v2/actions/runs/44856233770). The workflow includes type checks, tests, database/source-registry smoke checks, evaluation, build, and dependency audit in an isolated environment.

The committed [evaluation report](https://github.com/m8appz-dotcom/content-engine-v2/blob/7f098b2dfd4e50eb7c0281e83892358007dd2d52/evals/reports/latest.json) describes an earlier run. A file named `latest.json` is not automatically evidence for the current revision.

### JEV Contact Center QA: inspect failure recall

The [recorded evaluation](https://github.com/m8appz-dotcom/jev-contact-center-qa/blob/59aae2d041d468f41ed42bdefe8f4163e853519b/data/eval/informe.md) used 40 authored synthetic conversations with one annotator. It detected one of four identity-verification failures and none of two diagnosis failures.

Those counts expose limitations that high overall agreement can hide. A customer pilot and threshold calibration require their own evidence.

### Visual Development Toolkit: separate integration work from upstream engines

The [third-party record](https://github.com/m8appz-dotcom/visual-development-toolkit/blob/500683715263d01838e9003ed60ff0fee777626f/THIRD_PARTY.md) and pinned tool manifests identify the integrated upstream components. The project contribution is the integration layer, adapters, launchers, configuration, and workflows.

### M8 Live: publish source while preserving private history

The [public repository](https://github.com/m8appz-dotcom/m8-live-voice-assistant-public) contains fresh source snapshots on its primary and recovery branches. Generated bundles and earlier private history were excluded. Source publication does not establish latency, reconnect behavior, or a completed authenticator test; those need end-to-end validation.

### Longform Video Engine: respect stage dependencies

The [stage orchestrator](https://github.com/m8appz-dotcom/longform-video-engine/blob/67a243faaddf9cd9ca88b4bf9feb624df6476f8e/engine/longform_pipeline.py) expects earlier-stage artifacts when building props. The English guide makes that dependency explicit instead of suggesting that a new contract alone is sufficient.

Mock runs, actual provider calls, and reviewed audiovisual output serve different verification purposes. Performance and production-quality claims require a recorded run.

## Commit and delivery conventions

- Keep each commit tied to one purpose; separate documentation from functional changes.
- Use messages that identify the area and result, such as `docs(profile)` and `docs(workflow)` for this profile repository.
- Preserve history and recovery refs instead of rewriting them to improve appearances.
- Check the published commit and affected paths after a push or API-based update.
- Link conclusions to the revision, evaluation artifact, or CI run that supports them.
