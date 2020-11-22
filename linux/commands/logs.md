
**Looking for errors In System Journal log**

You can inspect system journal log for errors of the current boot;
*  `journalctl -b -p3`

The previous boot:
*  `journalctl -b -1 -p3`