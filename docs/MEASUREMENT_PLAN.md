# Measurement and safety plan

**Before probing:** Disconnect USB, unplug the battery if possible, and allow capacitors to discharge. Never use continuity or resistance mode on an energized PCB. Avoid shorting LiPo terminals; do not puncture, bend, or heat the cell.

1. Take orthogonal, well-lit photos of both PCB faces, with the battery moved safely aside without stressing wires. Include a ruler and chip close-ups.
2. Record every IC marking, reference designator, package dimensions, and pin-1 indication.
3. In unpowered continuity mode, identify GND using USB shield, jack sleeves, and large copper pours; do not assume all are connected.
4. Trace battery positive through protection and charging components; map USB VBUS separately.
5. Trace 74HC595 VCC/GND and pins 11 (SHCP), 12 (STCP), 14 (DS), 13 (OE), 10 (MR), 9 (Q7S); verify against datasheet and actual board orientation.
6. Map each output to LEDs or other loads using continuity, not guesses.
7. Trace audio jacks to nearby passives/ICs; record series capacitors and ground.
8. Identify display FPC pin 1 and count pins; verify all signals.
9. For any powered measurement, use current-limited bench equipment and an appropriate grounded probe setup; first verify rails and expected voltage ranges.

## Recording template
- Date:
- PCB revision:
- Photo filename / coordinates:
- Meter / mode:
- Probe A: reference, pin
- Probe B: reference, pin
- Reading:
- Interpretation:
- Confidence: observed / measured / inferred
