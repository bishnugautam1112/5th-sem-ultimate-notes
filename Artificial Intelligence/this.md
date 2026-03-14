


Here are the "Ready-to-Write" exam notes for questions 1(a) and 1(b) from your question paper, followed by crystal-clear Neplish explanations to help you memorize them easily.

---

### **1. a) What is Artificial Intelligence? Mention the advantages of Artificial Intelligence. [8 Marks]**

**[Exam Ready Note]**

**Definition of Artificial Intelligence (AI):**
Artificial Intelligence (AI) is a prominent branch of computer science dedicated to creating intelligent systems capable of performing tasks that typically require human intelligence. These tasks include learning from experience, reasoning, problem-solving, understanding natural language, and perceiving the environment. 
According to Russell and Norvig, AI can be defined through four distinct approaches:
1. Thinking Humanly (Cognitive modeling)
2. Acting Humanly (Turing test approach)
3. Thinking Rationally (Laws of thought)
4. Acting Rationally (Rational agent approach - maximizing expected performance).

**Advantages of Artificial Intelligence:**
1. **Automation of Repetitive Tasks:** AI excels at performing monotonous, repetitive tasks without fatigue, freeing up humans to focus on creative and complex problem-solving.
2. **24/7 Availability:** Unlike humans who require rest, AI systems and machines can operate continuously 24 hours a day, 7 days a week, increasing overall productivity.
3. **Reduction of Human Error:** AI models, when programmed properly, can process vast amounts of data with high precision and accuracy, significantly reducing "human error" in fields like data entry and complex calculations.
4. **Handling Hazardous Tasks (Risk Mitigation):** AI-driven robots can be deployed in environments dangerous to humans, such as bomb disposal, space exploration, deep-ocean mining, or handling radioactive materials.
5. **Faster Decision Making:** AI can analyze massive datasets (Big Data) and extract patterns much faster than a human, enabling rapid decision-making in critical areas like algorithmic stock trading or medical diagnosis.
6. **Digital Assistance:** AI powers virtual assistants (like Siri, Alexa, or Chatbots) that provide highly personalized experiences and immediate customer support.

***

**💡 Nepali Core Concept Summary (Neplish):**
*   **AI bhanya k ho?** AI bhaneko computer science ko tyo branch ho jasle machine lai manxe jastai sochne, bujhne ra decision line banauna madat garcha. Exam ma definition lekhda 'Learning, Reasoning, ra Problem-solving' vanne words chutaunai hudaina. Russell ra Norvig ko 4 wota approach (Thinking/Acting Humanly/Rationally) lekhdyo bhane marks full aauxa!
*   **Faida (Advantages) k k hun ta?** 
    1. *Boring kaam aafai garne* (Automation). 
    2. *Thakai nalagne* (24/7 kaam garna sakne). 
    3. *Galti nagarne* (High accuracy, human error nahune). 
    4. *Danger thau ma pathauna milne* (Jastai bomb disarm garna robot pathaune). 
    5. *Chhito decision line* (Thulo data lai second mai process garne).

---

### **1. b) What are the criteria for the evaluation of search algorithms? Compare DFS and BFS.[7 Marks]**

**[Exam Ready Note]**

**Criteria for the Evaluation of Search Algorithms:**
To evaluate and compare the performance of different search algorithms, we use the following four standard criteria:
1. **Completeness:** Is the algorithm guaranteed to find a solution if at least one solution exists?
2. **Optimality:** If there are multiple solutions, is the algorithm guaranteed to find the best (optimal/lowest cost) solution?
3. **Time Complexity:** How long does it take for the algorithm to find a solution? (Usually measured by the number of nodes generated).
4. **Space Complexity:** How much memory (RAM) is required to perform the search? (Usually measured by the maximum number of nodes stored in memory at any point).

**Comparison Between DFS and BFS:**

| Feature | Breadth-First Search (BFS) | Depth-First Search (DFS) |
| :--- | :--- | :--- |
| **Basic Approach** | Explores the search tree level-by-level (shallowest nodes first). | Explores the search tree by diving deep down one path to the bottom before backtracking. |
| **Data Structure Used** | Uses a **Queue** (FIFO - First In, First Out). | Uses a **Stack** (LIFO - Last In, First Out). |
| **Completeness** | **Yes** (Complete if the branching factor is finite). | **No** (It can get stuck in infinite loops or infinitely deep paths). |
| **Optimality** | **Yes** (Optimal if all step costs are equal). | **No** (It might find a longer, sub-optimal path first). |
| **Time Complexity** | $O(b^d)$ (where $b$ is branching factor, $d$ is depth of shallowest solution). | $O(b^m)$ (where $m$ is the maximum depth of the search tree). |
| **Space Complexity** | $O(b^d)$ - **Very High**. It must store all nodes of a level in memory. | $O(bm)$ - **Very Low/Linear**. It only stores a single path from root to leaf node. |

