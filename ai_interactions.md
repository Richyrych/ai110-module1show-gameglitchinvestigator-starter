# AI Interactions Log

> **Stretch features only.** Only fill in the sections that apply to stretch features you attempted. If you did not attempt a stretch feature, leave its section blank or delete it. This file is not required for the core project.

---

## Agent Workflow (SF8)

I submitted a prompt to Claude to add a feature that will display 
the guess history to the user as an array on the UI, beyond the debug history (which did not update prooperly).

**What task did you give the agent?**

Here is the actual prompt:
    I want to implement a new feature in which the user can see the history of guesses within a game session.  There is a field for History on the UI, but nothing is displayed.  The user should see the state update with each guess, displaying the numerical choice as an array under History.  The array should clear and reset upon each rerun when a new game is started.

**What did the agent do?**

The agent said the plumbing is already in place, and created a helper function to render the history on the UI and prevent stale data.

**What did you have to verify or fix manually?**

It was a simple fix, I did not have to add manually but I did look at the files and confirm on the web app.
The agent modified app.py and added the helper function.
---

## Test Generation (SF7)

> Document how you used AI to help generate or improve tests.

| Edge Case | Prompt Used | AI-Suggested Test | Did It Pass? | Your Reasoning |
|-----------|-------------|-------------------|--------------|----------------|
| | | | | |
| | | | | |
| | | | | |

---

## Linting & Style (SF9)

> Document your use of AI for linting or code style improvements.

**Prompt used:**

```
<!-- Paste the prompt you gave the AI -->
```

**Linting output before:**

```
<!-- Paste relevant linter warnings/errors -->
```

**Changes applied:**

<!-- Describe what you changed based on the AI's suggestions -->

---

## Model Comparison (SF11)

> Compare two AI models on the same task.

**Task given to both models:**

<!-- Describe what you asked each model to do -->

| | Model A | Model B |
|-|---------|---------|
| **Model name** | | |
| **Response summary** | | |
| **More Pythonic?** | | |
| **Clearer explanation?** | | |

**Which did you prefer and why?**

<!-- Your conclusion -->
