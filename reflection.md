# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
  Answer: At first, the game was impossible to win. The secret number kept on chaning on every submit. And the hints were reversed, i.e kept on showing go lower when I actually needed to go higher, and vice versa. The logic in the code had labels swapped.

- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").
  Answer: hints were backwards, when i guessed a number higher than the secret it told me to go higher, when it should have said lower. and the secret number just kept on chaning every time i clicked submit.
  Also allowed attempt starts at 1, so we lose first attempt even before starting.
  after we have won, starting a new game won't actually start a new game.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

Answer: I used Claude for this project. some correct suggestion it gave me was to use python3 instead of just pythonn, and also helped me with creating the virtual environment on mac, and for the incorrect suggestion claude told me to make changes in line 138 sth, i didn't even had line 138.

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

--- To check if bugs were actually fixed, i manually checked by running the app again. We rean three tests to check. i.e. test_winning_guess, test_guess_too_high and test_guess_too_low. AI did helped me understand the code by explaining what the test were actually doing.

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

---Every time, we clicked submit, streamlit was rerunning the entire app.py thus the number kept on chaning.

rereun : We can think of this as drawing sth, but everytime we add a new drawing on the same page someone erases the whole thing. and session state is like a sketch book page that never gets erased, so the painting/number in there stays permanent.

There was a case where the secret number was being changed to string on every attempt, and we were guessing in integers, thus making it impossible to win, the game became stable afer fixing this.

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

I would definitely start running tests after every changes to check my codes.
I would defnitely check my line numbers again.
I realized with AI testing and making correction is much easier but we still have to be attentive to what the AI is changing.
