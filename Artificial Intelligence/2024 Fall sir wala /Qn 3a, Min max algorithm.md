


Here is the **"Slay" Material for 2024 Q3a**. This is a combination of theory and game-tree numerical. The pruning logic here is super satisfying once you get it!

---

### **2024 Q3 a) What is the idea of Mini-Max search algorithm? Explain how alpha-beta pruning works with reference to the following game tree. Assume the root node is MAX.**

#### 📝 High-Yield Exam Note (Write this to get full marks)

**1. Idea of Mini-Max Search Algorithm:**
Mini-Max is an adversarial search algorithm used in game theory (like Chess or Tic-Tac-Toe). It computes the best possible move by assuming the opponent is also playing optimally. 
*   **MAX** player tries to get the highest possible score.
*   **MIN** player tries to get the lowest possible score.
*   The algorithm builds a complete game tree and propagates values from the bottom (leaves) to the top (root).

**2. How Alpha-Beta Pruning Works:**
Alpha-Beta pruning is an optimization technique for the Mini-Max algorithm. It avoids searching branches of the tree that cannot possibly influence the final decision, thus saving time.
*   **Alpha ($\alpha$):** The best (highest) value that MAX can guarantee so far. (Initial = $-\infty$)
*   **Beta ($\beta$):** The best (lowest) value that MIN can guarantee so far. (Initial = $+\infty$)
*   **Pruning Condition:** If at any node **$\alpha \ge \beta$**, stop searching its children and **Prune** the rest of the branch!

**3. Tracing the Given Game Tree:**
*   **Step 1 (Node D):** D is MAX. It looks at leaves 6 and 8. $D = \max(6, 8) = 8$. 
    *   Node B (MIN) now knows it can get at least an 8. So, $\beta$ for B becomes **8**.
*   **Step 2 (Node E):** E is MAX. It looks at the first leaf **9**. So E will be $\ge 9$. 
    *   But B is a MIN node and already has an option of **8**. B will never choose E (since $9 > 8$). 
    *   *Action:* **Prune the leaf '2' under E!** E returns 9, but B ignores it.
*   **Step 3 (Node F):** F is MAX. It looks at 1, then 10. $F = \max(1, 10) = 10$. B ignores it ($10 > 8$). 
    *   Node B returns **8** to Root Node A. 
    *   Root A (MAX) updates its **$\alpha = 8$**.
*   **Step 4 (Node C - Right Side):** A moves to the right branch. C is MIN.
    *   First, Node G (MAX) looks at leaves 4 and 5. $G = \max(4, 5) = 5$.
    *   Node C (MIN) updates its $\beta$ to **5**.
*   **Step 5 (Massive Pruning):** 
    *   Now, Root A (MAX) already has a guaranteed score of **8** from the left side ($\alpha = 8$).
    *   Node C (MIN) will return at most **5** ($\beta = 5$). 
    *   Since $\alpha \ge \beta$ ($8 \ge 5$), Root A will *never* choose the right path C. 
    *   *Action:* **Prune the entire nodes H and I (and their leaves 2, 3, 11, 12)!** They are completely ignored.

**Final Answer:** The optimal value at Root Node A is **8**.
*(Exam trick: Lightly cross out the pruned nodes '2', 'H', 'I', and their leaves with a pencil in your answer sheet diagram).*

---

### 🧠 Core Concept Guide (Romanized Nepali + English)

**Concept bujhne tarika (How to remember in 1 minute):**

*   **Mini-Max vaneko k हो?:** Dui jana ko fight ho. "MAX" aafno faida sochni, "MIN" aarko ko ghata garauni. Tala bata mathi value landa MAX node ma thulo number rakhne, MIN node ma sano number rakhne.
*   **Alpha-Beta Pruning Trick:** "Faltu kaam nagarne!" 
    *   Imagine you are MAX (A). You already found a path (Node B) that gives you **8 rupees**. 
    *   Now you check the other path (Node C). C's first option (Node G) says "I will only give you **5 rupees**". Since C is your enemy (MIN), they might give you even less than 5 later, but they will *never* give you more than 5. 
    *   Since you already have an 8-rupee guarantee from B, why will you even look at the rest of C's options? You just say "I don't care" and **Prune** (kaatdine) H and I. Yo step le marks fully tanxa! 
*   **Rule of Thumb:**
    *   $\alpha$ vaneko MAX le paune minimum guarantee.
    *   $\beta$ vaneko MIN le dine maximum guarantee.
    *   Jaba $\alpha$ ra $\beta$ cross hunxa ($\alpha \ge \beta$), tya bata aghi nabadhne.

---

**Status:** 2024 Q3(a) ✅ Slayed! The pruning diagram will fetch you 7 easy marks.

Let's move to **2024 Q3b (Knowledge Representation & Predicate Logic)**. Ready to translate English into AI Math?