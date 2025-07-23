# Initialize Vibes in Existing Project

Analyze an existing codebase and generate initial `CODEBASE.md` documentation.

## Usage

```
/vibes:init-existing
```

## What it does

- **Verifies** that you're in a project with vibes installed (`vibes/` directory exists)
- **Analyzes** the current project structure by:
  - Examining the directory tree to identify key folders (src/, lib/, components/, tests/, etc.)
  - Reading key files (README.md, package.json, requirements.txt, etc.) to understand the project
  - Identifying the project type and main technologies used
- **Generates** an initial `vibes/project/CODEBASE.md` following the directions in `vibes/instructions/summarizing-the-codebase.md`.
- **Asks clarifying questions** only when truly necessary. The user will likely want to revise the document themselves.

## Output

- A populated `CODEBASE.md` that gives you context about the existing project structure
- Suggestions for additional documentation that might be helpful

## Notes

This is meant to be run once after deploying vibes to create the initial project documentation. Focus on documenting what exists rather than making assumptions about what should exist.
