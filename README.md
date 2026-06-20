# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
- [ ] Detail which bugs you found.
- [ ] Explain what fixes you applied.

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. Select a Difficulty
2. Select Show Hints- enable or disable
3. Enter a number and submit
4. If the guess in incorrect, follow the hint(if using) for the next guess
5. When the game is complete, select New Game

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

~/D/C/ai110-module1show-gameglitchinvestigator-starter main*
.venv ❯ pytest
========================== test session starts ===========================
platform linux -- Python 3.13.14, pytest-9.0.3, pluggy-1.6.0
rootdir: /home/richarddevitt/Documents/CodePath AI 110/ai110-module1show-gameglitchinvestigator-starter
plugins: anyio-4.13.0
collected 3 items                                                        

tests/test_game_logic.py ...                                       [100%]

=========================== 3 passed in 0.01s ============================


## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
