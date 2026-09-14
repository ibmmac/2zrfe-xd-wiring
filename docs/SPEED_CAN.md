# Speed / CAN splice — this pair

The engine runs. Speed does **not** come from the U341E.

| Role | Vehicle | VIN | Notes |
|---|---|---|---|
| Chassis | 2010 Yaris 5-door hatch | `JTDKT4K35A5318649` | Built 5MT. VSC standard, **no VSC OFF button**. Keep **A30** + cluster + body CAN. |
| Powertrain | 2009 Scion xD | `JTKKU10409J041220` | **2ZR-FE + U341E** + xD Engine/ECT ECU + xD engine harness. |

U341E has **no tail-shaft VSS**. The 2010 Yaris cluster reads speed from the **Yaris A30 skid ECU over CAN**, not from the trans and not from the xD A15 module.

## Path

```
Wheels → Yaris sensors → Yaris A30 → CANH/CANL → cluster
                              └─────── same CAN ──→ xD 2ZR ECU A21
```

## Splices

| # | From | Pin | To | Pin | Why |
|---|---|---|---|---|---|
| 1 | Yaris A30 | seated | actuator | — | No A30 = no speed message |
| 2–5 | LF/RF/LR/RR sensors | 2-pin at hub | A30 | FL/FR/RL/RR ± | Wheel speed into A30 |
| 6 | Yaris A30 | **25 CANH** (W) | Yaris DLC3 | **6 CANH** (W) | Stock — confirm not cut |
| 7 | Yaris A30 | **14 CANL** (G) | Yaris DLC3 | **14 CANL** (V) | Stock — confirm not cut |
| 8 | xD ECM **A21** | **41 CANH** | Yaris DLC3 | **6 CANH** | Only new high wire |
| 9 | xD ECM **A21** | **49 CANL** | Yaris DLC3 | **14 CANL** | Only new low wire |

Keep the A21 pair twisted. Confirm 41/49 by tracing the xD harness twisted pair to the old xD DLC stub (pin 6 = CANH, pin 14 = CANL).

LEMON connector IDs:

- xD ECM cabin plug: **A21** 90980-12462 black
- xD ECM engine plug: **C19** 90980-12399 — **not used for CAN**
- Skid ECU: Yaris **A30** / xD **A15** 90980-12658 (same shell)
- DLC3: **F16** 90980-11978

## Do not connect

| Do not | Why |
|---|---|
| U341E case / any trans pin → cluster | No VSS on this box |
| A30 / A15 **pin 4** → pink speed / cluster | Pin 4 is **RL−**, not SPD |
| xD A15 CAN → Yaris cluster | Cluster only listens to Yaris A30 |
| xD A15 in place of Yaris A30 | Leave Yaris A30 in the Yaris |
| xD ECM C19 for CAN | CAN is on A21 |

The YarisWorld sticky “ABS pin 4” trick does **not** apply to this 2010 VSC hatch.

## Bench check

1. Key ON, A30 seated: ABS / slip lamps go out after the bulb check.
2. Scan tool on the Yaris DLC: you must see **ABS/VSC** and **Engine**. No Engine → A21 CAN splice wrong. No ABS → A30 CAN open.
3. Spin a front wheel: ABS data list should show wheel speed. If that works and the needle is dead, the cluster CAN junction is open.

## Still required (not speed)

- MAF power from EFI-2 add-a-circuit
- Extra ground in xD trans-plug cavity 9 — **do not cut the blue cavity-10 wire**
- Use the xD **Engine and ECT** ECU with the U341E (not a 5MT ECM)
- PNP / range switch must feed starter interlock (Yaris was a 5-speed)

## LEMON

- [2009 xD 2ZR-FE](https://lemon-manuals.la/Scion/2009/xD%20L4-1.8L%20%282ZR-FE%29/)
- [2010 Yaris 1NZ-FE](https://lemon-manuals.la/Toyota/2010/Yaris%20L4-1.5L%20%281NZ-FE%29/)
- xD connectors: A21 (ECM), A15 (skid), F16 (DLC3)
- Yaris: Connector Views By Connector Number → **A30**

Toyota color letters: W white, B black, Y yellow, L blue, G green, R red, P pink, V violet, LG light green.
