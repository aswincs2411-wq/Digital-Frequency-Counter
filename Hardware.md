# Hardware Documentation

## 1. Overview

The frequency counter is built using a combination of analog and digital integrated circuits. The hardware is divided into signal conditioning, timing, counting, and display sections.

## 2. Components Used

| Component | Quantity | Function |
|---|---:|---|
| NE555 | 1 | Generates the timing reference |
| LM393 | 1 | Converts the input signal into a square wave |
| CD4093 | 1 | Schmitt-trigger NAND logic |
| CD4026 | 2 | Decade counting and display driving |
| 7-Segment Display | 2 | Displays the measured frequency |
| Resistors | As required | Biasing and current limiting |
| Capacitors | As required | Timing and filtering |

## 3. Functional Blocks

### NE555 – Timing Reference

The NE555 timer is configured to generate an approximately 1 Hz timing signal. This signal provides the timing reference for the measurement process.

### LM393 – Input Signal Conditioning

The LM393 comparator processes the incoming signal and converts it into a digital square-wave signal suitable for the counting circuitry.

### CD4093 – Logic Circuit

The CD4093 contains four Schmitt-trigger NAND gates. It is used in the prototype's digital logic and signal-processing circuitry.

### CD4026 – Counting and Display

The CD4026 is a decade counter with an integrated seven-segment decoder. It counts incoming clock pulses and directly drives a seven-segment display.

## 4. Current Hardware Limitations

- The prototype exhibits an approximate positive measurement error of 8 Hz.
- The timing reference currently uses an NE555 timer.
- The display currently has two digits.

## 5. Planned Hardware Improvements

- Implement a crystal oscillator-based timing reference.
- Add a third seven-segment display.
- Improve measurement accuracy and stability.

---

**Development Status:** Prototype under development.
