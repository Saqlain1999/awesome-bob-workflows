# Validation record

Prepared 10 October 2026 (Europe/Dublin).

## Source review

The seven initial entries were reviewed using the primary sources recorded in [catalog/projects.json](catalog/projects.json). Repository availability, documented features, and license labels were inspected. No listed project was installed or executed by this catalogue, and no live Bob compatibility is claimed.

The public skills ZIP for Bob+ was visible. A downloadable VSIX package was not verified. Upstream test totals, performance numbers, and runtime outcomes were not independently reproduced.

## Local checks

Executed on Linux with Python **3.12.14** during preparation. Python 3.10 is the source compatibility target; no Python 3.10 execution is claimed.

`python3 tools/validate_catalog.py` exited **0** and reported:

```text
Validated 7 project entries, 10 Markdown files, and 22 local links.
External sources and Bob runtime behavior were not tested by this command.
```

An additional in-memory/disposable-fixture check confirmed rejection of four invalid cases: a runtime claim without evidence, a duplicate project, a credential-bearing source URL, and missing local file/heading targets. It exited **0**. No upstream installer, model, or work repository was used.

The command checks metadata and inline local Markdown paths/headings. It does not fetch external links or establish that their contents remain accurate. Repository URLs and technical facts need human review.

## Hosted CI and publication

The [GitHub Actions workflow](.github/workflows/validate.yml) uses the official [checkout](https://github.com/actions/checkout) and [setup-python](https://github.com/actions/setup-python) actions pinned to v7 commit references, read-only repository permissions, and no Bob credentials.

[GitHub Actions run 38008136347](https://github.com/Saqlain1999/awesome-bob-workflows/actions/runs/38008136347) completed successfully for published commit `c57876a4e6c3d1a8f894c795d12bf99fa63068ce` on 10 October 2026 (UTC). The `catalogue` job passed on `ubuntu-latest` with Python 3.12. This validates the catalogue's own metadata and local links; it does not install or execute any listed project.

The catalogue and companion repositories are now public. Publication and catalogue CI do not change the listed projects' runtime-evidence labels.
