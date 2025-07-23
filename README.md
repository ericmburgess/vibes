# `vibes` - Vibe coding for developers

`vibes` is intended to avoid the worst pitfalls of vibe coding, without taking all the fun out of it. It's aimed at professional developers, and may not provide a good experience for non-programmers. (Though this has not been tested!)

The intent is to give you a good chance to catch Claude's mistakes before it's too late, while still having him do most of the work for you.

## Claude needs discipline!

The following structure is imposed on each vibe session. It may sound like a lot, but it flows *very* naturally, and you don't have to remember all of it (or read any of it). Claude guides you through it very unobtrusively.

### Overview

1. Begin a **session** with a defined goal, refine it together, and create subtasks.
2. Tackle the **tasks** one by one.
3. End the **session** by updating documentation and logging the work, committing to git, and clearing Claude's memory.
4. Go to step 1.

### Detailed workflow

1. A **session** encapsulates a meaningful unit of work, before and after which the code will be in a working state. It could be a story/ticket/issue, or part of one. It has a definite goal, and you and Claude will refine the goal and define specific requirements together.
2. The session is then broken into **tasks**. Claude is pretty darn good at this part! A **task** is a portion of the full job. The crucial thing is that it is self-contained *and can be validated*.
3. Claude is *not allowed* to plan the concrete implementation of any task until the session requirements and tasks have been clearly established. 
4. Individual tasks are now tackled, one at a time. Claude will propose a low-level implementation plan (at the level of classes, functions, modules). He is *not allowed* to propose any edits until you have agreed on this plan. This allows you to correct, interrogate, or redirect him.
    - The list of **tasks** is not set in stone. They will often evolve in response to the choices made during previously completed tasks.
    - The **session** goal *will not* change during the session unless you explicitly say so.
6. Once the session goal has been accomplished, the session is finalized:
    - Claude maintains his own very high-level project documentation to keep himself orientated between sessions. He updates it now to reflect the work done.
    - Claude records what was done during the session in two forms: a detailed `session.<session#>.md` file, and a brief summary prepended to the `WORKLOG.md` file.
    - Claude asks permission to `git add` and `git commit`, suggesting a commit message. More likely, you hit Esc and do that part yourself.
    - Claude's memory is wiped with `/clear`, and then a new session can begin. **Don't neglect `/clear`!** Claude gets confused when his context is too large or includes stuff unrelated to the current task.

Item 4 is the most beneficial because it addresses, in my experience, the worst pain point of vibing with Claude. I kept catching him trying to do naive or ridiculously overcomplicated things when I looked at his proposed file edits. But it was easy to miss these looking at one part of one file at a time. His misguided plan might not be apparent from the first seven edits! He's *generally* able to revert accurately when you ask him to, but it's by no means guaranteed.

Forcing Claude to be very specific about his plan for a group of edits *before* making any of them makes it *much* easier to notice when he's about to drive off the cliff, before it's too late!

## Installation

1. From this repo's root, run `vibes-deploy <your repo root>` to install `vibes` in your repository.
2. Change to your repo root and run `claude`, then run these commands:
    - `/vibes:init-existing` to have Claude analyze your codebase and save a summary to `vibes/project/CODEBASE.md`.
    - `/vibes:build-worklog` to have Claude analyze a portion of your `git log` and create an initial `vibes/worklogs/WORKLOG.md`.
3. Review what Claude produced, and revise it as necessary.
4. Open Claude again, and run these commands:
    - `/vibes:howto` to learn how it works.
    - `/vibes:startsession` and get to vibing!
5. Claude will prompt you to use `/vibes:task` and `/vibes:endsession` at the appropriate times.

The deployment adds:
- `vibes/` directory with project templates and documentation
- `.claude/commands/vibes/` with framework commands  

# CAVEAT

Take EXTRA care if you're working with any sensitive information. Claude is prone to include full paths in his work logs, and is not smart about committing secrets. In fact, just don't use this for anything sensitive at all. That would be insane.

## Dogfooding!

The "source code" is in the `vibes.init/` folder. The `vibes/` and `.claude/` folders in the root of *this* repo are the ones that `vibes` installs and maintains when you use it in your project. That's because I'm using `vibes` while developing `vibes`. Explaining this to Claude so that he reliably understands was a fun exercise.
