---
name: policy-template
description: Template for a policy document defining strict governance rules, ownership boundaries, and architectural constraints.
---

# 1 Policy Template

## 1.1 Overview

Use this template to create a strict constraint or boundary document.

## 1.2 When To Use

Use this template when a user asks to enforce a rule, define ownership boundaries, or document strict restrictions.

## 1.3 File Shape

All policies use the exact same Domain Block shape. Even if the policy only enforces a single global rule, it must be contained within a logical Domain Block (e.g., `## Legacy Boundaries`).

1. frontmatter (with `doc_type: policy`)
2. title
3. `Rule` (Overall thesis statement)
4. `## [Domain Name 1]` (e.g. `## Project Structure` or `## Legacy Boundaries`)
   - `### Allowed`
   - `### Rejected`
   - `### Mechanism`
5. `## [Domain Name 2]` (If the policy governs multiple distinct domains, repeat the block.)

## 1.4 Rules

- Keep the document highly directive.
- Clearly separate what is allowed from what is prohibited using bullet points under the Domain Block.
- The `Rule` section should be a single, clear thesis sentence.
- If a section does not apply (e.g. there are no explicit "Rejected" paths), you can omit that H3, but you must keep the Domain H2.

## 1.5 Template

```md
---
name: <unique-name>
doc_type: policy
description: <Short description of the rule>
---

# 1 <Policy Title>

## 1.1 Rule

<The core constraint or boundary defined in 1-2 sentences.>

## 1.2 <Domain Name>

### 1.2.1 Allowed

- <Explicitly permitted action or structure>

### 1.2.2 Rejected

- <Explicitly rejected action or structure>

### 1.2.3 Mechanism

<How the platform enforces this rule, e.g., CI scripts or Copier checks.>
```
