My apologies! You are absolutely right. Let's finish the **2025 Q7 Short Notes** so you have everything organized.

---

### **2025 Q7. Writes short notes on: [Any two]**

#### **a) Learning Agent**
*   **Definition:** A Learning Agent is an AI agent that is capable of **improving its performance over time** based on its experiences. It is not explicitly programmed for every scenario but adapts and learns.
*   **Components:**
    1.  **Learning Element:** Responsible for making improvements by observing performance and proposing new rules/knowledge.
    2.  **Performance Element:** Selects actions (what the agent was originally designed to do).
    3.  **Critic:** Evaluates the agent's actions based on a performance standard and provides feedback to the Learning Element.
    4.  **Problem Generator:** Suggests exploratory actions that might lead to new and informative experiences.
*   **Mechanism:** It observes the outcomes of its actions, compares them to a performance standard, and uses the feedback to refine its knowledge base or action policies.
*   **Example:** A self-driving car learning to navigate new road conditions more effectively over time based on past driving data.

> **Concept (Nepali):** "Sikne Agent" vaneko tyo robot ho jasle aafno galti bata sikera aafai ramro kaam garna thalxa. Yesle purano experience lai use garera naya situation ma better decide garxa.

---

#### **b) Semantic Net and Frames**
*   **Semantic Net:**
    *   **Definition:** A graphical representation of knowledge using **nodes** and **labeled arcs (links)** to represent objects/concepts and their relationships.
    *   **Nodes:** Represent objects, concepts, or events (e.g., "Dog," "Animal," "Bark").
    *   **Links:** Represent relationships between nodes (e.g., "IS-A" (inheritance), "HAS-A" (part-whole), "CAN-DO").
    *   **Advantage:** Intuitive, easy to visualize, supports inheritance.
    *   **Example:** `Dog --IS-A--> Animal`; `Dog --HAS-A--> Tail`; `Dog --CAN-DO--> Bark`.
*   **Frames:**
    *   **Definition:** A data structure for representing a stereotyped situation. It's a collection of **slots** and their **fillers**.
    *   **Slots:** Attributes or properties of an object/concept (e.g., "Name," "Color," "Size").
    *   **Fillers:** The specific values for those attributes (e.g., "Labrador," "Brown," "Medium").
    *   **Inheritance:** Frames can inherit slots and fillers from parent frames.
    *   **Example (for a "Car" frame):**
        *   Slot: `Type` (Filler: `Sedan`)
        *   Slot: `Wheels` (Filler: `4`)
        *   Slot: `Color` (Filler: `Red`)
    *   **Advantage:** Organizes knowledge hierarchically, provides default values, good for representing typical situations.

> **Concept (Nepali):**
> *   **Semantic Net:** Dimag ko "Map" jastai. Gol gol dabba (Nodes) haru ma kura haru rakhne, ani arrow (Links) le kun kura ko kun sanga sambandha xa vanera dekhaune. "Kukur" (Node) --> "IS-A" (Link) --> "Janawar" (Node).
> *   **Frames:** Euta template jastai ho. Jastai "Car" ko Frame ma "Color" ko slot, "Wheel" ko slot hunxa, ani tyo slot ma "Red" ya "4" vanne value halna milxa.

---

#### **c) Alpha-Beta Pruning**
*   **Definition:** Alpha-Beta pruning is an optimization technique used in **Minimax search algorithm** for game playing (e.g., Chess). It reduces the number of nodes evaluated in the search tree.
*   **Purpose:** To make the Minimax algorithm more efficient by **eliminating branches** that cannot possibly affect the final decision.
*   **Key Values:**
    *   **Alpha ($\alpha$):** The best (maximum) score that the MAX player can guarantee for itself so far, along the current path. Initialized to $-\infty$.
    *   **Beta ($\beta$):** The best (minimum) score that the MIN player can guarantee for itself so far, along the current path. Initialized to $+\infty$.
*   **Pruning Condition:** A branch is pruned (cut off) when **$\alpha \ge \beta$**. This means that if MAX can already guarantee a better score from another branch, MIN's current branch (which is trying to minimize the score) won't be chosen by MAX anyway.

> **Concept (Nepali):** Yo "Minimax" algorithm ko "Jugaad" ho. Jaba timi lai thaha hunxa ki yo bato bata ramro result audaina, tyo bato ko agadi ko part check nai nagari "Kaaatdine" (prune garne). Timro "alpha" (MAX ko best score) timro opponent ko "beta" (MIN ko best score) vanda thulo vayo vane "Kaaatde".

---

### **🎉 FINAL CONFIRMATION!**
You now have **ALL** the requested notes from **2023, 2024, and 2025** sets, including the short notes.

**You are fully equipped.** Go conquer that exam!