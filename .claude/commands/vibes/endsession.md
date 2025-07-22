# End Development Session

Document a completed work session and prepare for the next.

## Usage

```
/endsession <instructions>
```

**Parameters:**
- `instructions`: Additional instructions to be followed while completing the command.

## What it does

- Documents the work done according to the instructions in
  `vibes/instructions/documenting-a-session.md`.
- Offers to execute `git add .` and `git commit -m <message>`. The format for commit messages is:
    - A single line
    - all lowercase
    - present tense
    - as terse as possible
    - e.g.: `[1234] streamline authentication`
- Prompts the user to use /clear and /startsession to continue development.

