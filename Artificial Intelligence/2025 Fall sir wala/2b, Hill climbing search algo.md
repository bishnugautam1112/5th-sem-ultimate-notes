Here is the **"Slay" Material for 2025 Q2b**. This is a high-frequency, purely conceptual question. It is incredibly easy to understand and score full marks if you draw the three diagrams.

---

### **2025 Q2 b). Explain the concept of Hill-Climbing Search algorithm. What are the common problems associated with it? Explain in detail. (8 Marks)**

#### 📝 High-Yield Exam Note

**1. Concept of Hill-Climbing Search:**
Hill-Climbing is a heuristic search algorithm (often called greedy local search) used for mathematical optimization problems. 
*   **The Idea:** Imagine climbing a mountain while blindfolded. You evaluate your current position and take a step in the direction that goes *up* (increases the value or decreases the cost). 
*   **The Rule:** It only looks at its immediate neighbors and always moves to the neighbor with the best heuristic value. It does not maintain a search tree (no memory of past states), making it highly memory-efficient.
*   **Stopping Condition:** It stops when it reaches a "peak" where no neighbor has a higher value than the current state.

**2. Common Problems Associated with Hill-Climbing:**
Because it only looks locally and has no memory, Hill-Climbing suffers from three major geographical problems that prevent it from finding the global optimum (the true highest peak).

*   **Problem 1: Local Maxima**
    *   *What it is:* A state that is better than all its immediate neighbors but is not the overall best state in the entire landscape (the Global Maximum).
    *   *The Issue:* The algorithm reaches the top of a small hill, sees that every step around it goes down, and falsely concludes it has reached the top of the entire mountain. It stops permanently.
*   **Problem 2: Plateau (Flat Local Maximum)**
    *   *What it is:* A flat area of the search space where all neighboring states have the exact same heuristic value as the current state.
    *   *The Issue:* The algorithm is unable to determine which direction to go because no step is "better." It wanders aimlessly or gets stuck in an infinite loop on the flat surface.
*   **Problem 3: Ridges**
    *   *What it is:* A sequence of local maxima that is higher than the surrounding areas but has a steep slope. The ridge itself slopes upwards, but the algorithm can only move along the axes (North, South, East, West).
    *   *The Issue:* Every single orthogonal step from the top of the ridge goes *down*. Therefore, the algorithm gets stuck, unable to zig-zag its way to the top of the ridge.

*(Exam Tip: You **MUST** draw a 2D line graph showing a small peak (Local Maximum), a flat line (Plateau), and the highest peak (Global Maximum). This diagram alone secures 4 out of the 8 marks).*

---

### 🧠 Core Concept Guide (Romanized Nepali + English)

**Concept bujhne tarika (How to remember in 1 minute):**

*   **Hill-Climbing (Aakha banda garera pahad chadhne):** Euta manxe aakha banda garera ukaalo lagdai xa. Usle mathi (high value) jane bato matra rojxa. Jaba uslai lagxa ki wari-pari sabai tira oralo xa, usle "Ma ta top ma puge" vanera tesaile rokinxa.
*   **3 ta thulo Samasya (Problems):**
    1.  **Local Maxima (Sano thumko):** Sano dada ko tuppo ma pugyo. Wari-pari sab oralo xa, tara tyo vanda thulo dada (Global Maxima) ali para thiyo. Tyo dekhdaina ra tei fasxa.
    2.  **Plateau (Tarai/Flat thau):** Yesto thau jaha aghi bade ni value same, paxi hate ni value same. Katai up-down nahuda kaha jane thaha navayera almalinxa.
    3.  **Ridge (Pahad ko dhar):** Dharilo dada jasto. Tya bata sidha agadi ya side ma janda sidhai tala khasinxa, tara zig-zag garera mathi jana milthyo, jaha Hill-climbing le step lina sakdaina.
*   **Exam Hack:** Graph banaune. Euta wave jasto line tanne. Sano wave lai "Local Maxima", bich ko flat line lai "Plateau", ra sab vanda thulo chuchho lai "Global Maxima" lekhdine. 

---

**Status:** 2025 Q2(b) ✅ Slayed! 

Now we face a choice for **2025 Q3**. It's the **Predicate Logic & Prolog Resolution** question (Twilight the Unicorn). 
It’s a classic, high-scoring logic conversion. Type **"Unicorn"** to translate English into AI math!