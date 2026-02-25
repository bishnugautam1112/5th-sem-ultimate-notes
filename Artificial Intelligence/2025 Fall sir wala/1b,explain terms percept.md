Here is the **"Slay" Material for 2025 Q1b**. This question is the "vocabulary" of AI. If you get these terms right, the examiner knows you understand the foundation.

---

### **2025 Q1 b). Explain the terms—agent, percept, percept sequence, agent function and agent program with example of vacuum-cleaner agent. (8 Marks)**

#### 📝 High-Yield Exam Note (Ultra-Efficient)

**1. Definitions:**
*   **Agent:** Anything that perceives its environment through **sensors** and acts upon that environment through **actuators**.
*   **Percept:** The agent's perceptual inputs at any given instant. (What the agent sees/feels *right now*).
*   **Percept Sequence:** The complete history of everything the agent has ever perceived from the start.
*   **Agent Function:** An abstract mathematical mapping that maps any given percept sequence to an action [$f: P^* \rightarrow A$]. It describes *what* the agent does.
*   **Agent Program:** The actual concrete implementation (the code) that runs on the physical architecture to produce the agent function.

**2. Example: Vacuum-Cleaner Agent**
Imagine a simple vacuum agent in a world with two rooms (A and B).
*   **Percepts:** `[Location, Status]` e.g., `[Room A, Dirty]`
*   **Percept Sequence:** `[[A, Clean], [A, Dirty], [B, Dirty]]` (The history of rooms it visited).
*   **Actions:** `Left`, `Right`, `Suck`, `NoOp` (Stop).
*   **Agent Function (The Logic):**
    *   If current status is **Dirty**, then **Suck**.
    *   If in **Room A** and clean, move **Right**.
    *   If in **Room B** and clean, move **Left**.
*   **Agent Program:** The actual Python or C++ code logic (If-Else statements) inside the vacuum's microchip that executes the above function.

---

### 🧠 Core Concept Guide (Romanized Nepali + English)

**Concept bujhne tarika (How to remember in 1 minute):**

*   **Agent (The Hero):** Jo environment ma basxa ani kaam garxa. (Manxe, Robot, software).
*   **Percept (Aankha le dekheko):** Yo moment ma k dekhiyo? (Current input).
*   **Percept Sequence (Purano yaad):** Suru dekhi aile samma k k dekhiyo? (History/Memory).
*   **Agent Function (Dimag ko Plan):** Yo condition vaye yo kaam garne vanne abstract logic. 
*   **Agent Program (Actual Code):** Function lai computer ma lekhda banne code. 
*   **Vacuum Example Trick:** 
    *   Khali dabba banaune (Room A, Room B).
    *   Dabba vitra fohor (Dirty) dekhaune.
    *   "Location" ra "Status" word use garne. Percept vaneko `[Kaha xa, kasto xa]` ho.

---

**Status:** 2025 Q1(b) ✅ Slayed!

Now, let's tackle a slightly tricky one: **2025 Q2a (A* Search escaping infinite loops)**. This is a "conceptual" question about A*. 

Type **"A-star"** to see how it avoids getting stuck!