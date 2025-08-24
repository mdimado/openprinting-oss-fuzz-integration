# Week 10

**Experiments:**
- Explored Python USB/IP implementations:
  - https://github.com/jtornosm/USBIP-Virtual-USB-Device/tree/master/python
  - Developed own extension: https://github.com/mdimado/py-virtualippusb
- Built a basic **virtual USB printer**:
  - Device is recognized by USBIP client
  - `usbip list` and `usbip attach` commands succeed at handshake
  - Attach step works and device shows up as exportable

**Challenge:**
- After attaching, client disconnects before sending USB requests
- Python server logs:  
  `Connection closed while receiving data (got 0/48 bytes)`
- Indicates USBIP session established but protocol negotiation incomplete
