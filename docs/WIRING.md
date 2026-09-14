# Wiring and electronic issues

Reconstructed from brushforhire, YarisWorld t=56678 and *My 2zrfe swap* (t=56233). Source post last edited **23 May 2016, 05:42 PM**.

## Wiring for all swaps — MAF +12 V

The xD MAF does **not** get power from the Yaris body harness. There is no pin in the fusebox cavity for that wire.

### Option 1 — Mini add-a-circuit (usual path)

1. Find the **black wire with silver speckles** in the engine-harness connector that lands in the under-hood fusebox. That is MAF power on the xD harness.
2. Pop the pin out of the cavity (preferred). Snipping it works but leaves a stub the author hated.
3. Feed that MAF power lead from a **mini add-a-circuit** on a true **ignition-switched** fuse.
4. Later 2ZR swaps (tmontague) used **EFI-2**, not a headlamp slot. Headlamp fuses stay hot with key off and keep the ECU / MAF awake (~80-90 mA extra draw).

KOEO check: battery voltage on MAF power, 0 ohms from MAF ground pin to battery negative.

See [diagrams/01-maf-add-a-circuit.svg](../diagrams/01-maf-add-a-circuit.svg).

Original names: `MAF sensor wire.JPG`, `add a circuit.jpg`. Attachment IDs: **57100**, **57162**.

### Option 2 — Leftover VSS power (Path B only)

If ABS now drives the speedometer, the old VSS circuit leaves a spare switched +12 V and a ground. The author planned to use that leftover +12 V for the MAF. Confirm it is ignition-switched first.

## Path A — Yaris automatic trans + xD engine harness

The xD harness does not provide a speed signal from its own transmission. Move the Yaris VSS wires onto the xD connector. Same cavities.

| Step | What | Original filename | Att. ID |
|---|---|---|---|
| 1 | VSS on top of the Yaris trans | speed plug.JPG | 57102 |
| 2 | Connector on the sensor | speed connector.JPG | 57101 |
| 3 | Cut old loom back to the white connector | speed harness.JPG | 57104 |
| 4 | Three wires to pull from the old connector | three wires in old plug.JPG | 57105 |
| 5 | Needle / terminal tool | removing pins.JPG, wires.jpg | 57103, 57106 |
| 6 | Same three pins in the xD connector | xd connector speed.JPG | 57108 |
| 7 | Pin order | this is how they go in.JPG | 57107 |

Lift the connector retainer first. A sewing needle works if you do not force the barb.

See [diagrams/02-vss-pin-move.svg](../diagrams/02-vss-pin-move.svg).

### Cavity 9 ground — do this, and do not cut the blue wire

On the automatic, add a pin in the **upper** trans connector:

- **Cavity 10** — solid **blue** wire. Already populated. **Leave it connected to the ECM.**
- **Cavity 9** — empty on the xD harness (rubber cavity plug). Hole immediately next to the blue wire.

The Yaris valve body grounded itself through the ECM. The xD harness does not. Cavity 9 is the new ground.

1. Pull one spare pin/wire from the old Yaris trans plug.
2. Remove the rubber plug from cavity 9 on the xD connector.
3. Seat the Yaris pin in cavity 9.
4. Add an eyelet and ground it to the **trans case**.
5. Author tapped an unthreaded hole **6 mm x 1.00** and ran a bolt.

See [diagrams/03-cavity-9-ground.svg](../diagrams/03-cavity-9-ground.svg).

> **Correction (author, 3 May 2016):** `example.JPG` (attachment **57110**) shows the blue wire cut and grounded. That picture is **wrong**. CEL cleared after he added a pin in 9 and restored pin 10. Quote: ALL YOU NEED TO DO IS ADD A PIN/WIRE TO THE EMPTY PIN LOCATION 9, NEXT TO THE BLUE WIRE IN SPOT 10, SO YOU CAN GROUND IT OUT.

Reference photo: `blue wire.JPG` (attachment **57109**).

## Path C — Yaris manual trans

Not confirmed. Author expected the VSS move to match Path A. Map it on the bench before you cut.

## Path B — Scion xD trans (speedo from ABS)

1. Buy Toyota pigtail **82998-12720**, or harvest the same terminal.
2. Insert it at **ABS connector location 4** — smaller white wire in the top row, four from the left counting the two bigger wires.
3. Cut the **pink** wire that originally ran to the transmission VSS.
4. Splice the new ABS speed-signal wire onto that pink wire so it still lands in the fusebox connector the cluster / ECM already expects.

Original photos: `abs connector.jpg` (57159), `wires.jpg` (57106).

See [diagrams/04-abs-pin4.svg](../diagrams/04-abs-pin4.svg).

Note: an xD manual case often has a cap where a VSS would sit. Some later builders drop the Yaris sensor in that hole. That is a different path than this ABS tap.

## Bench check before first start

- Key ON, engine OFF: MAF power = battery voltage. MAF ground = 0 ohms to battery negative.
- Path A: continuity from the new cavity-9 wire to the trans case. Blue cavity-10 still continuous back to the ECM.
- Path B: ABS pin 4 seated, pink splice insulated. Cluster speedo should tick when you spin a driven wheel.
- After the first run, clear codes. P0500 = speed circuit. P0100-P0104 = MAF (wrong fuse or wrong cavity).
