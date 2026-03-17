# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

- bug The hints are working oppisite.
  expected result : When the user guesses the number lower than the answer, hint should ask the user to go higher. When the user guesses the number higher than the answer, hint should ask the user to go lower. 

- bug : New Game Button Misbehaves (Does not start a new game after game completion)
  Expected : After completing a game, new game button doesnot start a new game

- bug : New Game Button Misbehaves (In middle of the running game)
  Expected : If user taps on new game in the middle of the game, it starts a new game, but the history of guesses is not cleared.

- bug : Difficulty Ranges Set incorrect. For normal difficulty, the range is set it 1, 100. For hard difficulty, the range is set to 1, 50 
  Expected : for range normal difficulty, the range must be 1 to 50, and for the hard difficulty the range must be 1 to 100

- bug: when difficulty is changed, the game is not updating
  Expected : When difficulty is changed, the game is should be reset to set difficulty.

- bug : At the start of the session, the attempts are set to 1.
  Expected : Attemps must be 0 at the start.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

- I used Copilot.
- One example where the AI suggestion was correct : It suggested me to change the logic for the input and submit button. It suggested me to use forms to correctly identify each input with out missing as this happened when user enters a number to guess and the second input is always missed.
- Sometimes the AI was suggesting to add code to change the UI design and add unncessary checks for inputs and also add extra logic. I avoided that.
---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
  I checked with my own inputs, confirmed after every step. For example, I fixed the logic to reset the game after changing the difficulty. I checked my changing the difficulty and verified with the valued that are being changed.

- Describe at least one test you ran (manual or using pytest)  
  After fixing the hint logic, I entered the numbers both that are higher and lower to verify if the hint is shown correctly

  and what it showed you about your code.
  It showed that my fis valid and working.

- Did AI help you design or understand any tests? How?
  It suggeested me to design a test case to check if the hint is working as intended. It suggested me go over both sides of the secret number.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
  I would say Streamlit reruns mean that every time the user clicks a button, types something, or changes a widget, Streamlit runs the script again from top to bottom. At first that felt confusing, because it looked like the app was restarting every time I interacted with it. Session state is what keeps important values, like score, secret number, attempts, and history, from getting lost during those reruns. So reruns refresh the app logic, while session state acts like memory that helps the app remember what was happening before the rerun.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  One habit I want to reuse is testing each fix right after making it instead of changing many things at once. That helped me see exactly which change solved a bug and whether a new problem was introduced. It made debugging much easier and saved time.

- What is one thing you would do differently next time you work with AI on a coding task?
  Next time, I would give more specific prompts and explain the bug more clearly before asking AI for help. I would also test each AI suggestion immediately instead of assuming it was correct. That would help me avoid extra changes that are not really needed.

- In one or two sentences, describe how this project changed the way you think about AI generated code.
  This project showed me that AI-generated code can be useful for finding ideas and speeding up debugging, but it should not be trusted without testing. I learned that I still need to check the logic carefully and make sure the code actually works in my app.
