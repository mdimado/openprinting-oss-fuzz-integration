# Week 5

**Work on ipp-usb:**
- Identified key fuzzing areas: string extraction, XML parsing
- Wrote first harnesses for these
- Created initial build script and Dockerfile
- Attempted local OSS-Fuzz build -> failed because ipp-usb is a **program (main)**, not a package

**Challenge:**
- Need workaround to fuzz ipp-usb despite its architecture
