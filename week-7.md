# Week 7

**New Approach:**
- Forked ipp-usb repo
- Changed `package main` -> `package usb`
- Started exporting unexported methods/fields:
  - `sanitizeIppResponse` -> `SanitizeIppResponse`
  - Exposed required struct fields

**Problem:**
- Build errors due to missing libusb functions
- CGO + hardware dependencies pulled in
