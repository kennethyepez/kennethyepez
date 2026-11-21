# Engineering workflow and evidence

I direct product definition, architecture, integration, validation, and delivery. AI coding agents write the implementation under my direction. Automated code and security reviews are identified as AI reviews; they are not human approvals.

## From a problem to a reviewed delivery

1. Record a real problem, acceptance criteria, and verification plan in an issue.
2. Inspect the repository and runtime, preserve recovery points, and work in an isolated branch.
3. Separate changes by purpose: format normalization, workflow documentation, validation, and behavior fixes.
4. Open a PR linked to the issue, with tests, limitations, and a recovery path.
5. Address review feedback and wait for product CI, source-format checks, and the configured AI reviews on the current revision.
6. Merge through the protected default branch, verify the published result, and close the issue with evidence.

The five application repositories require PRs, successful status checks, and resolved review conversations. Their active rules prevent force pushes and default-branch deletion. No human approval requirement is configured because there is no additional authorized human reviewer in these examples. A future human review must be attributed to the person who actually performs it.

## Current delivery examples

These are real changes to the delivery process, not an imported backlog or empty activity. Each PR preserves separate format, workflow, CI, and review-fix commits. Product checks and the configured automated reviews completed before integration.

| Repository | Problem and reviewed change | Product CI for the reviewed revision |
| --- | --- | --- |
| Content Engine V2 | [Issue #2](https://github.com/m8appz-dotcom/content-engine-v2/issues/2) → [PR #3](https://github.com/m8appz-dotcom/content-engine-v2/pull/3) | [Type checks, tests, renderer, migrations, evaluation, build and dependency audit](https://github.com/m8appz-dotcom/content-engine-v2/actions/runs/44931082337) |
| JEV Contact Center QA | [Issue #1](https://github.com/m8appz-dotcom/jev-contact-center-qa/issues/1) → [PR #2](https://github.com/m8appz-dotcom/jev-contact-center-qa/pull/2) | [Offline suite and report generation on Windows/Linux, Python 3.12/3.13](https://github.com/m8appz-dotcom/jev-contact-center-qa/actions/runs/44931086158) |
| Visual Development Toolkit | [Issue #1](https://github.com/m8appz-dotcom/visual-development-toolkit/issues/1) → [PR #2](https://github.com/m8appz-dotcom/visual-development-toolkit/pull/2) | [Actual stdio MCP regressions and packaging on Windows/Linux](https://github.com/m8appz-dotcom/visual-development-toolkit/actions/runs/44931094232) |
| M8 Live Voice Assistant | [Issue #1](https://github.com/m8appz-dotcom/m8-live-voice-assistant-public/issues/1) → [PR #2](https://github.com/m8appz-dotcom/m8-live-voice-assistant-public/pull/2) | [Type checks, audio/bridge regressions and Expo web export](https://github.com/m8appz-dotcom/m8-live-voice-assistant-public/actions/runs/44931102227) |
| Longform Video Engine | [Issue #1](https://github.com/m8appz-dotcom/longform-video-engine/issues/1) → [PR #2](https://github.com/m8appz-dotcom/longform-video-engine/pull/2) | [Distribution, startup, offline suite, renderer types and walkthrough](https://github.com/m8appz-dotcom/longform-video-engine/actions/runs/44931109844) |

In JEV and Longform, the AI reviewer found that changing a PR's target branch would not reevaluate the new review gate. The correction was applied across all five repositories, with regression checks for retargeting an unchanged revision and refusing non-default targets. The discussion and resolution remain visible in the PRs.

The initial policy PRs installed the gate and were checked before merge. Later default-branch changes must satisfy the installed gate as a required status. The [JEV campaign change](https://github.com/m8appz-dotcom/jev-contact-center-qa/pull/4) uses that workflow for a functional improvement.

## A measured, controlled case

The [JEV campaign reporting case](https://github.com/m8appz-dotcom/jev-contact-center-qa/blob/mvp-qa/docs/CASE-STUDY.md) explains a concrete gap: the earlier example generated three campaigns but exposed only one report. The change exposes all three, keeps the previous entry point compatible, and measures five actual local CLI runs.

The case includes the problem, acceptance, my responsibility, generated outputs, input identity, observed timings, regression checks, and limitations. It uses authored sample conversations and FakeJev. It is an offline workflow measurement, not evidence of model accuracy, customer adoption, production throughput, or business savings.

The separate [model evaluation](https://github.com/m8appz-dotcom/jev-contact-center-qa/blob/mvp-qa/data/eval/informe.md) remains visible, including weak failure recall in some rubric items. High overall agreement does not erase those limitations.

## What the evidence establishes

- Product tests and integration checks establish the behavior they exercise. Offline examples do not establish live-provider quality.
- CI links identify a particular revision and run; a stored file named latest.json does not automatically describe the current revision.
- The Toolkit's [third-party record](https://github.com/m8appz-dotcom/visual-development-toolkit/blob/main/THIRD_PARTY.md) separates integration work from upstream engines.
- M8 Live is a sanitized public source snapshot. Earlier development history remains private; a web export does not establish a completed authenticator or live-voice session.
- Longform's offline contract and rendering checks do not establish the quality of a finished audiovisual production.
- These examples show an individual directing AI-assisted delivery. They do not claim a multi-person engineering team or a history of independent human code review.

## Identity, history, and recovery

New work uses verified contributor identities and current timestamps. Historical aliases and imported snapshots retain their original attribution; neither author history nor dates are rewritten to improve the contribution calendar.

Recovery branches and original parent history remain intact. A mistake is corrected through a reviewed follow-up or revert. Push counts, stars, and contribution-calendar color are not quality metrics.

Each repository's CONTRIBUTING.md and docs/DELIVERY.md describe its issue, commit, validation, review, and recovery conventions. Future maintenance should follow the same process for genuine problems; this documentation does not schedule artificial activity.
