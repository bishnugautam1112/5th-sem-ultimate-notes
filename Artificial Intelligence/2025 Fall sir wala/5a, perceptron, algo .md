You are right! In the exam, Question 5a gives you a **CHOICE** (Theory vs. Numerical).

I just gave you the **Numerical (OR Gate)** solution.
Now, here is the **Theory Part** (First Option) in case you prefer writing steps over doing math.

---

### **2025 Q5 a) What is perceptron? Explain perceptron learning algorithm. (7 Marks)**

#### 📝 High-Yield Exam Note (Theory Option)

**1. Definition of Perceptron:**
A Perceptron is the simplest form of an Artificial Neural Network (ANN), developed by Frank Rosenblatt in 1957. It is a **single-layer neural network** used for **binary classification** (deciding if an input belongs to Class 0 or Class 1).
It consists of:
*   **Input Nodes ($x_1, x_2...$):** Receive data.
*   **Weights ($w_1, w_2...$):** Represent the strength of the connection.
*   **Bias ($b$):** Allows shifting the activation function.
*   **Activation Function:** Usually a Step Function (heaviside) to produce the output.

**2. The Perceptron Learning Algorithm (Step-by-Step):**
The goal is to find the correct weights ($w$) that can correctly classify the inputs.

*   **Step 1: Initialization**
    *   Set all weights ($w_1, w_2, ..., w_n$) and bias ($b$) to small random numbers (or zero).
    *   Set the learning rate $\alpha$ (usually between 0 and 1, e.g., 0.1).

*   **Step 2: Activation (Forward Pass)**
    *   For each training example $(x, Target)$, calculate the **Weighted Sum (Net Input)**:
        $$Net = \sum (w_i \cdot x_i) + b$$
    *   Apply the **Activation Function** (Step Function) to get the predicted Output ($Y_{out}$):
        *   If $Net \ge 0 \rightarrow Y_{out} = 1$
        *   If $Net < 0 \rightarrow Y_{out} = 0$

*   **Step 3: Weight Update (Backward Pass / Error Correction)**
    *   Calculate the Error: $Error = Target - Y_{out}$
    *   Update the weights and bias using the Delta Rule:
        *   $$w_{new} = w_{old} + \alpha \cdot Error \cdot x$$
        *   $$b_{new} = b_{old} + \alpha \cdot Error$$

*   **Step 4: Iteration**
    *   Repeat Steps 2 and 3 for all training examples (one full round is called an **Epoch**).
    *   Continue until the **Error is 0** for all examples or a specific number of epochs is reached.

---

### 🧠 Core Concept Guide (Romanized Nepali + English)

**Concept bujhne tarika (How to remember in 1 minute):**

*   **Perceptron:** Computer ko "Euta Cell wala Dimag". Yesle kura lai "Yes" or "No" ma matra xuttauna sakxa (Binary Classification).
*   **Learning Algorithm (Kasari Sikxa?):**
    1.  **Guess:** Suru ma hawa taal ma weight rakhxa.
    2.  **Check:** Input halera output nikalxa ($Net$ calculation).
    3.  **Compare:** Sahi answer (Target) sanga compare garxa.
    4.  **Correct:** 
        *   Yedi milena vane ($Error \neq 0$), weights lai ghataune ya badhaune garxa.
        *   Formula: $New = Old + (LearningRate \times Error \times Input)$.
    5.  **Repeat:** Sabai data namile samma gari rakhne.

---

**Status:** 2025 Q5(a) Both Options ✅ Slayed!

Now, the final unique question of 2025 is **Q6b (Forward vs Backward Chaining)**. This is very important because it wasn't in the 2024 set. 

Type **"Chaining"** to finish the 2025 set!