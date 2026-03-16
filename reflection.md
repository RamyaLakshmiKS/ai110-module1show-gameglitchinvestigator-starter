# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- When I first ran the game, the user interface was confusing because it did not match the actual game logic. The most obvious bug was that the hints were completely reversed, telling me to go higher when I actually needed to go lower. Additionally, the sidebar showed a different number of allowed attempts than the main screen, and the "attempts left" counter updated inconsistently as I played. This created a frustrating and confusing experience right out of the gate.

---

## 2. How did you use AI as a teammate?

- I primarily used GitHub Copilot as my AI teammate for this project to help speed up my workflow. One helpful thing it did was accurately generate the boilerplate code for the tests I needed based directly on my instructions. However, it was a bit misleading because it only did exactly what I explicitly prompted, without anticipating edge cases or offering proactive architectural improvements. It essentially acted like a very fast typist rather than a strategic brainstorming partner.

---

## 3. Debugging and testing your fixes

- To verify my bugs, I combined manual playtesting with automated testing. I manually played through the game multiple times to visually confirm the attempt counter decreased correctly and the hints pointed in the right direction. I also relied on GitHub Copilot to help me write test cases that checked the check_guess function with various inputs. Running these tests proved to me that the logic now correctly handles scenarios where the guess is too high, too low, or exactly matches the secret number.
---

## 4. What did you learn about Streamlit and state?

- In the original app, the secret number kept changing because Streamlit reruns the entire script from top to bottom every time a user clicks a button or types an input. You can think of Streamlit like a restaurant kitchen that cooks your entire meal from scratch every time you ask for an extra napkin, unless you use a special memory locker called "session state". I fixed the changing number by adding logic that only generates a new secret when the current_difficulty changes or a new game starts, safely storing that value in the session state. In a real-world business application, mastering this concept is crucial for keeping user shopping carts or multi-step checkout forms intact without losing data on every single click.

---

## 5. Looking ahead: your developer habits

- One valuable habit I plan to carry forward into my upcoming software engineering interviews is writing automated tests to verify my logic before assuming it works. Next time I work with AI, I want to try asking more open-ended questions to see if it can help me design better overall solutions, rather than just using it to type out my exact commands. Ultimately, this project taught me that AI-generated code is a helpful starting point, but it still requires a human engineer to thoroughly review, test, and guarantee it is actually safe for production.
