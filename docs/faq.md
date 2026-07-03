# FAQ / Troubleshooting — HC22002

> 🏠 [HardCode — all products](https://github.com/hardcodebr) · 🛒 [Shop](https://lectronz.com/stores/hardcode-electronics) · 🌐 [hardcode.com.br](https://hardcode.com.br)

**The port doesn't appear / can't connect.**
Install the USB-to-serial driver for your OS, try another USB-C cable, and confirm the
programmer enumerates as a serial port.

**Flashing fails or times out.**
Check TX↔RX are crossed, GND is connected, and the target is powered. If you power the
target from the programmer, connect VCC. Lower the baud rate and retry.

**Do I still need the BOOT/RST buttons?**
No — auto-reset handles download mode. The buttons are there for manual control only.

**Does it power my ESP board?**
It can supply the target over VCC for small modules. For boards with their own supply,
leave VCC disconnected.

**Which ESP chips are supported?**
ESP8266, ESP32, and ESP32-S2/S3/C3 over UART download.

**What are the two little jumpers (JP1 / JP2) for?**
They enable a pull-up on **EN** (JP1) and **IO0** (JP2) — the ESP's strap pins, which must idle
high to boot. They ship **fitted** so bare modules boot out of the box. Remove a cap only if your
target already has its own EN/IO0 pull-ups and you see boot/flash flakiness. See
[Pinout → Pull-up jumpers](pinout.md#pull-up-jumpers-jp1--jp2).

More help: support@hardcode.com.br
