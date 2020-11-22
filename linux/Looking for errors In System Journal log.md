Looking for errors In System Journal log


    You can inspect system journal log for errors of the current boot, or the previous one:
    journalctl -b -p3
    journalctl -b -1 -p3