***

**💡 Nepali Core Concept Summary (Neplish):**
*   **Evaluation Criteria:** Kunai pani search algorithm (bato khojne tarika) ramro cha ki nai vanera 4 wota kura ma test garincha:
    1. *Completeness:* Answer fix bhetaucha ki bhetaudaina?
    2. *Optimality:* Bhetayeko answer sabai bhanda best (chhoto bato) ho ki haina?
    3. *Time Complexity:* Kati time lagcha?
    4. *Space Complexity:* Kati memory/RAM khancha?
*   **BFS vs DFS Compare:** 
    *   **BFS (Breadth-First Search):** Yesle line-by-line (level wise) check garcha. **Queue** use garcha. Answer fix bhetcha (Complete) ra best answer bhetcha (Optimal). Tara sabai level ko data save garna parne vayekole **Memory ekdum dherai khancha** ($O(b^d)$).
    *   **DFS (Depth-First Search):** Yesle euta bato samatepachi tesko chheu sammai pugcha. **Stack** use garcha. Memory ekdum **kam khancha** ($O(bm)$). Tara yo baango-tingo bato ma fasna sakcha (Not complete) ra bhetayeko answer sabai bhanda best nahuna pani sakcha (Not optimal).


### **A* Search Algorithm (Short & Exam-Ready)**

**[Exam Ready Note]**

**Concept:** 
A* (A-star) is the most popular **Informed Search Algorithm**. It finds the shortest path by combining the actual cost taken so far with the estimated cost to reach the goal. 
It uses the evaluation function: **$f(n) = g(n) + h(n)$**
*   **$g(n)$**: Actual cost from the start node to the current node $n$.
*   **$h(n)$**: Heuristic (estimated) cost from the current node $n$ to the goal.
*   **$f(n)$**: Total estimated cost of the path through node $n$.

**Algorithm Steps:**
1.  **Initialize** two lists: 
    *   `OPEN` (Priority Queue to store unvisited nodes, sorted by lowest $f(n)$).
    *   `CLOSED` (List to store already visited nodes).
2.  Put the **Start Node** into the `OPEN` list.
3.  **Loop** while the `OPEN` list is not empty:
    *   **Pick** the node $n$ with the lowest $f(n)$ from `OPEN`.
    *   If $n$ is the **Goal Node**, return SUCCESS and trace back the path.
    *   Otherwise, remove $n$ from `OPEN` and put it in `CLOSED`.
    *   **Expand** node $n$ (generate its neighbors/successors).
    *   For each neighbor:
        *   Calculate its $f(n) = g(n) + h(n)$.
        *   If it is neither in `OPEN` nor `CLOSED`, add it to `OPEN`.
        *   If it is already in `OPEN` but with a higher cost, **update** it with this new lower cost.
4.  If `OPEN` becomes empty and the goal is not reached, return FAILURE.

***

**💡 Nepali Core Concept Summary (Neplish):**
*   **A* (A-star) Algorithm** sabai vanda best search technique ho. Yesle andha vayera bato khojdaina, formula lagaucha: **$f(n) = g(n) + h(n)$**.
*   **$g(n)$** bhaneko start point bata ahile ko thau samma aaudako actual kharcha (Past cost) ho. 
*   **$h(n)$** bhaneko ahile ko thau bata goal samma pugna kati lagla vanera guess gareko kharcha (Future cost/Heuristic) ho.
*   **Algorithm ko idea:** Duita list banaune (OPEN ra CLOSED). Suruma Start node lai OPEN ma halne. Tespachi OPEN list bata sabai vanda kam $f(n)$ (sasto bato) vako node nikalne. Yadi tyo goal ho vane sakkiyo! Haina vane tesko chhimeki (neighbors) haru ko $f(n)$ nikalne ra OPEN list ma halne. Yo process goal navetesamma repeat garirakhne.