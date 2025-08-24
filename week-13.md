# Week 13

**Updates:**
- Needed C++ wrapper for AFL++ shell script -> switched to libFuzzer
- Implemented black-box fuzzing using Go native scripts

**Fuzzers:**
- `daemon_fuzzer.go`: starts ipp-usb binary, fuzzes HTTP endpoints like `/ipp/print`
- `usb_fuzzer.go`: fuzzes USB protocol parsing
- `http_client_fuzzer.go`: fuzzes printer responses to test ipp-usb HTTP client
