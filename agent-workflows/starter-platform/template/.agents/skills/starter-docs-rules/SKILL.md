---
name: starter-docs-rules
description: Maintain the starter repository docs taxonomy and templates. Use when Codex needs to create, rename, reorganize, or review documentation in the docs tree; document feature requirements, a platform operation, template rule, behavior guard, or library feature; choose between -requirements, -guide, -guard, -policy, -toolkit, -usage, or README.md index files; or update docs cross-links and README maps.
---

# 1 Starter Docs Rules

## 1.1 Overview

Apply a strict taxonomy to all markdown documentation files to ensure their purpose is immediately obvious from the filename. The repository uses explicit filename suffixes mapped to YAML frontmatter.

## 1.2 Workflow

1. Determine the core purpose of the documentation.
2. Select the appropriate suffix (`-requirements.md`, `-guide.md`, `-guard.md`, `-policy.md`, `-toolkit.md`, or `-usage.md`).
3. Set the `doc_type` YAML frontmatter to exactly match the suffix (without the dash).
4. Load the matching template from this skill's `references/` directory.
5. Create or reformat the document to **strictly follow** the headings and layout defined in the template. Do not invent new headings.
6. Keep directory index maps exactly as `README.md` without suffixes, using the `index_template.md`.

## 1.3 Core Expectations

- **Numeric Headings**: All headings must be prefixed with numeric hierarchy values (e.g. `# 1 Title`, `## 1.1 Section`, `### 1.1.1 Subsection`).
- **Strict Templates**: Every file must strictly adhere to the bundled template for its `doc_type`. Do not diverge from the predefined markdown headings.
- **Requirements (`*-requirements.md`)**: Use for concise, implementation-independent requirements covering one feature or a small group of related features. Set frontmatter to `doc_type: requirements`.
- **Guides (`*-guide.md`)**: Use for step-by-step instructions, workflows, and how-tos. Set frontmatter to `doc_type: guide`.
- **Guards (`*-guard.md`)**: Use for behavior protection examples with a short raw-readable summary and per-case accepted/rejected snippets tied to current tests. Set frontmatter to `doc_type: guard`.
- **Policies (`*-policy.md`)**: Use for strict governance rules, ownership boundaries, and architectural constraints. They must explicitly map Allowed and Rejected actions. Set frontmatter to `doc_type: policy`.
- **Toolkits (`*-toolkit.md`)**: Use for CLI command suites, scripts, repo-doctors, and quality gates. Set frontmatter to `doc_type: toolkit`.
- **Usages (`*-usage.md`)**: Use for Python codebase interfaces, architectural usage specs, and static topological maps. Set frontmatter to `doc_type: usage`.
- **Indexes (`README.md`)**: Use purely as a mapping for a directory. Do not add suffixes to these files so GitHub UI rendering continues to work. Set frontmatter to `doc_type: index`.
- **Separation of Concerns**: Do not mix concerns. A single file should not act as both a guide and a toolkit. Split them if necessary.

## 1.4 Reference Map

- `references/requirements_template.md`
  Load this template whenever creating or formatting a `-requirements.md` file.
- `references/guide_template.md`
  Load this template whenever creating or formatting a `-guide.md` file.
- `references/guard_template.md`
  Load this template whenever creating or formatting a `-guard.md` file.
- `references/policy_template.md`
  Load this template whenever creating or formatting a `-policy.md` file.
- `references/toolkit_template.md`
  Load this template whenever creating or formatting a `-toolkit.md` file.
- `references/usage_template.md`
  Load this template whenever creating or formatting a `-usage.md` file.
- `references/index_template.md`
  Load this template whenever creating or formatting a `README.md` directory map.
- `docs/README.md`
  Load when you need to understand the root documentation map and the core platform domains.

## 1.5 Execution Notes

- Update cross-links and `README.md` maps whenever a file is renamed or added.
- When reformatting an existing file to match a template, preserve the core informational content but rigorously align the structure.
