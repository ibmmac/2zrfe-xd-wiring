# How to drop the original JPEGs in

YarisWorld serves attachments only to a logged-in browser.

1. Log into https://www.yarisworld.com/
2. Open https://www.yarisworld.com/forums/showthread.php?t=56678
3. Save each image into sources/originals/ using the names in this file.

```
sources/originals/57100-maf-sensor-wire.jpg
sources/originals/57162-add-a-circuit.jpg
sources/originals/57102-yaris-vss-on-trans.jpg
sources/originals/57101-vss-sensor-connector.jpg
sources/originals/57104-old-speed-harness.jpg
sources/originals/57105-three-wires-old-plug.jpg
sources/originals/57103-removing-pins.jpg
sources/originals/57106-wires.jpg
sources/originals/57108-xd-connector-speed.jpg
sources/originals/57107-pin-order.jpg
sources/originals/57109-blue-wire-cavity-10.jpg
sources/originals/57110-example-DO-NOT-FOLLOW.jpg
sources/originals/57159-abs-connector.jpg
```

If curl has your session cookie:

```bash
COOKIE='vbulletin_xxx=...; bbsessionhash=...'
for id in 57100 57162 57102 57101 57104 57105 57103 57106 57108 57107 57109 57110 57159; do
  curl -fsSL -H "Cookie: $COOKIE" \
    "https://www.yarisworld.com/forums/attachment.php?attachmentid=${id}" \
    -o "sources/originals/${id}.jpg"
  file "sources/originals/${id}.jpg"
done
```
