Here is the **"Slay" Material for 2025 Q3b**. This is where you play "Detective" using Logic.

---

### **2025 Q3 b). Use resolution to prove "Twilight is magical".**

#### 📝 High-Yield Exam Note (Write this to get full marks)

**Step 1: Convert Facts to CNF (Conjunctive Normal Form)**
To use resolution, we must remove arrows ($\rightarrow$) using the rule: $A \rightarrow B \equiv \neg A \lor B$.

1.  **Fact 1:** $\forall x [Live(x) \rightarrow Magical(x)]$ *(We only need the 'Magical' part for this proof)*
    *   **CNF 1:** $\neg Live(x) \lor Magical(x)$
2.  **Fact 2:** $\forall x [Unicorn(x) \rightarrow Live(x)]$
    *   **CNF 2:** $\neg Unicorn(y) \lor Live(y)$ *(Used 'y' to avoid variable confusion)*
3.  **Fact 3:** $Unicorn(Twilight)$
    *   **CNF 3:** $Unicorn(Twilight)$

**Step 2: Negate the Goal**
*   **Goal:** Prove $Magical(Twilight)$
*   **Assumption:** Assume the goal is FALSE.
    *   **Negated Goal:** $\neg Magical(Twilight)$

**Step 3: The Resolution Proof (Step-by-Step Cancellation)**
We look for pairs of clauses that have opposite terms (e.g., $P$ and $\neg P$) and cancel them out.

1.  **Start with:** $\neg Magical(Twilight)$ *(Negated Goal)*
2.  **Resolve with CNF 1:** $(\neg Live(x) \lor Magical(x))$
    *   *Unify x = Twilight*
    *   *Cancel $\neg Magical$ and $Magical$*
    *   **Result A:** $\neg Live(Twilight)$
3.  **Resolve Result A with CNF 2:** $(\neg Unicorn(y) \lor Live(y))$
    *   *Unify y = Twilight*
    *   *Cancel $\neg Live$ and $Live$*
    *   **Result B:** $\neg Unicorn(Twilight)$
4.  **Resolve Result B with CNF 3:** $Unicorn(Twilight)$
    *   *Cancel $\neg Unicorn$ and $Unicorn$*
    *   **Final Result:** **EMPTY CLAUSE (NIL) / Contradiction** $\bot$

**Conclusion:**
Since we reached a contradiction (Empty Clause), our assumption that "Twilight is NOT magical" was wrong. Therefore, **"Twilight is magical" is PROVED.**

---

### 🧠 Core Concept Guide (Romanized Nepali + English)

**Concept bujhne tarika (How to remember in 1 minute):**

*   **Resolution vaneko k ho?:** "Kat-kuta parne" (Cancelling) game ho.
    *   Imagine math: If $x + y = 5$ and $-x = -2$, add them $\rightarrow y = 3$. Same logic here. Use negatives to cancel positives.
*   **Proof by Contradiction (Ulto sochne):**
    *   Hami lai prove garnu xa "Ram chor ho".
    *   Hami suru garxau: "Maandim Ram chor haina" (Assume Negation).
    *   Logic lagaudai jada last ma "Impossible" result aayo vane, hamro suru ko assumption galat thiyo. Tesaile Ram chor nai ho.
*   **CNF Rule:** Arrow ($\rightarrow$) lai hatauna agadi ko part ma **$\neg$ (Not)** thapne ra bich ma **$\lor$ (Or)** rakhne.
    *   $A \rightarrow B$ becomes $\neg A \lor B$.
*   **Exam Hack:** Last ma **"Empty Clause / Contradiction found"** lekhnai parxa. Tyo box (NIL) banaune bittikai sir le full marks dinxa.

---

**Status:** 2025 Q3(b) ✅ Slayed!

Now we are moving to **2025 Q4a (Min-Conflicts Algorithm & 4-Queen Problem)**. This is a *highly probable* question for tomorrow because it wasn't in the 2024 set.

Type **"Queens"** to solve the puzzle!