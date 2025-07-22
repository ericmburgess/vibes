# Plan a unit of work

Plan a **task**, which is a unit of work (a set of related code edits). Multiple
tasks will be performed in order to achieve the session's **goal**, which
was defined at the beginning of the session. Tasks are discussed at the
same level of detail as in this sample:

```
I need to update all the API instantiations in the find.py file. There are several instances:
  1. Line 148: InstitutionsAPI
  2. Line 152: CasesAPI 
  3. Line 186: PatientsAPI
  4. Line 190: CasesAPI
  5. Line 238: CasesAPI

I need to add the base_url parameter to all of them. Then I will add this
argument everywhere these functions are called.
```
  
Go back and forth with the user until you have settled on the details. Once you
have, and the user has instructed you to begin, then begin.

**IMPORTANT** ALWAYS lean toward simplicity and minimality. In particular,
- Do not catch exceptions unless they are expected during normal operation. Unexpected
  errors should simply crash.
- If there is doubt about how to accomplish the task at the code level, e.g.,
  interfacing with an external resource, make a proof-of-concept script in
  `scratch/` first, before modifying the project code.

## Usage

```
/plan <task>
```

**Parameters:**
- `task`: Description of the single task. Typically a list of tasks will already have been agreed upon, so if no task description is provided, assume it is the next task in the list.

## What it does

- **BRIEFLY restates** the session goal and current progress.
- **Plans** a specific implementation.
- **Describes** the proposed implementation.
    - The level of detail here is intermediate between the task description and
      the actual code edits. For example, new classes/methods, refactorings,
      control flow changes, etc.
- **Discusses** the plan with the user, until they are happy with the plan.
- **Implements** the plan, with the user's permission.

## Output

- A concrete, code-level plan for completing the task.

