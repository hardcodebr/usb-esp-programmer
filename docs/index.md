# Quick-Start — USB-C ESP Programmer (HC22002)

Flash an ESP8266/ESP32 in three steps. No button presses required.

## 1. Connect
- Plug the programmer into your PC with the included **USB-C** cable.
- Wire the target header to your ESP (see **[Pinout](pinout.md)**):
  `TX→RX, RX→TX, EN, IO0, GND`, and `VCC` if powering the target from the programmer.
- Most operating systems detect the programmer automatically. If not, install the
  USB-to-serial driver for your system.

## 2. Select
- In **esptool / Arduino IDE / ESP-IDF**, pick your board and the programmer's serial port.

## 3. Flash
- Start the upload. The **auto-reset circuit** puts the target into download mode and
  resets it automatically — no need to touch BOOT/RST.

## Manual control (optional)
- **BOOT** + **RST** buttons are on board if you ever need to enter download mode by hand:
  hold **BOOT**, tap **RST**, release **BOOT**.

Trouble? See the **[FAQ](faq.md)**.

## 💬 Feedback & suggestions
Ideas, questions, or something you'd like to see? Open a discussion — we read every one:
**https://github.com/hardcodebr/usb-esp-programmer/discussions**
