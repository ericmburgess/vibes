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
- Offers to execute `git add .`, telling the user they may hit Esc and stage the files themselves if they prefer.
- Offers to execute `git commit -m <message>`. **PROPOSE A MESSAGE IN THE FOLLOWING FORMAT:**
    - all lowercase
    - present tense
    - as terse as possible
    - e.g.: `[1234] streamline authentication`
    - ONLY ONE SINGLE LINE, NOTHING ABOUT CLAUDE!
    - Tells the user they may hit Esc and type their own commit message.
        - If they do not include the `[session_number]` prefix, add it, **CHANGING NOTHING ELSE**, and ask again.
- Prompts the user to use /clear and /startsession to continue development.

