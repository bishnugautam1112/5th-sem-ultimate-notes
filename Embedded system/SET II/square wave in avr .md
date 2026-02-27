Here is the **exam-oriented solution** to generate a square wave using Timer 0 and Timer 1, designed to secure full marks. It is followed by the **Neplish explainer** to help you understand the core logic of AVR timers.

---

### **📝 Exam Solution: Square Wave Generation using Timer 0 and Timer 1 [7 Marks]**

**Concept:** 
The most efficient way to generate a continuous square wave in an AVR microcontroller (like ATmega16/32) is by using the **CTC (Clear Timer on Compare Match)** mode. In this mode, the timer automatically toggles a specific hardware pin (`OC0` for Timer 0 and `OC1A` for Timer 1) whenever the timer matches a predefined value, requiring zero CPU attention in the main loop.

**Hardware Pins Used:**
*   **Timer 0 Output:** `PB3` (OC0 pin)
*   **Timer 1 Output:** `PD5` (OC1A pin)

#### **AVR Embedded C Program:**

```c
#include <avr/io.h>

// Function to initialize Timer 0 for Square Wave
void Timer0_SquareWave_Init(void) {
    // 1. Set PB3 (OC0) as output pin
    DDRB |= (1 << PB3);
    
    // 2. Load the Compare Match value (Determines frequency)
    OCR0 = 127;  
    
    // 3. Configure TCCR0 (Timer/Counter Control Register 0)
    // WGM01 = 1: Select CTC Mode
    // COM00 = 1: Toggle OC0 on Compare Match
    // CS01=1, CS00=1: Prescaler = 64
    TCCR0 = (1 << WGM01) | (1 << COM00) | (1 << CS01) | (1 << CS00);
}

// Function to initialize Timer 1 for Square Wave
void Timer1_SquareWave_Init(void) {
    // 1. Set PD5 (OC1A) as output pin
    DDRD |= (1 << PD5);
    
    // 2. Load the 16-bit Compare Match value
    OCR1A = 15624;  // Example value for a specific low frequency
    
    // 3. Configure TCCR1A and TCCR1B (Timer 1 Control Registers)
    // COM1A0 = 1: Toggle OC1A on Compare Match
    TCCR1A = (1 << COM1A0);
    
    // WGM12 = 1: Select CTC Mode (Mode 4)
    // CS12 = 1: Prescaler = 256
    TCCR1B = (1 << WGM12) | (1 << CS12);
}

int main(void) {
    // Initialize both timers
    Timer0_SquareWave_Init();
    Timer1_SquareWave_Init();
    
    // Infinite loop
    while (1) {
        // The CPU does nothing! 
        // The hardware timers automatically generate the square waves 
        // on PB3 and PD5 completely in the background.
    }
    
    return 0;
}
```

**Explanation of Logic:**
1.  **CTC Mode (`WGM` bits):** The timer counts from 0 up to the value stored in the `OCR` (Output Compare Register). When it matches, it resets to 0 automatically.
2.  **Toggle on Match (`COM` bits):** Instead of manually writing code to turn the pin HIGH or LOW, the hardware is instructed to **Toggle** (flip from 1 to 0, or 0 to 1) the output pin every time the timer matches the `OCR` value. This creates a perfect 50% duty cycle square wave.
3.  **Prescaler (`CS` bits):** Divides the main CPU clock speed so the timer counts slower, allowing us to generate lower frequency waves.

---

### **💡 Neplish Explainer (Core Concept Bujhne Tarika)**

**Concept:** 
Timer haru lai use garera square wave nikalne bare sodheko ho. Square wave vaneko aadhi time ON (HIGH) ra aadhi time OFF (LOW) hune signal ho. 

**Kasari Samjhine? (Point-by-Point):**

1.  **CTC Mode (Sabai vanda important trick):**
    *   Timer lai euta target dinxa (e.g., `OCR0 = 127`).
    *   Timer le 0, 1, 2... gardai gancha. Jab 127 pugcha, tesle aafai pin lai ON bata OFF (wa OFF bata ON) banaidincha ra feri 0 bata ganna thalcha. 
    *   Yeslai **Toggle OC0 on Compare Match** vanxa. Yesle garda CPU purai free hunxa (`while(1)` bhitra kei lekhnai pardaina!).

2.  **Timer 0 ra Timer 1 ma k farak xa?**
    *   **Timer 0:** 8-bit ko ho. Yesle maximum **255** samma matra ganna sakcha. Yesko output pin **PB3 (OC0)** ho.
    *   **Timer 1:** 16-bit ko ho. Yesle **65,535** samma ganna sakcha (mathi code ma `15624` rakheko chau). Yesko output pin **PD5 (OC1A)** ho.

3.  **Registers Yaad Garne Tarika:**
    *   `DDR`: Pin lai output banaune. Square wave bahira pathauna output nai garna paryo.
    *   `OCR` (Output Compare Register): Target value set garne dabba.
    *   `TCCR` (Timer/Counter Control Register): Remote control jastai ho. Yesma **WGM** le mode (CTC) set garxa, **COM** le Toggle garxa, ra **CS** le prescaler (speed) set garxa.

**Exam Tips:** 
Exam ma thakkai yo code lekhyou vane check garne sir impress hunxa kina bhane dherai student le `_delay_ms()` use garera code lekhxan jun professional hudaina. Hardware Timer bata toggle garne tarika le 100% full marks fix auxa! 🚀