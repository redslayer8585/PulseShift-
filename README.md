# PulseShift Technology

**PulseShift** is an open-source power management system designed for safe **hot-swapping of tool batteries** in mobility scooters, e-bikes, and other small EVs.  
By separating **drive power** from a **keep-alive circuit**, the controller stays powered while you swap batteries — avoiding resets, brownouts, or surges.  

This allows users to extend range by swapping in fresh packs (e.g. DeWalt, Ryobi, Bauer, etc.) without shutting down the vehicle.

---

## System Overview

PulseShift uses three key elements:

1. **Main Drive Path** (high current)  
   - Feeds motor controller directly.  
   - Isolated with **ideal diodes** to prevent backfeed between packs.  

2. **Keep-Alive Path** (low current)  
   - Powers controller logic & memory during swaps.  
   - Uses a **buck/boost module** (20A recommended) to maintain stable voltage.  
   - Backed by a **supercapacitor bank (12–16V)** to hold voltage briefly when packs are disconnected.  

3. **User Control / Indicator**  
   - A switch on the keep-alive line to engage/disengage PulseShift.  
   - Optional 12V LED indicator to show keep-alive status.  

---


---

## Supported Voltage Systems

PulseShift is **chemistry-agnostic**. Packs never interact directly — they are isolated by ideal diodes and only feed the system.  

- **48V Systems**  
  - Nominal input: 40–54V (e.g. 13S Li-ion)  
  - Buck/boost module steps down to 12V keep-alive  

- **36V Systems**  
  - Nominal input: 30–42V (e.g. 10S Li-ion)  
  - Buck/boost module steps down to 12V keep-alive  

- **24V Systems**  
  - Nominal input: 20–29V (e.g. 7S Li-ion or lead-acid replacement)  
  - Buck/boost module steps down to 12V keep-alive  

**Current Handling:**  
- Drive path: match motor controller (typically 20–40A for scooters, up to 100A for larger EVs)  
- Keep-alive path: <2A continuous (logic-level only)  

---

## Quick Start Guide

1. **Assemble Modules**
   - Install tool battery adapters.  
   - Wire ideal diodes on each pack output to the drive bus.  
   - Wire buck/boost + supercap bank to keep-alive circuit.  

2. **Install Switch & Indicator**
   - Add a toggle on the 12V keep-alive line.  
   - Wire LED indicator to show circuit activity.  

3. **Power Up**
   - Turn on keep-alive first.  
   - Insert battery pack. Confirm controller wakes.  

4. **Hot-Swap**
   - Add new pack before removing the old.  
   - Controller remains awake via keep-alive.  

---

## Warnings ⚠️

- 🔥 **High Current Risk**: Ensure all wiring, connectors, and diodes are rated above motor peak draw.  
- ⚡ **Polarity Critical**: Reversing tool packs will damage the system. Double-check before plugging in.  
- ❌ **Not a BMS**: Each battery must have its own onboard protection.  
- 🔋 **Supercaps**: Never exceed rated voltage (typically 16V).  
- 🛠️ **Prototype Use Only**: Not certified for commercial EV use.  

---

## License

This project is released under the **GNU General Public License v3.0 (GPL-3.0)**.  
You are free to use, modify, and distribute this project under the same license.  

See [LICENSE](LICENSE) for full details.
