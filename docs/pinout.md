# Pinout — USB-C ESP Programmer (HC22002)

> 🏠 [HardCode — all products](https://github.com/hardcodebr) · 🛒 [Shop](https://lectronz.com/stores/hardcode-electronics) · 🌐 [hardcode.com.br](https://hardcode.com.br)

Target header (programmer → target):

| Signal | Direction | Connect to ESP |
|--------|-----------|----------------|
| **GND** | — | GND |
| **VCC** | out (optional) | 3V3 — only if powering the target from the programmer |
| **TX**  | out | target **RX** |
| **RX**  | in  | target **TX** |
| **EN (RST)** | out | EN / reset (driven by the auto-reset circuit) |
| **IO0 (BOOT)** | out | IO0 / boot strap (driven by the auto-reset circuit) |

- Logic level: **3.3 V**.
- Cross TX↔RX (programmer TX goes to target RX, and vice-versa).
- A populated header + jumper cap selects the pull-up configuration (pre-set to a
  sensible default; move it only for non-standard targets).

*(Exact header pin order/pitch and electrical limits: see the product page.)*
