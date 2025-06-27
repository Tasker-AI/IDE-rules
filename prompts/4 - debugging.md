# Debugging Prompt 1

```md
We are currently in stage <X> and have recently implemented the changes in `checklist.md`

While implementing <X> we have encountered the following error/problem:
<error message, description, logs>

We have already tried fixing it with the following approaches:
<What you have already tried and why it didnt work>

Please look at all the relevant context before proposing a plan how to fix this issue.
There is a high likelihood that part of the problem is that we have overcomplicated this. There is probably a very simple fix that requires taking a step back to find it.

Propose 3 approaches to fix the issue, and ask for any additional context, logs, or experiments that we can run to improve your guess.
Then choose the most likely reason for our problem and put it on top of your plan.
```

# Debugging Prompt 2

```md
Follow this structured sequence to solve <X> problem in <X> file(s):
1. Hypothesize Broadly – List 5-7 possible root causes, including edge cases, concurrency issues, and unexpected dependencies.
2. Distill with First Principles – Reduce the possibilities to 1-2 most probable sources based on known system behavior and past incidents.
3. Validate with Logs – Insert targeted logs to track transformations of key data structures and verify assumptions before modifying code.
4. Simulate Before Fixing – Where feasible, write small mock scenarios to replicate the issue in isolation.
5. Clarify Requirements – If the root cause relates to business logic, either ask for clarifications or list explicit assumptions before making changes.
```

# Debugging Prompt 3
```md
Follow this structured sequence to solve <X> problem in <X> file(s):

1. Figure Out the Symptoms
- The first step is to understand the symptoms of the bug. What
is the incorrect behavior? What errors are being reported? Take
time to digest the bug report and play around with the software
to replicate the issue.

2. Reproduce the Bug
- Reproduce the bug in a controlled environment. Start by 
reproducing it in the same environment where it was originally 
reported, and then reduce the steps to the minimum necessary to
trigger the bug. This helps in isolating the issue.

3. Understand the System
- Gain a thorough understanding of the system and its 
components. Knowing how different parts of the system interact 
can help you narrow down where the bug might be located.

4. Form a Hypothesis
- Based on your understanding, form a hypothesis about where 
the bug is located. Ask questions like which component or 
module might be causing the issue and whether it's related to 
interactions between components.

5. Test Your Hypothesis
- Test your hypothesis by validating input/output of the 
suspected component. Modify the code if necessary to get more 
information, such as adding debug logs. Ensure that any 
modifications do not hide the bug.
```