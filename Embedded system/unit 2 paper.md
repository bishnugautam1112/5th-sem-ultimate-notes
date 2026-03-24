Here is the properly formatted, clean, and highly readable version of your exam syllabus breakdown. I have organized it into structured tables so you can easily track the probability, frequency, and sources of each question for your exam preparation.

---

### **Syllabus 2.1 — Overview of AVR Architecture**
| Q.No | Exam Question | Board | Pre-Board | Prob. | Source (Exam/Year) |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **1** | Describe the architecture of the AVR (ATmega32) microcontroller with a neatly labeled block diagram. Highlight the key features of its architecture. | 3/3 | 5/6 | **81%** | PU F24·Q1b, NEC·Q1b, PU Int·Q1b, Everest·Q1a, NCIT·Q2a, Universal·Q2a, MB·Q2a |
| **2** | Explain the key features of AVR architecture with a figure. Include the role of General-Purpose Registers, ALU, Program Counter, and Watchdog Timer in AVR. | 1/3 | 2/6 | **81%** | NCIT 2025·Q2a, MB 2026·Q2a *(Overlaps with Q1)* |
| **3** | What are the key factors a programmer needs to consider when choosing a general-purpose controller? | 0/3 | 1/6 | **19%** | Gandaki Fall 2025·Q2b |

---

### **Syllabus 2.2.1 / 2.2.2 — Intro to C + Data Types, Control Structures, Pointers**
| Q.No | Exam Question | Board | Pre-Board | Prob. | Source (Exam/Year) |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **4** | What are the main differences between standard C and Embedded C? What is Data types in Embedded C? | 0/3 | 1/6 | **19%** | Universal Engineering 2025·Q2b |

---

### **Syllabus 2.2.3 — Memory Management**
| Q.No | Exam Question | Board | Pre-Board | Prob. | Source (Exam/Year) |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **5** | Write a program to store and retrieve a value from the EEPROM memory of an AVR microcontroller. | 1/3 | 2/6 | **36%** | PU Internal 2025·Q2b, MB 2026·Q2b_OR |
| **6** | Discuss how memory is managed in Embedded C for AVR microcontrollers. Explain with C code and a circuit diagram. | 0/3 | 1/6 | **36%** | NCIT Fall 2025·Q2b |

---

### **Syllabus 2.2.4 — AVR Interrupt Handling**
| Q.No | Exam Question | Board | Pre-Board | Prob. | Source (Exam/Year) |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **7** | Explain the process involved in interrupt handling in AVR. | 1/3 | 0/6 | **35%** | PU Spring 2025·Q2a |
| **8** | Explain interrupt handling in AVR microcontrollers. Differentiate between polling and interrupt-driven I/O with suitable examples. | 1/3 | 0/6 | **35%** | PU Internal 2025·Q2a |

---

### **Syllabus 2.2.5 — Input and Output Ports Interfacing on AVR**
| Q.No | Exam Question | Board | Pre-Board | Prob. | Source (Exam/Year) |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **9** | Write a program to toggle the LEDs connected to PORTD of the ATmega32. Include a properly labeled diagram. <br><br>**OR:** Write a program — LEDs ON when switch pressed, OFF when released. Include labeled diagram. | 2/3 | 2/6 | **54%** | PU F24·Q2a, NEC·Q2a, PU F24 OR variant |
| **10** | Write a simple Embedded C program to blink an LED connected to PORTB pin 0 of an AVR microcontroller. | 0/3 | 1/6 | **54%** | MB 2026·Q2b |
| **11** | Explain input and output ports interfacing on AVR. | 0/3 | 1/6 | **54%** | Gandaki Fall 2025·Q2a |

---

### **Syllabus 2.2.6 — Timers and Counters in AVR** *(High Priority)*
| Q.No | Exam Question | Board | Pre-Board | Prob. | Source (Exam/Year) |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **12** | Write a program — LED blinks using Timer0 in Normal mode. Generate 1-second delay. Show complete delay calculation. Include circuit diagram. | 2/3 | 2/6 | **62%** | PU F24·Q5b, NEC 2026·Q5b *(identical)* |
| **13** | Write an AVR program in C to generate a square wave using Timer0 and Timer1. Also mention circuit diagram. | 2/3 | 1/6 | **62%** | PU F24·Q2b, NCIT 2025·Q2b_OR |
| **14** | Write a program to create a square wave of 50% duty cycle on the PORTB.5 bit. Use Timer to generate time delay. | 1/3 | 1/6 | **62%** | PU Spring 2025·Q2b |
| **15** | What is the difference between counter and timers in AVR? Write an ALP to generate a square wave of 50% duty cycle using polling. | 0/3 | 1/6 | **62%** | Everest Fall 2025·Q2a |
| **16** | *(Short Note)* Timer and Counters of AVR microcontroller. | 2/3 | 0/6 | **62%** | PU F24·Q7a, NEC·Q7a |

---

### **Syllabus 2.2.7 — Serial Communication in AVR**
| Q.No | Exam Question | Board | Pre-Board | Prob. | Source (Exam/Year) |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **17** | Explain the concepts of UART. Write a program to display "Hello World" on UART with default configuration (9600 baud, 8-bit, 1 stop bit). | 1/3 | 1/6 | **54%** | NEC 2026·Q2b *(PU F24·Q5a for UART frame — Unit V)* |
| **18** | How is serial communication achieved in AVR? Write a program in ATmega32 to receive bytes of data serially → Port B. Baud 9600, 8-bit, 1 stop bit. Use interrupt instead of polling. | 0/3 | 1/6 | **54%** | Everest Fall 2025·Q2b |
| **19** | **(OR)** Write a program in ATmega32 to receive bytes serially → Port A. Baud 9600, 8-bit, 1 stop bit. | 1/3 | 0/6 | **54%** | PU Spring 2025·Q2b_OR |