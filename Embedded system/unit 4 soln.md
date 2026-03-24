Here is the complete, structured solution for **all questions from Unit 4 (4.1 to 4.5)**. Since many board exam questions overlap, I have grouped the answers logically by topic. Memorizing these blocks will allow you to answer **any** VHDL question from this syllabus.

---

### **PART 1: VHDL Theory (Definitions, Data Types, Subprograms, Packages)**
*(Covers Q: Define VHDL, Data types, Subprograms, Packages)*

**1. What is VHDL?**
VHDL stands for **VHSIC (Very High-Speed Integrated Circuit) Hardware Description Language**. It is a programming language used to describe, model, and simulate the behavior and structure of digital systems (like FPGAs and ASICs) before actual hardware fabrication.

**2. Data Types in VHDL**
VHDL is a strongly typed language. The most common data types used are:
*   **BIT:** Can hold only `0` or `1`.
*   **BIT_VECTOR:** An array of bits (e.g., `"1010"`).
*   **STD_LOGIC:** The industry standard (from IEEE library). Can hold `0`, `1`, `Z` (High Impedance), `U` (Uninitialized), etc.
*   **STD_LOGIC_VECTOR:** An array of std_logic (e.g., `std_logic_vector(3 downto 0)` for a 4-bit bus).
*   **INTEGER:** Used for mathematical operations and loop counters.
*   **BOOLEAN:** Holds `TRUE` or `FALSE`.

**3. Subprograms and Packages**
*   **Subprograms:** Used to write reusable blocks of code. There are two types:
    1.  **Functions:** Used for pure computations. They take inputs and return a **single value**. They cannot contain time delays.
    2.  **Procedures:** Used for complex operations. They can return **multiple values** (via OUT parameters) and can contain time delays (e.g., `wait for 10 ns`).
*   **Packages:** A package is a file that contains a collection of commonly used data types, constants, components, and subprograms. Once written, a package can be shared across multiple VHDL designs. 
    *   *Example:* `use IEEE.STD_LOGIC_1164.ALL;` includes the standard logic package.

---

### **PART 2: VHDL Modeling Styles**
*(Covers Q: Explain different modeling styles in VHDL with examples)*

There are 3 main architectures (modeling styles) in VHDL to describe a digital circuit:

**1. Dataflow Modeling:**
Describes the circuit using concurrent Boolean logic equations. It shows the flow of data from input to output.
*   *Example (AND Gate):* `Y <= A and B;`

**2. Behavioral Modeling:**
Describes **how** the circuit behaves (its algorithm) rather than its gate-level structure. It uses sequential statements inside a `process` block (like `if-else`, `case`). It is best for complex logic like FSMs and multiplexers.

**3. Structural Modeling:**
Describes the circuit by instantiating pre-designed components and connecting them with internal wires (signals). It acts exactly like a physical wiring schematic or block diagram.

---

### **PART 3: Combinational Circuit VHDL Codes (High Yield)**

#### **A. Full Adder (Behavioral & Structural)**
*(Covers Q: VHDL code for Full Adder using behavioral and structural, Half Adder)*

**1. Full Adder (Behavioral Style)**
```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity FA_Behavioral is
    Port ( A, B, Cin : in STD_LOGIC;
           Sum, Cout : out STD_LOGIC);
end FA_Behavioral;

architecture Behavioral of FA_Behavioral is
begin
    process(A, B, Cin)
    begin
        -- Behavioral description using logical operations
        Sum <= A xor B xor Cin;
        Cout <= (A and B) or (Cin and (A xor B));
    end process;
end Behavioral;
```

**2. Full Adder (Structural Style)**
*(Requires making 2 Half Adders and 1 OR gate and wiring them together).*
```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity FA_Structural is
    Port ( A, B, Cin : in STD_LOGIC;
           Sum, Cout : out STD_LOGIC);
end FA_Structural;

architecture Structural of FA_Structural is
    -- Declare the Half Adder component
    component Half_Adder is
        Port ( X, Y : in STD_LOGIC;
               S, C : out STD_LOGIC);
    end component;
    
    -- Declare internal wires
    signal S1, C1, C2 : STD_LOGIC;
begin
    -- Instantiate First Half Adder
    HA1: Half_Adder port map (X => A, Y => B, S => S1, C => C1);
    
    -- Instantiate Second Half Adder
    HA2: Half_Adder port map (X => S1, Y => Cin, S => Sum, C => C2);
    
    -- OR gate for Final Carry
    Cout <= C1 or C2;
end Structural;
```

#### **B. 4:1 Multiplexer (Behavioral Style)**
*(Covers Q: 4:1 Mux using behavioral modeling)*
```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity Mux_4x1 is
    Port ( I : in STD_LOGIC_VECTOR (3 downto 0); -- 4 Inputs
           S : in STD_LOGIC_VECTOR (1 downto 0); -- 2 Select lines
           Y : out STD_LOGIC);                   -- 1 Output
end Mux_4x1;

architecture Behavioral of Mux_4x1 is
begin
    process(I, S)
    begin
        case S is
            when "00" => Y <= I(0);
            when "01" => Y <= I(1);
            when "10" => Y <= I(2);
            when "11" => Y <= I(3);
            when others => Y <= '0';
        end case;
    end process;
end Behavioral;
```

