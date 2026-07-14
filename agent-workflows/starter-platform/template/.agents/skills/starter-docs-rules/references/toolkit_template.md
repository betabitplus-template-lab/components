---
name: toolkit-template
description: Template for a toolkit document defining CLI command suites, scripts, repo-doctors, and quality gates.
---

# 1 Toolkit Template

## 1.1 Overview

Use this template to document a suite of tools, automated scripts, or commands.

## 1.2 When To Use

Use this template when documenting CLI tools, repo-doctor routines, CI verification scripts, or any command-line execution interfaces.

## 1.3 File Shape

1. frontmatter (with `doc_type: toolkit`)
2. title
3. `Overview`
4. `Commands` (or `Routines`)
5. `Usage`

## 1.4 Rules

- Use `###` for each specific command or routine.
- Include the exact CLI invocation inside a `bash` code block.
- Describe what the command does, its flags, and expected outputs.

## 1.5 Template

```md
---
name: <unique-name>
doc_type: toolkit
description: <Short description of the toolkit>
---

# 1 <Toolkit Title>

## 1.1 Overview

<Brief summary of the toolkit's purpose.>

## 1.2 Commands

### 1.2.1 <Command Name>

<Description of what the command does.>

```bash
uv run <command-name>
```

## 1.3 Usage

<Optional: Step-by-step example of how to use the commands together.>
```
