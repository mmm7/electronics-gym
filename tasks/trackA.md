# Track A

## Chapter 1: Analogue Circuits
Tasks:

1. LED: "Hanging" wire: when connected to +5V, LED is on, when connected to 0V, LED is off.
2. LED+button: LED is on while button is pressed.
3. LED+button: LED is off while button is pressed.
4. Alternating LEDs: 2 LEDs, when button is pressed, LED-1 is on, LED-2 is off, when button is released, LED-1 is off, LED-2 is on.

## Chapter 2: From Analogue to Digital
Levels:

*  Logical low = binary 0 = 0V
*  Logical high = binary 1 = +5V

Tasks:

1. Logical inverter from transistors.
1. 2-input NAND gate from transistors.
1. 2-input OR gate from transistors.
1. 2-input AND gate from transistors.
1. 4-input NAND gate from transistors.
1. 4-input OR gate from transistors.

## Chapter 3: Timing

1. RC Delay: LED lights up ~0.5s after pressing a button (and keeping it pressed).
1. Monostable Multivibrator 1: At every button-press, a LED lights up for ~1s (no matter how log the button is pressed).
2. Retriggerable one-shot Multivibrator: LED lights up when button is pressed. LED remains on for ~2s after the button is released. If the butting is pressed again, the timer resets. 

## Chapter 4: State

### RS

RS flip-flop from transistors.
*  R=reset
*  S=set
*  Q=output

| S (input) | R (input) | Q (output) |
|:---------:|:---------:|:----------:|
| 1         | 0         | 1          |
| 0         | 1         | 0          |
| 0         | 0         | hold       |
| 1         | 1         | undefined  |

### Bistable Multivibrator

Build a circuit (form transistors, capacitors and resistors) that makes 2 LEDs blink in opposite states at ~1Hz.

[Solution](https://www.instructables.com/Simple-Blinking-LED-Circuit/)

## Chapter 5: Edge Detection

🠕 denotes *rising edge*.

🠗 denotes *falling edge*.

### Edge triggered RS flip-flop

* Build an Edge triggered RS flip-flop from transistors

| Clock (clk) | S (input) | R (input) | Q (output) |
|:-----------:|:---------:|:---------:|:----------:|
| 🠕           | 1         | 0         | 1 (set)    |
| 🠕           | 0         | 1         | 0 (reset)  |
| 🠕           | 0         | 0         | Q (hold)   |
| 🠕           | 1         | 1         | undefined  |
| X           |           |           | hold       |

*  Build the same RS flip-flop triggered by **falling** edge (instead of rising).

### Edge triggered JK flip-flop

* Build an Edge triggered JK flip-flop from transistors. JK is very similar
  to RS, but if both inputs being high means **toggle** (instead of invalid).

| Clock (clk) | J (input) | K (input) | Q (output) |
|:-----------:|:---------:|:---------:|:----------:|
| 🠕           | 1         | 0         | 1 (set)    |
| 🠕           | 0         | 1         | 0 (reset)  |
| 🠕           | 0         | 0         | Q (hold)   |
| 🠕           | 1         | 1         | !Q (toggle)|
| X           |           |           | hold       |

### Edge triggered D flip-flop

* Build an Edge triggered D flip-flop from transistors. D flip-flops "store"
  a single ("data") bit. There is only 1 input: D.

| Clock (clk) | D (input) | Q (output) |
|:-----------:|:---------:|:----------:|
| 🠕           | 1         | 1 (set)    |
| 🠕           | 0         | 0 (reset)  |
| X           |           | hold       |

## Chapter 6: Bit by bit

### Counter

* Build a 3-bit counter (with reset input) from transistors.

| Clock (clk) | RST (input) | (C,B,A) (output)            |
|:-----------:|:-----------:|:---------------------------:|
| 🠕           | 0           | 0,0,0 (reset to 0)          |
| 🠕           | 1           | (C,B,A)+1 (increment)       |
| X           |             | (C,B,A) (hold)              |

The counter has 3 outputs (3 bits). It cycles through the states:

`(0,0,0) -> (0,0,1) -> (0,1,0) -> (0,1,1) -> (1,0,0) -> (1,0,1) -> (1,1,0) -> (1,1,1)`

* Modify 3-bit counter to a 3-bit *5-counter*.

The 5 counter has 5 state, cyscles through the follwing states:

`(0,0,0) -> (0,0,1) -> (0,1,0) -> (0,1,1) -> (1,0,0)`

Use the reset input.

### Shift-register

* Build a 3-bit 1-directional shift-register (from transistors).

SI: Serial Input

| Clock (clk) | SI (input)  | C   | B   | A   |
|:-----------:|:-----------:|:---:|:---:|:---:|
| 🠕           | 0           | B   | A   | 0   |
| 🠕           | 1           | B   | A   | 1   |
| X           |             | C   | B   | A   |

## Chapter 7:

Coming soon... stay tuned.
