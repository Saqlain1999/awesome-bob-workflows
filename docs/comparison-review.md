# Workflow overlap review

Reviewed **10 October 2026**. This is a focused comparison of nearby public projects, not an exhaustive survey or a claim of uniqueness. Primary documentation, representative code, file trees, licenses, and selected release metadata were inspected. No upstream project was installed, no model was called, and no runtime or deployment was tested by this catalogue.

All entries remain `documentation-reviewed` with empty `runtime_evidence`. Upstream reports can be useful without becoming independent catalogue validation. The [metadata](../catalog/projects.json) records exact supporting URLs and the [README](../README.md) provides the browsing view.

## Choose by responsibility

| Need | Existing starting point | Boundary to check |
| --- | --- | --- |
| Continue a Bob session or manage its context | [Native Shell commands](https://bob.ibm.com/docs/shell/features/slash-commands), [context management](https://bob.ibm.com/docs/ide/core-concepts/context-window-management), [IDE rollback](https://bob.ibm.com/docs/ide/features/rollback) | Restored history is not proof that earlier facts or tests remain current. |
| Specifications or a scoped assess/fix/test process | [Spec Kit](https://github.com/github/spec-kit) | Its existing artifacts and skill names should remain authoritative when used. |
| Reusable repository context for Spec Kit | [Verified Codebase Context](https://github.com/philo-x/spec-kit-preset-codebase-memory-context) | Four core-command replacements target Spec Kit 1.1.2; Bob is absent from the listed test matrix. |
| A shared board and agent dispatch | [Bob Control](https://github.com/PounceAI/bob-control) | Review board paths, approval policy, verification configuration and client-specific adapters. |
| A service API around Bob | [Headless Bob](https://github.com/ibm-self-serve-assets/building-blocks/tree/main/ai/engineering/headless-bob/assets/headlessbob) | It is an application to operate, with a trusted-operator model; it is not an OS sandbox. |
| Domain skills and integration assets | [Bob+ Building Blocks](https://github.com/ibm-self-serve-assets/building-blocks) | Select assets individually; review MCP changes and license notices. |
| Instruction and orchestration examples | [IBM workshop](https://github.com/IBM/intro-bob-workshop), [IBM demos](https://github.com/IBM/bob-demo) | Examples carry version assumptions; current product documentation remains the feature reference. |
| Convert third-party skill sources | [bob-skill-installer](https://github.com/funhere/bob-skill-installer) | Inspect conversion output, source-file inclusion and actual backup behavior. |

These projects already cover many commonly proposed additions: context files, evidence-qualified claims, per-task reports, installation manifests, checkpoints, queues and subprocess loops. A small workflow kit can still help through good defaults, simple adoption, coexistence and reproducible behavior reports. Those are contributions to demonstrate, not unique mechanisms established by this review.

When tools overlap, name one owner for each artifact. A lightweight checkpoint can link to Spec Kit's assessment/test reports, a Beads issue or a shared board task. An existing repository profile can supply context, with critical facts rechecked against current source. Maintaining two independent authoritative records creates avoidable drift.

## Versioned source ledger

The following revisions identify the code inspected. A main-branch snapshot is not automatically a release or a supported version. License labels concern the indicated source; dependency and asset notices still apply.

| Project | Reviewed revision | Representative primary sources | License scope |
| --- | --- | --- | --- |
| Spec Kit | `0443760542e7e5269724744a2ac55c4bd386d095` | [Bob adapter](https://github.com/github/spec-kit/blob/0443760542e7e5269724744a2ac55c4bd386d095/src/specify_cli/integrations/bob/__init__.py), [bug workflow](https://github.com/github/spec-kit/blob/0443760542e7e5269724744a2ac55c4bd386d095/extensions/bug/README.md), [adapter tests](https://github.com/github/spec-kit/blob/0443760542e7e5269724744a2ac55c4bd386d095/tests/integrations/test_integration_bob.py) | [MIT](https://github.com/github/spec-kit/blob/0443760542e7e5269724744a2ac55c4bd386d095/LICENSE) |
| Verified Codebase Context | `52b67e61b0ecdac0aec7c17acb0852e0355f31c1` (`v1.1.0`) | [Contract, installation and validation limits](https://github.com/philo-x/spec-kit-preset-codebase-memory-context/blob/52b67e61b0ecdac0aec7c17acb0852e0355f31c1/README.md) | [MIT](https://github.com/philo-x/spec-kit-preset-codebase-memory-context/blob/52b67e61b0ecdac0aec7c17acb0852e0355f31c1/LICENSE) |
| Bob Control | `315cbf54076842f06462ea8846aae837594c67cd` | [README](https://github.com/PounceAI/bob-control/blob/315cbf54076842f06462ea8846aae837594c67cd/README.md), [checkpoint code](https://github.com/PounceAI/bob-control/blob/315cbf54076842f06462ea8846aae837594c67cd/src/checkpoint.ts), [judge code](https://github.com/PounceAI/bob-control/blob/315cbf54076842f06462ea8846aae837594c67cd/src/judge.ts) | [Apache-2.0](https://github.com/PounceAI/bob-control/blob/315cbf54076842f06462ea8846aae837594c67cd/LICENSE) |
| Bob+ and Headless Bob | `5c610971dc72f9e9035821b3cb2c3edea868f8b4` | [Extension changelog](https://github.com/ibm-self-serve-assets/building-blocks/blob/5c610971dc72f9e9035821b3cb2c3edea868f8b4/ibm-bob/extension/CHANGELOG.md), [headlessbob source](https://github.com/ibm-self-serve-assets/building-blocks/tree/5c610971dc72f9e9035821b3cb2c3edea868f8b4/ai/engineering/headless-bob/assets/headlessbob) | [Apache-2.0 root](https://github.com/ibm-self-serve-assets/building-blocks/blob/5c610971dc72f9e9035821b3cb2c3edea868f8b4/LICENSE); [MIT skills subtree](https://github.com/ibm-self-serve-assets/building-blocks/blob/5c610971dc72f9e9035821b3cb2c3edea868f8b4/ibm-bob/skills/LICENSE.txt) |
| IBM workshop | `352cdb45d8ad2a53b27aaa31a9248edf3bc8f2fe` | [Power-user lab](https://github.com/IBM/intro-bob-workshop/blob/352cdb45d8ad2a53b27aaa31a9248edf3bc8f2fe/docs/lab-7/README.md), [Python Bob loop skill](https://github.com/IBM/intro-bob-workshop/blob/352cdb45d8ad2a53b27aaa31a9248edf3bc8f2fe/.bob/skills/agent-with-bob-shell/SKILL.md) | [Apache-2.0](https://github.com/IBM/intro-bob-workshop/blob/352cdb45d8ad2a53b27aaa31a9248edf3bc8f2fe/LICENSE) |
| IBM demos | `bc8a8f874cd34abd6cff97bcbf863070710e7566` | [Beads example](https://github.com/IBM/bob-demo/blob/bc8a8f874cd34abd6cff97bcbf863070710e7566/beads/README.md), [skills example](https://github.com/IBM/bob-demo/blob/bc8a8f874cd34abd6cff97bcbf863070710e7566/getting-started-skills/README.md) | [Apache-2.0](https://github.com/IBM/bob-demo/blob/bc8a8f874cd34abd6cff97bcbf863070710e7566/LICENSE) |
| bob-skill-installer | `78a29b77cdfd6ed9feb46e2644e0e7b881093e0b` | [Installer code](https://github.com/funhere/bob-skill-installer/blob/78a29b77cdfd6ed9feb46e2644e0e7b881093e0b/src/bob_skill_installer/installer/installer.py), [tests](https://github.com/funhere/bob-skill-installer/blob/78a29b77cdfd6ed9feb46e2644e0e7b881093e0b/tests/unit/test_installer.py), [package metadata](https://github.com/funhere/bob-skill-installer/blob/78a29b77cdfd6ed9feb46e2644e0e7b881093e0b/pyproject.toml) | [Declared Apache-2.0](https://github.com/funhere/bob-skill-installer/blob/78a29b77cdfd6ed9feb46e2644e0e7b881093e0b/LICENSE) |

The observed Spec Kit release was [v1.1.3, published 9 October](https://github.com/github/spec-kit/releases/tag/v1.1.3), distinct from the main snapshot above. Verified Codebase Context's four command replacements retain a **1.1.2** baseline and require review with that newer release. Its README records commands without claiming the profile generator executed them, and explicitly qualifies concurrency protection and agent-test limitations.

## Material implementation notes

### Bob Control acceptance policy

In the [reviewed judge implementation](https://github.com/PounceAI/bob-control/blob/315cbf54076842f06462ea8846aae837594c67cd/src/judge.ts), an unavailable LLM judge returns `pass: true` with `error: true` and a recorded reason. This is an intentional fail-open policy, not evidence that an acceptance test succeeded. A configured verification command runs first and can independently fail the task. Evaluate the actual policy and recorded results for the workflow; this note does not characterize every task as unchecked.

### Skill installer backup behavior

The [README](https://github.com/funhere/bob-skill-installer/blob/78a29b77cdfd6ed9feb46e2644e0e7b881093e0b/README.md) says `--upgrade` retains a backup. At the reviewed revision, `_swap_into_place` deletes that backup after successful installation and `test_upgrade_replaces_and_cleans_backup` expects it to be absent. This is a source-level documentation mismatch; it was not reproduced by execution. Do not rely on the README's retained-backup promise for this revision.

### Bob+ packaging and scope

A `bob-plus-assets-1.1.0.vsix` file exists in the reviewed tree. Its presence establishes an artifact, not installation success. The version's changelog removes the Modes panel and adds automatic MCP configuration, while the older website guide still describes modes. The root license is Apache-2.0; the skills subtree has an MIT notice. Review the chosen asset and installed version rather than treating all documentation or licenses as interchangeable.

## Unresolved project identity

The exact public repository for **Propel SDLC for IBM Bob** has not been established. No substitute has been catalogued. A contributor can resolve this by providing the maintainer's repository or primary documentation identifying the Bob-specific project and its licensing. Search non-discovery does not show that a competing capability is absent.

## What additional evidence would help

Useful contributions include a Bob trial for the context preset, a dated install/coexistence report, or a resume exercise that changes relevant source after a checkpoint and records whether the agent detects stale evidence. Each should identify the source revision, Bob version and surface, environment, task, actual edits and checks, and limitations. Small fixtures establish their observed behavior; they do not establish large-repository performance.
