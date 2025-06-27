# Workflow Prompt

Agents vary in how strictly they follow steps; your job is orchestration — intervene, test, commit.
When an agent drifts, re-prompt with the current checklist state and remind it of the steps.

```md
We are currently in stage <X> and have recently implemented the changes in `checklist.md`

For each unchecked item in the checklist:
1. Read the item.
2. Gather context (`project-rules.md`, `checklist.md`, relevant files).
3. Plan the edits.
4. Execute.
5. If backend-related, run a quick terminal test.
6. Mark the item complete & note decisions/bugs.
7. Repeat until checklist is done.
```