---
name: index-template
description: Template for a directory index map (README.md) organizing related documentation files.
---

# 1 Index Template

## 1.1 Overview

Use this template to create a mapping for a documentation domain directory.

## 1.2 When To Use

Use this template for the `README.md` file located at the root of a domain directory in `docs/`.

## 1.3 File Shape

1. frontmatter (with `doc_type: index`)
2. title
3. Domain description
4. `Files` or `Concepts` section

## 1.4 Rules

- The filename must always be `README.md` (no suffix).
- Provide a short 1-2 sentence description of the domain.
- The `Files` section must list all files in the directory as markdown links.
- Use the exact filename and match the description from the target file's frontmatter.

## 1.5 Template

```md
---
name: <folder-name>
doc_type: index
description: Index for <domain> docs.
---

# 1 <Domain Title>

<1-2 sentences describing the domain.>

## 1.1 Files

- [<file-name-guide.md>](<file-name-guide.md>)
  <Short description matching the file's frontmatter description.>
```
