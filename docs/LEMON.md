# LEMON Manuals

Catalogs:
- Toyota chassis: https://lemon-manuals.la/Toyota/
- Scion donor: https://lemon-manuals.la/Scion/

This repo does **not** republish OEM wiring plates. Use the links next to FIGURES.md.

## Donor book (Scion xD, 2ZR-FE) — use this for Path B

xD is listed under **Scion**, not Toyota:

- Make index: https://lemon-manuals.la/Scion/
- 2008 xD L4-1.8L (2ZR-FE): https://lemon-manuals.la/Scion/2008/xD%20L4-1.8L%20%282ZR-FE%29/
- 2009 xD L4-1.8L (2ZR-FE): https://lemon-manuals.la/Scion/2009/xD%20L4-1.8L%20%282ZR-FE%29/
- 2010 xD L4-1.8L (2ZR-FE): https://lemon-manuals.la/Scion/2010/xD%20L4-1.8L%20%282ZR-FE%29/

Year lists:
- https://lemon-manuals.la/Scion/2008/
- https://lemon-manuals.la/Scion/2009/
- https://lemon-manuals.la/Scion/2010/

Open the year that matches the donor harness / ECM. Inside the book pull:

- Engine Control (2ZR-FE) — MAF +12 V, CA2 pin 9
- ABS / VSC connector A15 — speed-out (forum working cavity is **4**, after trying 11 w/ VSC and 22 w/o VSC)
- Automatic transaxle connector — cavity 9 empty, blue wire in cavity 10
- Power source / EFI

Do **not** use Scion tC or xB books (those are 2AZ-FE).

## Chassis book (Yaris XP90 you are wiring into)

- 2010 Yaris L4-1.5L (1NZ-FE): https://lemon-manuals.la/Toyota/2010/Yaris%20L4-1.5L%20%281NZ-FE%29/
- Year index: https://lemon-manuals.la/Toyota/2010/

Look for Combination Meter (pink VSS into cluster), Power Source / EFI-2, Yaris auto VSS if Path A.

Skip the 2020 Yaris LE sedan book — that is the Mazda XP150.

## How this lines up

| Swap step | Forum | LEMON |
|---|---|---|
| MAF / CA2 #9 | t=56678 #4; t=56031 | 2008–2010 Scion xD Engine Control |
| EFI-2 fuse tap | t=61572 | 2010 Yaris power source |
| VSS 3-wire move | t=56678 #4 | Yaris ECT + xD harness |
| Cavity 9 ground | t=56678 #4; t=56233 #51 | xD trans connector end view |
| ABS pin 4 + 82998-12720 | t=56678; t=56233 | xD ABS connector end view |

## Citation

LEMON Manuals, Scion index https://lemon-manuals.la/Scion/ and Toyota index https://lemon-manuals.la/Toyota/ (retrieved 14 Sep 2026). OEM artwork remains Toyota/Scion; LEMON is the access copy.
