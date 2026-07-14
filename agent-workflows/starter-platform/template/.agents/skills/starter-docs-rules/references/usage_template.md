---
name: usage-template
description: Template for a usage document defining technical specifications, Python code interfaces, and architectural mappings.
---

# 1 Usage Template

## 1.1 Overview

Use this template to create an internal codebase API, architectural specification, or structural usage document.

## 1.2 When To Use

Use this template to document static information, system mechanics, or Python code interfaces exported by the runtime or tooling packages.

## 1.3 File Shape

1. frontmatter (with `doc_type: usage`)
2. title
3. `Overview`
4. `Features`
5. `Examples`
6. `Runnable Examples`

## 1.4 Rules

- Provide a concise, bulleted list of features at the top so readers can instantly grasp what the component is capable of.
- The `Examples` section is the core of the document. Strongly encourage multiple examples.
- Group examples by feature or specific situational context using `###` headers.
- Include complete Python code blocks for each example showing both the exact imports and the contextual usage.
- Add `Runnable Examples` when a committed script demonstrates the full public API flow better than inline snippets.
- Link runnable examples to real files and include exact commands.
- Use `examples/` for illustrative public API scripts, `tests/**/e2e/` for asserted behavior scenarios, and `workbench/` for manual live investigation.
- Avoid mixing step-by-step CI workflows here; point to a `-guide.md` instead if workflows are needed.

## 1.5 Template

````md
---
name: <unique-name>
doc_type: usage
description: <Short description of the component>
---

# 1 <Usage Title>

## 1.1 Overview

<Brief summary of what this component or API does.>

## 1.2 Features

- <Feature 1 description>
- <Feature 2 description>
- <Feature 3 description>

## 1.3 Examples

### 1.3.1 <Feature 1 or Context A>

<Brief explanation of the situation and how this feature solves it.>

```python
from py_lib_runtime import <component>

# Example demonstrating Feature 1 in context
```

### 1.3.2 <Feature 2 or Context B>

<Brief explanation of the situation and how this feature solves it.>

```python
from py_lib_runtime import <component>

# Example demonstrating Feature 2 in context
```

## 1.4 Runnable Examples

- `<path/to/example.py>`
  Run with: `<command>`
````
