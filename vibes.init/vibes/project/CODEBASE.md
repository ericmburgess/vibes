**INSTRUCTIONS FOR CLAUDE:**
- The purpose of this document is for YOU to orient YOURSELF at
  the start of each coding session.
- It is NOT intended to be comprehensive. It's just a rough ROADMAP.
- KEEP THIS DOCUMENT VERY LEAN! You're going to be revising it at
  the end of each coding session.

# Vibes Framework Codebase Documentation

## Project Overview

A framework for structured development sessions with Claude Code, emphasizing focused work through sessions and tasks.

## Structure

- `.claude/commands/vibes/` - Claude Code slash commands for the framework
    - `startsession.md` - Begin development sessions with goal setting
    - `task.md` - Plan and execute focused work units
    - `endsession.md` - Document completed work and commit changes
    - `help.md` - Display framework usage instructions
- `vibes.init/` - Template files for new projects using the framework
    - `vibes/instructions/` - Documentation templates and guidelines
        - `documenting-a-session.md` - Session logging format and requirements
        - `summarizing-the-codebase.md` - Codebase documentation guidelines
    - `vibes/project/` - Project metadata templates
        - `CODEBASE.md` - Project structure and architecture template
        - `TODO.md` - Task tracking template
    - `vibes/vibes-help.md` - Framework workflow documentation
    - `vibes/worklogs/` - Session tracking templates
        - `WORKLOG.md` - Session history template

## Design Principles

- **Session-based workflow**: Major goals broken into focused sessions
- **Task decomposition**: Sessions divided into self-contained work units
- **Documentation-driven**: Comprehensive tracking of development progress
- **Template-based**: Standardized structure for consistent project setup

## Tooling

- Claude Code with custom slash commands
- Git for version control and session boundaries
- Markdown for documentation and templates
