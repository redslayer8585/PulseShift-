# PulseShift-
Open-source power management method for safely hot-swapping batteries in mobility and light EV applications. PulseShift isolates keep-alive circuits and drive power paths to extend runtime using common tool batteries.
# PulseShift ⚡

PulseShift is an open-source power management method that enables **safe hot-swapping of tool batteries** for mobility scooters, e-bikes, and other light electric vehicles. By separating the **keep-alive low-power circuits** from the **main drive circuits**, PulseShift allows riders to extend range without shutting down the controller or electronics.

---

## 🚀 Why PulseShift?
- **Continuous Power**: Swap batteries without rebooting the system.
- **Modular Design**: Works with common tool-style battery packs (DeWalt, Makita, etc.).
- **Safety First**: Uses controlled pathways to prevent arcing, surges, or brownouts.
- **Scalable**: Can be applied to scooters, bikes, lawn equipment, and beyond.

---

## 🔧 How It Works
PulseShift uses a **dual-path approach**:
1. **Keep-Alive Path** – a small, isolated supply powers the controller and electronics.  
2. **Drive Path** – the main power path feeds motors, lights, and heavy loads.  

When a battery is removed, the keep-alive path stays active, so the system never resets.  
When a new pack is connected, the drive path re-engages seamlessly.

---

## 📂 Repository Contents
- `README.md` — project overview (this file)  
- `docs/` — technical diagrams, notes, and schematics (to be added)  
- `examples/` — implementation notes and test builds (to be added)  

---

## 🛠️ Applications
- Mobility scooters  
- E-bikes  
- Power wheels conversions  
- Portable power systems  
- Lawn & garden equipment  

---

## 📜 License
This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.  
You are free to use, modify, and share as long as modifications remain open-source.

---

## 🤝 Contributing
Contributions, suggestions, and discussions are welcome!  
Open an Issue or Pull Request to share improvements, ideas, or questions.

---

## 🌱 Roadmap
- [ ] Upload first schematic diagram  
- [ ] Post reference build photos  
- [ ] Add implementation guide for 24V & 36V systems  
- [ ] Expand documentation for advanced features (multi-pack balancing, solar assist)
