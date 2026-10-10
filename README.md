# Awesome Bob Workflows

A curated guide to public IBM Bob workflows, skills, learning material, and integration projects.

This is an independent community catalogue. It is not an IBM product, an official marketplace, or a certification programme. Entries are selected for relevance and inspectable evidence; inclusion is not an endorsement or a guarantee that a project will work in your environment.

**Source review: 10 October 2026 (Europe/Dublin).** All seven initial project entries are based on public documentation and repository inspection. None has been installed or run with Bob by this catalogue. The machine-readable [catalogue](catalog/projects.json) records the evidence and review date for each entry.

## Find a useful starting point

| Your goal | Start with |
| --- | --- |
| Learn the extension points and see examples | [Official references](#official-references), IBM Bob Workshops, and IBM Bob Demos |
| Turn a substantial feature into a specification and plan | GitHub Spec Kit |
| Add a domain-specific skill or integration | Bob+ Technology Building Blocks |
| Investigate skill installation and conversion | bob-skill-installer |
| Explore repository onboarding as a guided experience | OnboardOps |
| Study investigation, regression evidence, and debugging handoffs | Debug Swarm |
| Install a small operating workflow, evaluate it, or explore a runner | [Companion projects](#companion-projects) |

Follow the upstream instructions for the version you intend to use. This catalogue does not install third-party content or run commands from the linked projects.

## Read the status correctly

Three different observations matter:

- **Public source:** an inspectable repository is available. This does not establish that a release package exists or that the project runs.
- **Installation documented:** upstream provides setup or usage instructions. Those instructions have not necessarily been executed by a catalogue contributor.
- **Runtime evidence:** a dated report names the source revision, exact Bob version, interface, environment, task, and result. A linked report applies to that combination and task; it is not universal support.

The initial entries have **documentation review only** and no runtime evidence. “Not assessed” means we did not establish a fact during this review; it does not mean the capability is absent. Repository licenses describe upstream material and do not turn every dependency or service into a free or supported product.

See the [curation policy](docs/curation.md) and [metadata format](docs/metadata.md) for the full definitions.

## Specifications and planning

### GitHub Spec Kit

[Source](https://github.com/github/spec-kit) · [Official IBM Bob integration reference](https://github.github.io/spec-kit/reference/integrations.html) · MIT

Spec Kit supplies structured development processes and reusable templates. Its integration guide explicitly lists IBM Bob under the `bob` key. The documented default writes `speckit-<command>/SKILL.md` files into `.bob/skills/` and uses `/speckit-<command>` invocation. The same guide distinguishes the deprecated Bob 1.x command layout and its migration.

Useful when a task needs a maintained specification and plan. Installation is documented; this catalogue has not executed it.

## Learning and examples

### IBM Bob Workshops

[Source](https://github.com/IBM/intro-bob-workshop) · [Workshop site](https://ibm.github.io/intro-bob-workshop/) · Apache-2.0

Workshop source, exercises, and an `agent-with-bob-shell` skill. The power-user material covers rules, skills, MCP, repository analysis, and team workflows. Labs have different audiences; the power-user workshop specifically targets IBM employees, while other material addresses external audiences.

Use it to learn the underlying mechanisms and adapt an appropriate exercise. Setup and usage are documented; no catalogue runtime test has been performed.

### IBM Bob Demos

[Source](https://github.com/IBM/bob-demo) · Apache-2.0

Examples cover skills, documentation indexing, architecture work, modernization, and DevOps. Check each example's version assumptions: the reviewed README still lists earlier modes such as Code, Advanced, and Orchestrator. Its public-repository disclosure distinguishes this source project from a supported IBM product.

Useful as task examples, with installation instructions to review before trying them.

## Skills and domain integrations

### Bob+ Technology Building Blocks

[Source](https://github.com/ibm-self-serve-assets/building-blocks) · [Skills documentation](https://ibm-self-serve-assets.github.io/building-blocks-docs/ai-core/bob-skills-and-modes/) · Apache-2.0

IBM Build Engineering reference implementations include integration assets and Bob skills and modes. A public [skills ZIP](https://github.com/ibm-self-serve-assets/building-blocks/blob/main/ibm-bob/skills.zip) is visible, and the documentation describes project and global skill locations.

An [extension installation guide](https://ibm-self-serve-assets.github.io/building-blocks-docs/ibm-bob/extension/install/) describes a VSIX interface. This review did not verify a downloadable VSIX package or execute the skills. Choose relevant domain assets individually.

## Distribution and installation tools

### bob-skill-installer

[Source](https://github.com/funhere/bob-skill-installer) · Apache-2.0

A community Python implementation for fetching, converting, validating, and installing skills. It documents project/global scope, dry runs, and upgrade backups.

Review the options before use: its documented default preserves source files, including secret files unless excluded. A converter's output still needs inspection for the destination Bob client's tools and behavior. Installation is documented; the catalogue has not run the tool or its scanner.

## Onboarding and debugging

### OnboardOps

[Source](https://github.com/rohan879/OnboardOps) · MIT

A community hackathon project combining Bob onboarding instructions, skills, an MCP server, and a dashboard for repository exploration and learning. It is useful as an example of a richer onboarding experience.

The public source and documented design were reviewed. Installation was not assessed. Its custom-mode representation needs checking against the actual Bob client before use.

### Debug Swarm

[Source](https://github.com/Gabriel-ASM/IBM-Bob-Hackathon) · MIT

A community hackathon project with a seven-phase debugging skill, focused investigators, stored run artifacts, a dashboard, and a benchmark containing planted bugs. It documents setup and replayable reference runs.

Useful for studying how investigation and regression evidence can be made visible. Upstream test counts and benchmark outcomes have not been independently reproduced here.

## Official references

These are product references, not open-source package entries. Consult the page for your actual client and version:

| Topic | Primary reference |
| --- | --- |
| IDE custom rules | [IBM Bob IDE rules](https://bob.ibm.com/docs/ide/configuration/rules) |
| Shell custom rules | [IBM Bob Shell rules](https://bob.ibm.com/docs/shell/configuration/bobshell-custom-rules) |
| IDE skills | [IBM Bob IDE skills](https://bob.ibm.com/docs/ide/features/skills) |
| Shell skills and invocation | [Create and use skills in Bob Shell](https://bob.ibm.com/docs/shell/tutorials/use-skills) |
| Working with large projects | [Large projects](https://bob.ibm.com/docs/ide/core-concepts/large-projects) |
| Context management | [Context-window management](https://bob.ibm.com/docs/ide/core-concepts/context-window-management) |
| Automated Shell use | [Non-interactive Bob Shell](https://bob.ibm.com/docs/shell/getting-started/start-bobshell-non-interactive) |
| Release-specific changes | [IDE changelog](https://bob.ibm.com/docs/ide/changelog) and [Shell changelog](https://bob.ibm.com/docs/shell/changelog) |

Descriptions in this catalogue are original summaries. Primary links and the claims they support are also recorded in [catalog/projects.json](catalog/projects.json).

## Companion projects

These public companion repositories cover different parts of the workflow. Check each repository's own implementation status and available validation evidence.

| Repository | Intended responsibility |
| --- | --- |
| [bob-workflow-kit](https://github.com/Saqlain1999/bob-workflow-kit) | A practical guide, operating instructions, a focused skill, installation tooling, and recovery templates |
| [bob-workflow-evals](https://github.com/Saqlain1999/bob-workflow-evals) | Reproducible tasks and evidence for assessing workflow behavior |
| [bob-workflow-runner](https://github.com/Saqlain1999/bob-workflow-runner) | Controller design preview; no executable runner |
| This catalogue | Source-backed discovery and clearly scoped compatibility notes |

Keep each project's role separate. A catalogue entry is not a performance result; an evaluation is not an installation guide; a runner only controls work launched through that runner.

## Contribute a useful entry

Start with [CONTRIBUTING.md](CONTRIBUTING.md), copy [the entry template](templates/project-entry.json), and provide a direct primary link showing the Bob connection. An author's own example or a public implementation is useful evidence. Popularity and marketing language alone are not.

Corrections to stale paths, ambiguous licensing, unavailable artifacts, or version assumptions are valuable contributions. Disclose an affiliation with a project you submit. We do not rank projects by stars, claim exhaustive coverage, or copy upstream performance claims as verified results.

## Validate the catalogue locally

Python 3.10 or later is the validator's compatibility target. It uses only the standard library.

```sh
python3 tools/validate_catalog.py
```

The command checks metadata structure, source URLs, IDs, review/evidence consistency, README coverage, and repository-local Markdown links. It performs no network requests and does not install or evaluate any listed project. It exits nonzero for invalid catalogue content. The included CI workflow runs this same check; a workflow definition is not evidence that hosted CI has passed.

See [VALIDATION.md](VALIDATION.md) for the actual local preparation record.

## License and community

Original catalogue text, metadata, and tooling are available under the [MIT license](LICENSE). Linked projects retain their own licenses, trademarks, and support arrangements.

Follow the [community conduct guide](CODE_OF_CONDUCT.md). For catalogue corrections, use an issue or pull request; for a problem in an upstream tool, consult that project's support instructions. See [SECURITY.md](SECURITY.md) before sharing sensitive findings.
