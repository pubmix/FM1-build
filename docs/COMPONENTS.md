# Component inventory — DX7 MB V07

Confidence: **Observed** = readable in provided photo; **Reported** = external teardown; **Hypothesis** = needs verification.

| Ref / region | Identification | Confidence | Notes |
|---|---|---|---|
| Main JL IC | JieLi-branded, ~48-pin square package | Observed | Top mark approx C189734-1188, not a model ID |
| Main processor model | AC7911B8 / AC791N family | Reported | Community FM-1 teardown; compare package and pinout |
| U2, U3 | 74HC595D shift registers | Observed | Pin-level nets not traced |
| Battery | LiPo 3.7V, 2000mAh, 7.4Wh | Observed | Battery connector wires visible |
| USB | USB-C receptacle | Observed | USB signals not traced |
| Audio | Two 3.5 mm sockets | Observed | Determine line/headphone/mic roles |
| Controls | Multiple potentiometers/encoders and tactile buttons | Observed | Determine each pin function |
| Display | FPC ribbon connector | Observed | Pin count and signals unverified |
| LEDs/electrodes | Many LEDs and comb-pattern copper structures | Observed | Capacitive-touch function unverified |
| DAC | CS4344 | Reported | Verify physical IC and pinout before use |
| Amplifier | SL5316 | Reported | Verify physical IC and pinout before use |
| Power IC | ACC3610S | Reported | Function and exact marking unverified |

Do not infer electrical connectivity from physical proximity. For all parts, verify orientation, pin 1, supply voltage, and footprints.
