---
name: requirements-template
description: Template for concise requirements covering one feature or a small group of related features.
---

# 1 Requirements Template

## 1.1 Overview

Use this template to record agreed product or feature requirements.

## 1.2 When To Use

Use it when the requested behavior should be kept as a durable, implementation-independent specification.

## 1.3 File Shape

1. frontmatter (with `doc_type: requirements`)
2. title naming the exact feature scope
3. one or more domain sections
4. one `REQ-NN` subsection per requirement
5. one short requirement statement under each subsection

## 1.4 Rules

- Include only feature-specific requirements that are non-standard, surprising, or intentionally different from normal implementation defaults.
- Omit anything a reasonable implementation would already do without an explicit requirement.
- Do not add a requirement when the same constraint is already covered elsewhere in the document.
- Include a requirement only when omitting it could reasonably lead to a different acceptable implementation.

## 1.5 Template

```md
---
name: <feature-name>-requirements
doc_type: requirements
description: Requirements for <specific feature scope>.
---

# 1 <Feature Name> Requirements

## 1.1 <Domain Name>

### 1.1.1 REQ-01 — <Short Name>

<One short requirement statement.>
```
