# Week 11

**Progress:**
- Improved Python-based virtual IPP-over-USB device:
  - Handles standard USB control requests (e.g., `get_descriptor`, `set_configuration`)
  - Bulk OUT transfers forwarded as IPP POST requests to real CUPS server
  - Bulk IN transfers return CUPS response (or empty reply)
  - Background thread reports connection stats

**Problem:**
- Client attaches successfully but closes immediately after
- Logs:
  - `usbip: error: recv different busid 1-1`
  - Server: `Waiting for USB request #1... No command received, connection may have closed`

**Discovery:**
- Hardcoded BusID mismatch was root cause
- Correct BusID negotiation is required (`usbip list` confirms correct device ID: `1-1: HP, Inc : unknown product (03f0:1234)`)

**Next:**
- Fix BusID handling
- Add proper IPP-over-USB request forwarding to CUPS
