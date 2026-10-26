# Reverse-engineering notebook

## Board
- Device: M-VAVE FM-1 pocket synthesizer (user identification)
- PCB: DX7 MB V07, marking 260918
- Photos: both sides and multiple detail shots supplied in ChatGPT conversation, not yet checked into GitHub.

## Current architecture (functional hypothesis)
LiPo -> charging / protection / regulators -> JL audio SoC -> digital audio DAC -> amplifier -> output jacks.
JL SoC -> 74HC595 shift registers -> some LED outputs (routing unverified).
Controls, display, USB-C, and patterned copper electrodes connect through yet-to-be-traced circuitry.

**None of the arrows above represent a verified net.**

## Schematic sheet plan
1. Power and battery charging / protection
2. JL processor, clock, boot straps, reset, external memory
3. USB-C and programming / MIDI
4. Audio DAC, amplifier, and jacks
5. Display FPC
6. Rotary controls and buttons
7. Shift registers, LED matrix, patterned electrodes

## Net verification table
| Net ID | Pin A | Pin B | Evidence | Status |
|---|---|---|---|---|
| TBD | TBD | TBD | continuity / visual trace | Unverified |

## Questions to resolve
- Exact JL model and package pinout; confirm AC7911B8 hypothesis.
- Whether main IC is directly connected to USB-C D+/D-.
- What ICs sit near the jacks and power inductors.
- Whether the patterned copper areas are capacitive electrodes.
- What the FPC connects to and its connector pin numbering.
- Battery protection / charger topology.
- Number of PCB layers and any hidden vias/traces.

## Prior research
- https://github.com/AL-255/FM-1-RE
- https://github.com/aroum/fm1-custom-fw
- https://github.com/cicloid/awesome-fm-1

External firmware information is not evidence of a specific PCB net. Preserve a clear separation between photographed facts, external reports, and hypotheses.
