# Week 6

**Experiments:**
- Tried local copy approach:
  - Copied ipp-usb sources into fuzzing repo
  - Used `go mod edit -replace` to make imports work
- Harnesses written:
  - `FuzzIppAttrsGetStrings`
  - `FuzzConfLoadInternal`
  - `FuzzHttpProxy`

**Issues:**
- OSS-Fuzz builds failed:
  - Undefined types (UsbTransport, NewLogger)
  - Unexported types/methods
  - Requires mock USB device for HTTP proxy fuzzing
