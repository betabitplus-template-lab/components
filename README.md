# Template Components

Reusable template source lives here. Each component stores output files under
its own `template/` payload directory.

Committed template builds live in `template-builds/`. Edit components first,
then assemble builds.

## Current Components

| Component | Generated surface | Consumers |
| --- | --- | --- |
| `agent-workflows/core` | Repository-agnostic agent skills and `RTK.md` | standard, internal, platform |
| `agent-workflows/starter-platform` | Starter-specific documentation taxonomy skill | platform |
| `agent-workflows/python-library` | Generated-library `AGENTS.md` and Python library rules | standard, internal |
| `common-project/hygiene` | Shared `.editorconfig`, `.gitleaks.toml`, and `typos.toml` | standard, internal, platform |
| `common-project/identity` | `README.md`, `MANIFEST.in` | standard, internal |
| `common-project/license` | Reusable `LICENSE` | standard, internal, platform |
| `common-project/changelog-bootstrap` | Initial generated `CHANGELOG.md` | standard, internal |
| `common-project/markdown` | Markdown lint, format, and link-check config | standard, internal, platform |
| `python/config-surface` | Public and internal config modules under `src/[[[ package_name ]]]/` | standard, internal, platform |
| `python/docs-surface` | Generated package docs under `docs/` | standard, internal |
| `python/examples-surface` | Runnable examples under `examples/` | standard, internal |
| `python/gitignore` | Copier-aware Python project `.gitignore` | standard, internal, platform |
| `python/package-surface` | Base package markers under `src/` | standard, internal, platform |
| `python/pyproject` | Generated project `pyproject.toml` | standard, internal |
| `python/tests-surface` | Generated pytest tree under `tests/` | standard, internal |
| `python/workbench-surface` | Workbench package markers under `workbench/` | standard, internal |
| `repo-shell/copier-answers` | Copier-generated answers file selected by `_copier_conf.answers_file` | standard, platform |
| `repo-shell/contributing-guide` | Generated `CONTRIBUTING.md` | standard |
| `repo-shell/dev-environment` | Devcontainer, direnv, setup, and environment scripts | standard, platform |
| `repo-shell/editor` | VS Code workspace defaults | standard, platform |
| `repo-shell/github-ci` | Reusable setup action and CI workflows | standard, platform |
| `repo-shell/github-repository` | Downstream administration, release, Renovate, and PR files | standard |
| `repo-shell/quality-hooks` | Generated pre-commit configuration | standard |
| `repo-shell/scripts` | Generated repo script entrypoints | standard |
| `repo-shell/template-sync` | Profile-aware starter-sync workflow | standard, platform |

`agent-workflows/starter-platform` intentionally remains platform-only until its
documentation taxonomy is generalized for generated libraries.

`python/config-surface`, including `_api/types.py`, and
`python/package-surface` are shared without platform-specific branches.
Starter-only APIs, type declarations, and config additions remain normal local
changes preserved by Copier; they do not require separate components.

## Assembly

Validate assembled builds with:

```bash
uv run py-lib-check-template-components
```

Assemble one build without touching committed outputs:

```bash
uv run py-lib-assemble-template python-lib-standard --output /tmp/python-lib-standard --clean
uv run py-lib-assemble-template python-internal-package --output /tmp/python-internal-package --clean
uv run py-lib-assemble-template python-starter-platform --output /tmp/python-starter-platform --clean
```
