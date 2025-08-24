# Week 14

**Work with Python (pycups):**
- Explored Atheris (Python fuzzing engine)
- Studied OSS-Fuzz integrations for Pillow, PyYAML

**Fuzzing Harnesses:**
- Implemented harness for:
  - `UTF8_from_PyObj()`
  - `PyObj_from_UTF8()`

**Build & Testing:**
- Wrote build scripts and Dockerfile
- Tested harness on OSS-Fuzz -> ran successfully

**Next Targets:**
- `getFile`, `putFile`
- `writeRequestData()`
- `readIO` and `writeIO` for `IPP I/O` callback mechanism
- authentication callback handling
