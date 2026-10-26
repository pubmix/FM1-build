# FM1-build

Reverse engineering and KiCad reconstruction of the **M-VAVE FM-1** synthesizer hardware, photographed PCB marked **DX7 MB V07**.

> **Status: research / unverified schematic.** This repository is not a production-ready board design. Do not fabricate or apply power based on inferred wiring.

## Goals

1. Document both sides of the original PCB and all component markings.
2. Reconstruct a **pin-accurate KiCad schematic** with provenance for each net.
3. Verify power, processor, audio, display, encoders, buttons, and LED circuitry.
4. Compare the hardware with published FM-1 firmware and hardware research.
5. Optionally make a replacement board only after electrical validation.

## What we know from the photos

- Main JL/JieLi-marked square IC, apparently 48 pins. The visible top marking is **approximately** `C189734-1188`; this is *not* a verified processor part number.
- PCB silkscreen `DX7 MB V07`, additional marking `260918`.
- Two clearly marked `74HC595D` shift registers (U2/U3).
- USB-C port, two 3.5 mm jacks, multiple rotary controls, tactile switches, LEDs, ribbon/display connector.
- Li-polymer battery marked 3.7 V, 2000 mAh, 7.4 Wh.
- No FPGA is visually identified; absence is not electrically proven.

## Processor research

An independently reported FM-1 teardown identifies a **JieLi AC7911B8**, in the **AC791N/WL82** family. **That identification has not yet been verified against this particular PCB's chip marking or pinout.** Package similarity alone is insufficient.

## Research links

- [AL-255/FM-1-RE](https://github.com/AL-255/FM-1-RE) — firmware reverse engineering
- [aroum/fm1-custom-fw](https://github.com/aroum/fm1-custom-fw) — custom firmware and hardware notes
- [FM-1 hardware research](https://github.com/aroum/fm1-custom-fw/blob/main/REVERSE_ENGINEERING.md)
- [cicloid/awesome-fm-1](https://github.com/cicloid/awesome-fm-1) — community project directory
- [JieLi research](https://kagaimiq.github.io/jielie/)
- [74HC595 datasheet](https://assets.nexperia.com/documents/data-sheet/74HC_HCT595.pdf)

## Start on your computer

```bash
git clone https://github.com/pubmix/FM1-build.git
cd FM1-build
```

Open KiCad, create a new project named `FM1-build` inside `hardware/kicad/`, then start with the blocks in [docs/REVERSE_ENGINEERING.md](docs/REVERSE_ENGINEERING.md). **No verified native KiCad schematic has been committed yet.**

See [docs/COMPONENTS.md](docs/COMPONENTS.md) and [docs/MEASUREMENT_PLAN.md](docs/MEASUREMENT_PLAN.md).

## Provenance

Compiled from user-supplied disassembly photographs and conversation research (October 2026). The original photographs and preliminary PDF are **not yet committed**. Third-party repositories are linked, not copied. Any later verified net should record photo reference, test points, measurement, and confidence.
