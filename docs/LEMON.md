# LEMON Manuals (lemon-manuals.la/Toyota)

Catalog used: https://lemon-manuals.la/Toyota/

LEMON is a free service-manual library (CHARM-era books plus later years). Wiring plates live under each vehicle's Repair and Diagnosis tree. This repo does **not** republish those OEM sheets. Use the links below next to the swap diagrams in FIGURES.md.

## Chassis book (what you are wiring into)

XP90 Yaris, 1NZ-FE body / fusebox / cluster / ABS / VSS:

- 2010 Yaris L4-1.5L (1NZ-FE): https://lemon-manuals.la/Toyota/2010/Yaris%20L4-1.5L%20%281NZ-FE%29/
- Year index: https://lemon-manuals.la/Toyota/2010/
- 2012 Yaris Hatchback L4-1.5L (1NZ-FE): listed at https://lemon-manuals.la/Toyota/2012/

Inside the 2010 Yaris book, look for:

- Wiring Diagrams / System Wiring Diagrams
- Engine Control (1NZ-FE) — MAF, EFI power
- Combination Meter — vehicle speed input (the pink VSS wire Path B splices into)
- ABS / VSC — speed-signal output (Path B donor idea; confirm pin 4 on the **xD** ABS connector, not this Yaris book)
- Power Source / EFI, EFI-2 fuses
- Electronically Controlled Transmission — Yaris auto VSS on top of the case (Path A)

## Do not use this Yaris book for the swap

- 2020 Yaris LE sedan: https://lemon-manuals.la/Toyota/2020/Yaris%20LE%2C%204D%20Sedan%2C%20Standard%20Trans/Repair%20and%20Diagnosis%20%28Single%20Page%29/

That is the Mazda-built XP150 sedan (P5 engine control, 07/2015+ procedures). Wrong car.

## Donor engine / harness book (2ZR-FE)

The xD / Corolla 2ZR-FE electrical is **not** in the 2010 Yaris 1NZ book. On LEMON, start at https://lemon-manuals.la/Toyota/ and open:

- 2009–2013 Corolla 1.8 2ZR-FE (same engine family as the xD donor)
- 2010 Prius 2ZR-FXE is hybrid only — different harness, skip it for this swap

Confirm the book title says **2ZR-FE**, then pull:

- Engine Control (2ZR-FE) — MAF +12 V on CA2 pin 9
- ABS / VSC connector A15 — speed-out pin (forum found working cavity **4** after trying 11 / 22)
- Automatic transaxle connector — cavity 9 empty / cavity 10 blue on the xD harness

## How this lines up with the swap notes

| Swap step | Forum source | LEMON book to open |
|---|---|---|
| MAF has no Yaris fusebox pin | brushforhire t=56678 #4; ArmstrongRacing t=56031 CA2#9 | 2010 Yaris 1NZ power-source + 2ZR-FE engine-control |
| EFI-2 not headlamp | tmontague t=61572 | 2010 Yaris fuse / power source |
| VSS 3-wire move | t=56678 #4 | 2010 Yaris ECT / VSS + xD/Corolla 2ZR engine harness |
| Cavity 9 ground | t=56678 #4; t=56233 #51 | xD/Corolla trans connector end view |
| ABS pin 4 + pigtail 82998-12720 | t=56678; t=56233 23 May 2016 | xD ABS connector end view |

## Citation

LEMON Manuals, Toyota index, https://lemon-manuals.la/Toyota/ (retrieved 14 Sep 2026). Individual vehicle pages as linked above. OEM artwork remains Toyota's; LEMON is the access copy.
