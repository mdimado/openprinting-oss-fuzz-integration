# Week 8

**Focus:**
- Debugged persistent libusb linker errors:
  - `libusb_alloc_transfer`, `libusb_cancel_transfer`, etc.
- Attempted fixes:
  - Installing libusb dev libraries in Dockerfile
  - Adding CGO environment variables

**Outcome:**
- Errors persisted, blocking progress
- Realization: fuzzing ipp-usb as a library drags in hardware I/O dependencies
