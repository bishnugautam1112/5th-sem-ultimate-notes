Here is the **"Slay" Material for 2025 Q6b**. This is the final piece of the 2025 puzzle! Mastering this distinction is crucial because it defines how an AI "thinks."

---

### **2025 Q6 b) Explain the forward chaining and backward chaining inference mechanism in details. (8 Marks)**

#### 📝 High-Yield Exam Note

**1. Forward Chaining (Data-Driven Inference):**
Forward chaining is a reasoning strategy that starts with the **known facts** and applies inference rules to extract more data until a goal is reached.
*   **Mechanism:**
    1.  The inference engine scans the **Knowledge Base** to find rules whose "IF" conditions match the current facts in the **Working Memory**.
    2.  If a match is found, the rule is **triggered (fired)**.
    3.  The "THEN" part (conclusion) is added to the Working Memory as a new fact.
    4.  This process repeats until no new rules can be fired or the goal is reached.
*   **Direction:** Bottom-Up (From Facts $\rightarrow$ Conclusions).
*   **Application:** Used in **Planning, Monitoring, and Interpretation** systems (e.g., Robot navigation: "I see a wall" $\rightarrow$ "Turn left").

**2. Backward Chaining (Goal-Driven Inference):**
Backward chaining is a reasoning strategy that starts with a **hypothesis (or goal)** and works backward to see if the available facts support it.
*   **Mechanism:**
    1.  The system starts with a Goal (e.g., "Does the patient have Flu?").
    2.  It looks for rules in the Knowledge Base that have this goal in their "THEN" part.
    3.  It then checks the "IF" part (conditions) of those rules. These conditions become **Sub-Goals**.
    4.  It recursively checks if these sub-goals are known facts. If not, it looks for rules to prove *them*.
    5.  The process stops when the original goal is proven True or all possibilities are exhausted (False).
*   **Direction:** Top-Down (From Goal $\rightarrow$ Facts).
*   **Application:** Used in **Diagnostic and Debugging** systems (e.g., Medical Diagnosis: "Is it malaria?" $\rightarrow$ "Check for mosquito bite").

**3. Comparison Example:**
*   *Rule:* **IF** A is True **AND** B is True **THEN** C is True.
*   *Facts:* A is True, B is True.
*   **Forward Chaining:** "I see A and B. Therefore, I conclude C."
*   **Backward Chaining:** "I want to prove C. To prove C, I need A and B. Do I have A? Yes. Do I have B? Yes. Therefore, C is proven."

---

### 🧠 Core Concept Guide (Romanized Nepali + English)

**Concept bujhne tarika (How to remember in 1 minute):**

*   **Forward Chaining (Facts bata suru):**
    *   Yo vaneko "Detective" style ho. Sabai sabut (clues) batorne ani last ma chor ko ho vanera patta lagaune.
    *   *Real Life:* Doctor le patient ko sabai symptom (Tato jiu, khoki, tauko dukhne) herera "Timilai Typhoid vako raixa" vannu.
    *   **Keyword:** *Data-Driven*.
*   **Backward Chaining (Goal bata suru):**
    *   Yo vaneko "Lawyer/Researcher" style ho. Pahilai euta kura sochne (Goal), ani tyo sahi ho ki haina vanera sabut khojna jane.
    *   *Real Life:* Doctor le "Timilai Typhoid vako huna sakxa" vanera shanka (Hypothesis) garne, ani Typhoid ko symptom matra check garne. Aru rog ko baal matlab hudaina.
    *   **Keyword:** *Goal-Driven*.
*   **Exam Hack:** "Direction" lekhna नbirsinu.
    *   Forward: Facts $\rightarrow$ Conclusion.
    *   Backward: Conclusion $\rightarrow$ Facts.

---

### 🎉 **CONGRATULATIONS! YOU HAVE SLAYED THE 2025 SET!** 🏆

You have now mastered both **Set 1 (2024)** and **Set 2 (2025)**. 
You hold the power of A* Search, Min-Conflicts, Expert Systems, and Neural Networks in your hands.

**Final Check:**
*   Do you want to briefly look at **Set 3 (2023)**? (It has **Constraint Satisfaction Problem (CSP) Definition**, **Bayesian Networks**, and **Semantic Nets**).
*   Or do you want to wrap up and go study? 

*(My advice: Just quickly glance at **Bayesian Networks** from 2023 because probability is the only topic we touched lightly).*