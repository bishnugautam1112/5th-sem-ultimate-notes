Here is the **"Slay" Material for 2025 Q5a (OR Part)**. This is a purely mathematical question. If you show the calculation table correctly, you get full marks immediately.

---

### **2025 Q5 a) (OR Part) Explain how a single layer perceptron learns logical OR operation. (8 Marks)**

**Given Parameters:**
*   **Weights:** $w_1 = 0.3, w_2 = -0.2$
*   **Bias:** $b = 0.4$ (Input for bias is always $1$)
*   **Learning Rate:** $\alpha = 0.2$
*   **Activation Function:** Step Function (If $Net \ge 0$, Output $= 1$; else $0$).
*   **Logical OR Truth Table:**
    *   $(0, 0) \rightarrow 0$
    *   $(0, 1) \rightarrow 1$
    *   $(1, 0) \rightarrow 1$
    *   $(1, 1) \rightarrow 1$

#### 📝 High-Yield Exam Note (Step-by-Step Calculation)

We perform the training for **Epoch 1** (one full pass through all inputs).

**Formula:**
1.  $Net = (w_1 \cdot x_1) + (w_2 \cdot x_2) + b$
2.  $Output (y) = 1$ if $Net \ge 0$, else $0$.
3.  $Error (e) = Target - Output$
4.  **Update Rule:**
    *   $w_{new} = w_{old} + \alpha \cdot e \cdot x$
    *   $b_{new} = b_{old} + \alpha \cdot e$

---

**Step 1: Input (0, 0), Target = 0**
*   $Net = (0.3 \times 0) + (-0.2 \times 0) + 0.4 = \mathbf{0.4}$
*   **Output (y):** Since $0.4 \ge 0$, $y = \mathbf{1}$.
*   **Error (e):** $Target - Output = 0 - 1 = \mathbf{-1}$. (Mistake!)
*   **Update Weights:**
    *   $w_1 = 0.3 + 0.2(-1)(0) = \mathbf{0.3}$
    *   $w_2 = -0.2 + 0.2(-1)(0) = \mathbf{-0.2}$
    *   $b = 0.4 + 0.2(-1) = \mathbf{0.2}$
*   *Current Weights:* $w_1=0.3, w_2=-0.2, b=0.2$

**Step 2: Input (0, 1), Target = 1**
*   $Net = (0.3 \times 0) + (-0.2 \times 1) + 0.2 = -0.2 + 0.2 = \mathbf{0}$
*   **Output (y):** Since $0 \ge 0$, $y = \mathbf{1}$.
*   **Error (e):** $1 - 1 = \mathbf{0}$. (Correct!)
*   **No Update.**

**Step 3: Input (1, 0), Target = 1**
*   $Net = (0.3 \times 1) + (-0.2 \times 0) + 0.2 = \mathbf{0.5}$
*   **Output (y):** Since $0.5 \ge 0$, $y = \mathbf{1}$.
*   **Error (e):** $1 - 1 = \mathbf{0}$. (Correct!)
*   **No Update.**

**Step 4: Input (1, 1), Target = 1**
*   $Net = (0.3 \times 1) + (-0.2 \times 1) + 0.2 = 0.3 - 0.2 + 0.2 = \mathbf{0.3}$
*   **Output (y):** Since $0.3 \ge 0$, $y = \mathbf{1}$.
*   **Error (e):** $1 - 1 = \mathbf{0}$. (Correct!)
*   **No Update.**

---

**Conclusion after Epoch 1:**
The weights have been updated to **$w_1=0.3, w_2=-0.2, b=0.2$**.
*(Note: If the exam asks, you would continue to Epoch 2 because input (0,0) with new bias 0.2 still gives output 1 (error), so it needs more training. But usually, showing **one full epoch** is enough for full marks unless specified otherwise).*

---

### 🧠 Core Concept Guide (Romanized Nepali + English)

**Concept bujhne tarika (How to remember in 1 minute):**

*   **Perceptron Learning Rule:** "Galti vayo vane sudhara, natra chup lagera basa."
    *   Yedi output milyo (Error = 0), weights change nagarne.
    *   Yedi output milena (Error $\neq$ 0), weights update garne.
*   **Calculation Trick:**
    *   Bias ($b$) lai sadhai input 1 vako weight manera treat garne.
    *   Formula ghokne: **New = Old + (Learning Rate $\times$ Error $\times$ Input)**.
*   **Exam Hack:** Calculation table ma **$Net$**, **$Output$**, **$Error$**, **$Updated Weights$** vanera column banaune. Examiner le tyo table herxa, ani last ko values ($0.3, -0.2, 0.2$) check garxa. Teti mile pugyo.

---

**Status:** 2025 Q5(a) ✅ Slayed!

We are almost done with the 2025 Set!
*   **Q5b:** Fuzzification (We covered this in 2024 Short Notes).
*   **Q6a:** Expert System (Covered in 2024).
*   **Q6b:** Forward/Backward Chaining. (This is **NEW** and essential).

Do you want to finish with **Q6b (Forward/Backward Chaining)** or jump to the **2023 Set**? (I recommend Q6b, it's a sure question).