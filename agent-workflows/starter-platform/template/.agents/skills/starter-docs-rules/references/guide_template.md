---
name: guide-template
description: Template for a guide document defining step-by-step instructions, workflows, and how-tos.
---

# 1 Guide Template

## 1.1 Overview

Use this template to create an instructional workflow or step-by-step guide.

## 1.2 When To Use

Use this template when a user asks how to perform a specific task or workflow (e.g., releasing, syncing, or switching runners).

## 1.3 File Shape

1. frontmatter (with `doc_type: guide`)
2. title
3. `Overview`
4. `When To Use` or `Prerequisites` (Optional)
5. `Steps` or `How To Apply`
6. `Validation` (Optional)

## 1.4 Rules

- Steps must be actionable and clearly separated (e.g. numbered lists, or clear subsections like "Local Compute" and "GitHub-Hosted").
- Include the bash commands or code necessary to complete the steps.
- If applicable, explain how the user can verify their actions were successful.

## 1.5 Template

```md
---
name: <unique-name>
doc_type: guide
description: <Short description of the workflow>
---

# 1 <Guide Title>

## 1.1 Overview

<Brief summary of what this workflow accomplishes.>

## 1.2 When To Use

<Optional: Conditions under which this guide should be executed.>

## 1.3 Steps

1. <Actionable step 1>
   ```bash
   <command>
   ```

## 1.4 Validation

<How to verify the workflow succeeded.>
```
