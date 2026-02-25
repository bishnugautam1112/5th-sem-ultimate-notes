


Here is the optimized, ultra-efficient note for **2024 Q1b**. I have stripped away the fluff so you only memorize what gets you marks.

---

### **2024 Q1 b) What is PEAS? Explain the architecture of reflex and goal-based agents with an example such as a vacuum cleaning agent.**

#### 📝 High-Yield Exam Note (Write this to get full marks)

**1. What is PEAS?**
PEAS is a framework used to design and describe an AI agent's working environment. 
*   **P**erformance Measure: How we judge the agent's success (e.g., amount of dirt cleaned, electricity saved).
*   **E**nvironment: Where the agent operates (e.g., room, floor, obstacles).
*   **A**ctuators: The parts it uses to take action (e.g., wheels, vacuum motor, brushes).
*   **S**ensors: The parts it uses to perceive the environment (e.g., dirt sensor, bump sensor).

**2. Simple Reflex Agent (Architecture & Example)**
*   **Concept:** It acts *only* based on the current percept (what it sees right now). It has no memory and ignores the past. It uses **Condition-Action (IF-THEN)** rules.
*   **Architecture Flow:** `Sensors -> What is the world like now? -> Condition-Action Rules -> What action I should do now? -> Actuators`
*   **Vacuum Example:** 
    *   *Rule:* **IF** current square is dirty **THEN** suck dirt. 
    *   *Rule:* **IF** current square is clean **THEN** move right. 
    *   *(It doesn't remember if it already cleaned the right side).*

**3. Goal-Based Agent (Architecture & Example)**
*   **Concept:** It acts to achieve a specific **Goal**. It keeps track of the world (state/memory) and considers the *future consequences* of its actions before acting ("What will happen if I do this?").
*   **Architecture Flow:** `Sensors -> State/Model of the world -> What will my action do? -> GOALS -> Action selection -> Actuators`
*   **Vacuum Example:** 
    *   *Goal:* "Make the whole house 100% clean."
    *   *Action:* It remembers a map of the house, knows which rooms are already clean, and plans a path to the dirty rooms without wandering randomly.

---

### 🧠 Core Concept Guide (Romanized Nepali + English)

**Concept bujhne tarika (How to remember in 1 minute):**

*   **PEAS vaneko k ho?:** Kunai pani AI lai job dida dine "Job Description" ho. K kaam garne (Performance), kaha garne (Environment), k le garne (Actuator), ra kasari tha paune (Sensor). 
*   **Reflex Agent (Bina soche react garne):** Yo dimag nabhayeko agent ho. J dekhxa tei garxa.
    *   *Example:* Tatto kura choyo vane haat paxi tanxau ni? Tyo reflex ho. Vacuum le fohor dekhyo -> taanyo. Teti matra. Agadi paxi k xa baal matlab hudaina. **Keyword:** *IF-THEN rule*.
*   **Goal-Based Agent (Plan garera kaam garne):** Yo ali smart hunxa. Yeslai aafno "Target" (Goal) tha hunxa ra yesle past memory pani rakhxa.
    *   *Example:* Bato ma hidda aafno destination (Goal) tha payera map herera hidne manxe. Vacuum le purai ghar ko map banauxa, fohor vako thau ma matra janxa, euta thau 2 choti jadaina. **Keyword:** *Future consequence & Target*.

---
