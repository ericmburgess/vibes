# Log My Work

Document work that has already been completed and is currently staged.

## Usage

```
/log-my-work <instructions>
```

**Parameters:**
- `instructions`: Additional instructions to be followed while completing the command.

## What it does

- **Confirms** that there are staged changes to document by checking `git status --porcelain --cached`.
- **Analyzes** the staged changes using `git diff --cached` to understand what work was completed.
- **Documents** the work done according to the instructions in `vibes/instructions/documenting-a-session.md`.
- **Does NOT** automatically stage or commit files - works only with changes that are already staged.
- Offers to execute `git commit -m <message>`. **PROPOSE A MESSAGE IN THE FOLLOWING FORMAT:**
    - all lowercase
    - present tense
    - as terse as possible
    - e.g.: `[1234] streamline authentication`
    - ONLY ONE SINGLE LINE, NOTHING ABOUT CLAUDE!
    - Tells the user they may hit Esc and type their own commit message.
        - If they do not include the `[session_number]` prefix, add it, **CHANGING NOTHING ELSE**, and ask again.
- Prompts the user to use /clear and /startsession to continue development.


## Output

- Session documentation file with analysis of the staged work
- Updated worklog entry summarizing the completed tasks
- Updated CODEBASE.md if the staged changes affect project structure