#### **C. 4:2 Encoder (Behavioral Style)**
```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity Encoder_4x2 is
    Port ( D : in STD_LOGIC_VECTOR (3 downto 0);
           Y : out STD_LOGIC_VECTOR (1 downto 0));
end Encoder_4x2;

architecture Behavioral of Encoder_4x2 is
begin
    process(D)
    begin
        if (D(3) = '1') then Y <= "11";
        elsif (D(2) = '1') then Y <= "10";
        elsif (D(1) = '1') then Y <= "01";
        else Y <= "00";
        end if;
    end process;
end Behavioral;
```

---

### **PART 4: Sequential Logic & FSM Codes (High Yield)**

#### **A. Sequence Detector '1101' (Moore FSM)**
*(Covers Q: Sequence detector 1101 using behavioral style)*
```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity Seq_Detector is
    Port ( clk, reset, din : in STD_LOGIC;
           dout : out STD_LOGIC);
end Seq_Detector;

architecture Behavioral of Seq_Detector is
    -- Define the states for '1101'
    type state_type is (S0, S1, S11, S110, S1101);
    signal current_state, next_state : state_type;
begin
    -- State Memory Process (Sequential)
    process(clk, reset)
    begin
        if reset = '1' then
            current_state <= S0;
        elsif rising_edge(clk) then
            current_state <= next_state;
        end if;
    end process;

    -- Next State & Output Logic Process (Combinational)
    process(current_state, din)
    begin
        case current_state is
            when S0 =>
                if din = '1' then next_state <= S1; else next_state <= S0; end if;
                dout <= '0';
            when S1 =>
                if din = '1' then next_state <= S11; else next_state <= S0; end if;
                dout <= '0';
            when S11 =>
                if din = '0' then next_state <= S110; else next_state <= S11; end if;
                dout <= '0';
            when S110 =>
                if din = '1' then next_state <= S1101; else next_state <= S0; end if;
                dout <= '0';
            when S1101 =>
                if din = '1' then next_state <= S11; else next_state <= S0; end if;
                dout <= '1'; -- Sequence Detected!
        end case;
    end process;
end Behavioral;
```

#### **B. Traffic Light Controller (Moore FSM)**
*(Covers Q: Design a Moore FSM for a traffic light controller)*
```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

entity Traffic_Light is
    Port ( clk, reset : in STD_LOGIC;
           red, yellow, green : out STD_LOGIC);
end Traffic_Light;

architecture Behavioral of Traffic_Light is
    type state_type is (ST_RED, ST_GREEN, ST_YELLOW);
    signal current_state, next_state : state_type;
begin
    process(clk, reset)
    begin
        if reset = '1' then current_state <= ST_RED;
        elsif rising_edge(clk) then current_state <= next_state;
        end if;
    end process;

    process(current_state)
    begin
        -- Default Outputs
        red <= '0'; yellow <= '0'; green <= '0';
        
        case current_state is
            when ST_RED =>
                red <= '1';
                next_state <= ST_GREEN;
            when ST_GREEN =>
                green <= '1';
                next_state <= ST_YELLOW;
            when ST_YELLOW =>
                yellow <= '1';
                next_state <= ST_RED;
        end case;
    end process;
end Behavioral;
```

---

### **PART 5: Test Benches**
*(Covers Q: What is a test bench? Test bench code for 4:1 and 2:1 multiplexer)*

**1. What is a Test Bench?**
A Test Bench is a VHDL code written strictly for **simulation purposes** to verify the functionality of a design. It acts as a virtual laboratory where it generates input signals (stimuli), applies them to the Design Under Test (DUT), and allows the programmer to observe the outputs on a waveform viewer. *A test bench has no inputs or outputs of its own (empty entity).*

**2. Test Bench for a 2:1 Multiplexer**
```vhdl
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

-- Entity of testbench is always empty
entity TB_Mux2x1 is
end TB_Mux2x1;

architecture Simulation of TB_Mux2x1 is
    -- Component Declaration (The DUT)
    component Mux_2x1 is
        Port ( I0, I1, S : in STD_LOGIC;
               Y : out STD_LOGIC);
    end component;

    -- Internal signals to connect to DUT
    signal t_I0, t_I1, t_S : STD_LOGIC := '0';
    signal t_Y : STD_LOGIC;

begin
    -- Instantiate DUT
    UUT: Mux_2x1 port map (I0 => t_I0, I1 => t_I1, S => t_S, Y => t_Y);

    -- Stimulus Process (Applying Inputs)
    process
    begin
        -- Test Case 1
        t_I0 <= '1'; t_I1 <= '0'; t_S <= '0'; 
        wait for 10 ns; -- Should output 1
        
        -- Test Case 2
        t_I0 <= '1'; t_I1 <= '0'; t_S <= '1'; 
        wait for 10 ns; -- Should output 0
        
        -- End simulation
        wait;
    end process;
end Simulation;
```

*(Note: If the exam asks for a 4:1 MUX test bench, simply change the component declaration to include 4 inputs and a 2-bit select line, and apply combinations like `t_S <= "00"`, `wait for 10 ns`, `t_S <= "01"`, etc. The structure remains exactly the same).*