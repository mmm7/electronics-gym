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

### Edge Detection
JK tároló tranzisztorból
D tároló tranzisztorból
3-bites számláló tranzisztorból
3-bites [output] shift-regiszter tranzisztorból

## Chapter 5:

Coming soon... stay tuned.
