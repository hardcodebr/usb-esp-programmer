# Datasheet — USB-C ESP Programmer (HC22002)

*Rev A (pilot). Items marked **TBD** are being finalized.*

| | Specification |
|---|---|
| **Type** | Non-isolated USB-to-UART ESP programmer |
| **SKU** | HC22002 |
| **Host interface** | USB-C (bus-powered — no external supply) |
| **USB-UART bridge** | TBD |
| **Target interface** | UART — TX, RX, EN (reset), IO0 (boot), GND, VCC |
| **Logic level** | 3.3 V |
| **Auto-reset / auto-boot** | Yes — DTR/RTS → EN/IO0 (two-transistor network) |
| **On-board buttons** | RST, BOOT (manual control) |
| **Pull-up selection** | 2.54 mm header + jumper cap, pre-set default |
| **Flow control** | None (RTS/CTS not used for data) |
| **Max validated baud** | TBD |
| **Power to target** | Optional VCC (3.3 V); max current TBD |
| **Dimensions** | TBD |
| **Mounting** | 4× stick-on rubber feet |
| **Toolchain** | esptool, Arduino IDE, ESP-IDF |
| **Supported targets** | ESP8266, ESP32, ESP32-S2/S3, ESP32-C3 |

**In the box:** board (feet + header & jumper cap fitted) · USB-C cable · 2× leads (Dupont + ribbon) · quick-start card · ESD bag.

See also: [Quick-Start](index.md) · [Pinout](pinout.md) · [FAQ](faq.md)
