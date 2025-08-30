# PulseShift Technology

**PulseShift** is an open-source power system for **safe hot-swapping** of tool batteries in scooters, e-bikes, and light EVs.  
It separates **drive power** from a **keep-alive circuit**, ensuring the controller stays powered during swaps — no brownouts or reboot.

---

## Wiring Diagram

[![PulseShift Wiring Diagram](docs/wiring-diagram.svg)](docs/wiring-diagram.svg)

**Legend:**
- 🔴 **Red** = Main Drive Path (~pack voltage to motor/controller)  
- 🔵 **Blue** = Keep-Alive Path (regulated 12V logic)  
- ⚫ **Black** = Common Ground (tie all negatives)  
- 🟢 **Green** = Optional control/indicator lines

---

## Quick Start

1. **Install tool battery adapter and fuse.**  
2. **Wire main drive via ideal-diode to the booster → controller +.**  
3. **Setup keep-alive rail**: pack → buck/boost to 12V → diode → supercap → booster IN+.  
4. **Turn on keep-alive**, then insert battery pack — controller should stay powered.  
5. **Hot-swap**: Insert new pack before removing the old; logic stays alive via supercap.

---

## Compatibility & Parameters

PulseShift works for **24V, 36V, and 48V systems** using Li-ion or comparable tool packs.  
- Use a **20 A+ booster** with adjustable CV/CC.  
- Set booster output ~0.5–1 V below the stock pack’s rest voltage.  
- Keep the supercap on the 12V rail only.

---

## Warnings & Safety

- **Risk of fire/injury** — double-check polarity and fuse every line.  
- Use components rated **higher than your peak current**.  
- Each pack must include its own BMS.  
- **Supercap must never connect to the high-voltage bus.**

---

## License

GPL-3.0 — This project is free to use and modify under the same terms.  
See [LICENSE](LICENSE) for the full text.
