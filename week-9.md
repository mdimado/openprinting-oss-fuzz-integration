# Week 9

**Discussions with Alexander:**
- Architecturally ipp-usb is a **standalone program**, not a library
- Import-based fuzzing not feasible
- Only viable path: fuzz via **HTTP interface**
- Problem: requires actual IPP-over-USB device
- Perfect solution: write a **virtual device simulator**

**Next:**
- Explore usbip and VirtualUSBDevice projects for simulation
