Here is the **exam-oriented solution** for Question 4(a), designed for the best length-to-marks ratio.

---

### **📝 Exam Solution: 4(a) VHDL Test Bench & Code for 2:1 MUX [7 Marks]**

#### **1. What is a VHDL Test Bench?**
A **Test Bench** is a VHDL program written to simulate and verify the functionality of a digital circuit (Design Under Test - DUT) without using physical hardware.
*   **Key Characteristic:** It has an **empty entity** (no input/output ports) because it is a self-contained simulation environment.
*   **Function:** It generates input signals (stimuli), applies them to the component, and monitors the output response to ensure the circuit works correctly.

#### **2. Test Bench Code for 2:1 Multiplexer**

*Assumption: The 2:1 MUX Entity has inputs `A`, `B`, `Sel` and output `Y`.*

```vhdl
LIBRARY ieee;
USE ieee.std_logic_1164.ALL;

-- 1. Entity Declaration (Always Empty for Test Bench)
ENTITY tb_mux21 IS
END tb_mux21;

-- 2. Architecture
ARCHITECTURE behavior OF tb_mux21 IS

    -- Component Declaration (The Unit to be Tested)
    COMPONENT MUX2to1
    PORT(
         A, B : IN  std_logic;
         Sel  : IN  std_logic;
         Y    : OUT std_logic
        );
    END COMPONENT;

    -- Signal Declaration (Wires to connect to the component)
    signal A_in   : std_logic := '0';
    signal B_in   : std_logic := '0';
    signal Sel_in : std_logic := '0';
    signal Y_out  : std_logic;

BEGIN
    -- 3. Instantiate the Unit Under Test (UUT)
    uut: MUX2to1 PORT MAP (
          A => A_in,
          B => B_in,
          Sel => Sel_in,
          Y => Y_out
        );

    -- 4. Stimulus Process (Apply Inputs)
    stim_proc: PROCESS
    BEGIN
        -- Test Case 1: Select A (Sel=0)
        A_in <= '1'; B_in <= '0'; Sel_in <= '0';
        wait for 100 ns;  -- Expect Y = 1 (A)

        -- Test Case 2: Select B (Sel=1)
        A_in <= '1'; B_in <= '0'; Sel_in <= '1';
        wait for 100 ns;  -- Expect Y = 0 (B)
        
        -- Test Case 3: Change inputs
        A_in <= '0'; B_in <= '1'; Sel_in <= '1';
        wait for 100 ns;  -- Expect Y = 1 (B)

        wait; -- Stop simulation
    END PROCESS;

END behavior;
```

---

### **💡 Neplish Explainer (Core Concept Bujhne Tarika)**

**Concept:**
Test Bench vaneko euta **Virtual Lab** ho. Jasari mobile kinna agadi pasal ma on garera check garinxha, tesari nai VHDL code (Hardware) lai chip ma halnu agadi software ma check garna Test Bench lekhinxha.

**Kasari Samjhine? (4 Steps Code Structure):**

1.  **Empty Entity:**
    *   Test bench aafai ma kunai device haina, yo euta environment ho. Tei vayera yesko entity ma `Port` hudaina. Just `ENTITY tb IS END tb;`.
2.  **Component Declaration:**
    *   Hamile jun MUX check garna lako ho, teslai "Bolako" (Declare gareko).
3.  **Signals (Taar Jodine):**
    *   MUX ko input/output lai drive garna internal signals (`A_in`, `B_in`...) banaune. Yo vaneko breadboard ma taar thika pareko jastai ho.
4.  **Stimulus Process:**
    *   Yo main part ho. `wait for 100 ns` lekhdai input change garne.
    *   Example: "Oye MUX, yedi Sel=0 chha vane A ko value pass gar ta!" vanera check gareko.

**Exam Tip:**
Code lekhda comments (`--`) use garera "Test Case 1", "Test Case 2" lekhyou vane, examiner le logic bujhxa ra full marks dinxa. `wait;` last ma lekhna nabirsine, natra simulation kahile rokidaina!