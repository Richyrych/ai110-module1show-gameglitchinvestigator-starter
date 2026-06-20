# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

1. If input is higher than secret value, user is told to GO HIGHER!  Should be told to go lower.

2. Once game is finished, the message instructs user to start a new game, however, clicking on "New Game" does not clear the current game.

3. If input is lower than secret, user is told to GO LOWER!  Should be told to go higher.



**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| 60|             GO LOWER  |GO HIGHER       |                         |
| 10|   GO HIGHER             | GO LOWER           |                   |
| Click "Start New Game"| Data is cleared, new game starts| no change | |

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

I used Claude Code directly in the IDE.  I referenced specific files
and tried to be as specific and intentional as I could.  I separated
instructions, but could have been better about that.  I Asked Claude
to fix the bugs in one command, whereas maybe I should have separated those instructiosn to reduce the chance for errors.
I also asked Claude to refactor and separate the logic from the state/UI and update the imports.  Claude found a few more bugs as well, like a discrepancy in which the number of attempts was intialized at 1 and elsewhere it was at 0.  
I verified the results with pytest, first Claude ran its own and then I ran one manually.  I found I had to add a conftest.py file 
in the root folder to run it.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?
I ran pytest, both with Claude and in my own terminal.
I also ran the application and used it and tested as a user.
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
Great questions.  I don't know that I got a deep understanding of streamlit specifically here.  From what I saw, the session is not too different from express or other web-based session in which state is maintained and modified based on user input.  The UI functions manipulate the state directly, and they call on the backend logic to decide what to do with the state. 
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
I absolutely will be more specific and intentional in how I prompt the agent in checking for bugs.
Next time I use AI in a project, I will do better to separate commands and prompts to focus on one specific task at a time.