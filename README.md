# 2ZR-FE / Scion xD harness wiring

Shop notes for a **2ZR-FE** + **Scion xD engine harness / ECM** in a **2nd-gen Yaris (XP90)**.

Primary source used: [brushforhire, *Wiring and electronic issues*, YarisWorld t=56678 post #4](https://yarisworld.com/forums/showpost.php?p=781189&postcount=4) (12 May 2016, last edited 23 May 2016).

**Do not cut the blue wire in cavity 10.** The `example.JPG` in that post is the author's own mistake.

## Start here

- [docs/FIGURES.md](docs/FIGURES.md) — diagrams with sources under each figure
- [docs/WIRING.md](docs/WIRING.md) — full wiring write-up
- [docs/EXHAUST.md](docs/EXHAUST.md)
- [docs/PARTS.md](docs/PARTS.md)
- [docs/CITATIONS.md](docs/CITATIONS.md) — every thread, post, and attachment ID
- [scripts/fetch-attachments.md](scripts/fetch-attachments.md) — how to copy the original JPEGs once you are logged into YarisWorld

Original attachment JPEGs are login-walled and not in the Wayback Machine. The SVGs in `/diagrams` reconstruct pin locations from the text.

## Paths

- Path A: Yaris AUTO trans — move 3 VSS pins onto the xD connector, add ground in cavity 9
- Path B: Scion xD trans — ABS pin 4 to pink VSS wire; leftover VSS +12V can feed MAF
- Path C: Yaris MANUAL — unconfirmed; treat like Path A until mapped
