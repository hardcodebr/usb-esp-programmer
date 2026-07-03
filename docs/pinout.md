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

## Pull-up jumpers (JP1 / JP2)

Next to the target header are two small **2-pin jumpers**. Each one connects an optional
**pull-up** onto one of the ESP's two strapping pins:

| Jumper | Pull-up on | ESP pin |
|--------|------------|---------|
| **JP1** | EN / RESET | chip-enable |
| **JP2** | IO0 / BOOT | boot strap |

- **Jumper cap fitted = pull-up ON.** Cap removed = that line is left to the target.
- **Ships with both caps fitted** (both pull-ups enabled) — the default that works for most targets.

**What they do.** EN and IO0 must idle **high** for an ESP to run and boot normally — the
auto-reset circuit only pulses them low for the moment of flashing. A **bare ESP module** or a
minimal custom board with no pull-ups of its own can fail to boot or hang in reset. These jumpers
give those two pins a clean high idle level so flashing just works out of the box.

**When to remove a cap:**
- Your target board **already has its own EN/IO0 pull-ups** (most dev boards do). Two in parallel
  is usually harmless, but pull the cap(s) if you see boot or flashing flakiness.
- You need EN or IO0 **fully released** so the target can drive it.
- Leave them **fitted** whenever bringing up a bare module — that's what they're for.

*(JP1/JP2 are marked on the board silkscreen. Exact header pin order/pitch and electrical limits:
see the product page.)*
