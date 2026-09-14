# Citations

All technical claims in this repo come from the public YarisWorld threads below. Original JPEGs stay on YarisWorld (login required). Diagrams in `/diagrams` are reconstructions of those posts, not scans of the JPEGs.

## Primary source (the post in the phone screenshot)

1. brushforhire, *Wiring and electronic issues*, post #4 in *THE 2ZRFE engine swap thread - Just the facts*, 12 May 2016, last edited 23 May 2016.
   - Live post: https://yarisworld.com/forums/showpost.php?p=781189&postcount=4
   - Thread: https://www.yarisworld.com/forums/showthread.php?t=56678
   - Archive (attachment IDs inline): https://www.yarisworld.com/forums/archive/index.php/t-56678.html

   Attachment IDs from that post: 57100 (MAF wire), 57162 (add-a-circuit), 57102 (VSS on trans), 57101 (VSS plug), 57104 (old loom), 57105 (three wires), 57103 and 57106 (pin pull), 57108 (xD connector), 57107 (pin order), 57109 (blue wire / cavity 10), 57110 (example.JPG — author marked incorrect), 57159 (ABS connector).

2. Same thread, brushforhire, 12 May 2016 05:44 PM. ABS trial-and-error: first tried A15 pin 11 (with VSC) / pin 22 (without VSC); working speed signal was **pin 4**. Pigtail **82998-12720**.

3. Same thread, *Exhaust* post, 12 May 2016. Collector flange mismatch and RPM / DC Sports notes.

## Same author, build thread

4. brushforhire, *My 2zrfe swap*, https://www.yarisworld.com/forums/showthread.php?t=56233
   - Speed-sensor post: https://yarisworld.com/forums/showpost.php?p=778739&postcount=50
   - Ground-wire correction: https://yarisworld.com/forums/showpost.php?p=778741&postcount=51 (cavity 9 add, do not cut cavity 10). Edited 3 May 2016.
   - ABS signal found: archive t-56233, 23 May 2016. Attachments **57160**, **57161**. GPS vs cluster check.

## Supporting threads (fuse tap / CA2 pin 9)

5. ArmstrongRacing, *The 2zr-fe engine swap guide*, https://www.yarisworld.com/forums/showthread.php?t=56031 — CA2 pin 9 is MAF power; no supporting pin in the Yaris fusebox; mini add-a-circuit on an IG-switched fuse.

6. tmontague, *2zr MAF amperage draw*, https://www.yarisworld.com/forums/showthread.php?t=61572 — do not tap LH headlamp (constant hot). Use **EFI 2**. MAF ~80-90 mA.

7. Project 2ZR Vios part Deux, https://yarisworld.com/forums/showpost.php?p=834496&postcount=13 — CA2 pin 9 / add-a-fuse vs populating the vacant fusebox pin from a junkyard micro-fuse slot.

8. CrankyOldMan, *2ZR MAF sensor connector info*, https://www.yarisworld.com/forums/showthread.php?t=61387 — Sumitomo TS 6189-1046.

## What we could not copy

YarisWorld `attachment.php?attachmentid=NNNNN` returns a login page unless you have a forum session. Wayback Machine has no captures of those attachment URLs (checked 14 Sep 2026). Use `scripts/fetch-attachments.md` to drop the originals into `sources/originals/` from a logged-in browser.
