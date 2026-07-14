---
name: guard-template
description: Template for a guard document showing behavior protected by tests with compact accepted and rejected examples.
---

# 1 Guard Template

## 1.1 Overview

Use this template to document tested protection behavior with examples readers can scan without opening fixture data.

## 1.2 When To Use

Use this template when a policy, invariant, or sync rule is enforced by tests and readers need concrete pass/fail examples.

## 1.3 File Shape

1. frontmatter (with `doc_type: guard`)
2. title
3. `Overview`
4. `At A Glance`
5. `Guard Cases`
6. `Enforcement`

## 1.4 Rules

- Keep the document focused on one guard or one tightly related guard family.
- Start with a compact raw-readable summary that orients readers without repeating examples, rejection notes, or scenario names.
- Use repeated guard-case blocks instead of one large accepted section and one large rejected section.
- Each guard case must include `Protected`, `Accepted`, `Rejected`, `Why rejected`, and `Covered by` labels.
- Keep snippets minimal and label the file or surface they belong to when it is not obvious.
- Link to the tests, scenarios, or command that enforce the guard.
- Do not replace policy docs; link to the policy when a governance rule exists.

## 1.5 Template

````md
---
name: <unique-name>
doc_type: guard
description: <Short description of the protected behavior>
---

# 1 <Guard Title>

## 1.1 Overview

<Brief summary of what behavior is protected and why it matters.>

## 1.2 At A Glance

- `<surface-or-behavior>`: <one sentence explaining what is protected and what kind of drift is rejected.>
- `<surface-or-behavior>`: <one sentence explaining another protected case.>

## 1.3 Guard Cases

### 1.3.1 <Surface Or Behavior>

Protected:

- <Specific invariant protected by tests>

Accepted:

```toml
<minimal accepted snippet>
```

Rejected:

```toml
<minimal rejected snippet>
```

Why rejected:

- <Short reason the rejected snippet violates the protected behavior.>

Covered by:

- Pass: `<scenario-name>`
- Fail: `<scenario-name>`

## 1.4 Enforcement

- Test: `<path/to/test>`
- Command: `<command>`
````
