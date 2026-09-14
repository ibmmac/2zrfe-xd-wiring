# 2ZR-FE / Scion xD harness wiring

Shop notes for putting a **2ZR-FE** and **Scion xD engine harness / ECM** into a **2nd-gen Yaris (XP90)**.

Clean reconstruction of brushforhire's YarisWorld posts (May 2016), plus later corrections from the same author and from tmontague / 06YarisRS.

**Do not cut the blue wire in cavity 10.** That photo in the original post is the author's mistake. He fixed it. See docs/WIRING.md.

## Files

- [docs/WIRING.md](docs/WIRING.md) — MAF power, VSS move, cavity 9 ground, ABS speed tap
- [docs/EXHAUST.md](docs/EXHAUST.md) — collector flange / midpipe / header
- [docs/PARTS.md](docs/PARTS.md) — part numbers and fuse-tap notes
- [docs/SOURCES.md](docs/SOURCES.md) — thread URLs and attachment IDs
- [diagrams/](diagrams/) — SVG pin maps from the text
- [scripts/fetch-attachments.md](scripts/fetch-attachments.md) — drop in original JPEGs with a YarisWorld login

Original attachment JPEGs are login-walled and not on Wayback. sources/originals/ starts empty on purpose.

## Paths

- Path A: Yaris AUTO trans — move 3 VSS pins onto the xD connector, add ground in cavity 9
- Path B: Scion xD trans — ABS pin 4 to pink VSS wire; leftover VSS +12V can feed MAF
- Path C: Yaris MANUAL — unconfirmed; treat like Path A until mapped

## Credit

brushforhire, YarisWorld *THE 2ZRFE engine swap thread - Just the facts*, last edited 2016-05-23.
