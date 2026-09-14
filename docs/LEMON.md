# LEMON Manuals — this swap

**Cars:** 2010 Toyota Yaris hatchback (chassis) + 2009 Scion xD 2ZR-FE (donor harness / ECM / engine).

Catalogs:
- Toyota 2010: https://lemon-manuals.la/Toyota/2010/
- Scion 2009: https://lemon-manuals.la/Scion/2009/

This repo does **not** republish OEM plates.

## 2009 Scion xD (donor)

Engine-family book (use this first):
- https://lemon-manuals.la/Scion/2009/xD%20L4-1.8L%20%282ZR-FE%29/

Year list (ignore tC / xB — those are 2AZ-FE):
- https://lemon-manuals.la/Scion/2009/

Open in that book:
- Engine Control (2ZR-FE) — MAF +12 V, CA2 pin 9
- ABS / VSC connector A15 — speed-out. Forum working cavity is **4** (tried 11 w/ VSC and 22 w/o VSC first)
- Auto transaxle connector — add ground in cavity **9**, leave the blue wire in **10**
- Power source / EFI

Pigtail P/N **82998-12720** for the ABS pin.

## 2010 Yaris hatch (chassis)

Engine-family book (1NZ fusebox / cluster / body):
- https://lemon-manuals.la/Toyota/2010/Yaris%20L4-1.5L%20%281NZ-FE%29/

Body-style books on the same year page:
- 2D Hatch Automatic: https://lemon-manuals.la/Toyota/2010/Yaris%202D%20Hatchback%2C%20Automatic/
- 2D Hatch Standard: https://lemon-manuals.la/Toyota/2010/Yaris%202D%20Hatchback%2C%20Standard/
- 4D Hatch Automatic: https://lemon-manuals.la/Toyota/2010/Yaris%204D%20Hatchback%2C%20Automatic/
- 4D Hatch Standard: https://lemon-manuals.la/Toyota/2010/Yaris%204D%20Hatchback%2C%20Standard/

Year index: https://lemon-manuals.la/Toyota/2010/

Open in the Yaris book:
- Power Source / EFI-2 (ignition, not headlamp)
- Combination Meter — pink vehicle-speed input that Path B splices into
- ECT / VSS if you keep the Yaris auto (Path A, move 3 pins)

Do not use sedan books unless the car is a sedan. Do not use the 2020 Yaris LE book (Mazda XP150).

## Path picker

- Path A — keep Yaris auto: Yaris VSS 3-wire move + cavity 9 ground on the xD harness connector.
- Path B — xD trans: ABS pin 4 → pink VSS toward Yaris fusebox/cluster; leftover VSS +12 V can feed MAF.
- Path C — Yaris manual: unconfirmed; treat like Path A until mapped.

## Citation

LEMON Manuals, 2010 Toyota Yaris and 2009 Scion xD pages linked above (retrieved 14 Sep 2026). Forum wiring: brushforhire, YarisWorld t=56678 post #4 and t=56233. OEM artwork remains Toyota/Scion.
