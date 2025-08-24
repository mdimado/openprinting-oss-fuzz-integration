# Week 12

**Context:**
- ipp-usb is a standalone program, not a library
- Turning it into a library is not feasible
- Only viable testing approach: external interfaces (HTTP over USB)

**Black-Box Fuzzing Plan:**
- Fuzzer (AFL++) provides input data
- Simulated IPP-over-USB device (emulator) is started
- ipp-usb daemon is started, connecting to virtual device
- Fuzzed input is injected into the communication loop
- AFL++ monitors the process for crashes

**Progress:**
- Created build scripts (`build.sh`, `oss_fuzz_build.sh`)
- Builds complete for both AFL and libFuzzer engines

**Challenge:**
- afl-fuzz failed with a "shell script" error

**Next step:**
- Create small C++ wrapper program for AFL++ to work with shell script
