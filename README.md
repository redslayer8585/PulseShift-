# PulseShift

<p align="center">
  <img src="assets/logo.png" alt="PulseShift Logo" width="300"/>
</p>

### *Liberating Energy*

---

## 🚀 What is PulseShift?
PulseShift is an **open-source power-handling system** that extends the range of mobility devices (like scooters) without modifying the OEM battery system.  
It uses **classic diode OR-ing** for **passive handoff** between the stock battery and an auxiliary pack, so the extra source only engages when the main pack sags.

Think of it as the **Robin Hood of power systems**:  
- Simple
- Cheap
- Chemistry-agnostic
- Proven in telecom and aerospace — now applied to personal mobility.

---

## ⚡ How it Works
- A **Ryobi 40V pack** is connected in parallel to the scooter’s main battery.  
- A **DROK buck/boost converter** stabilizes voltage for a clean handoff.  
- A **power diode** isolates the paths, ensuring the main battery is always primary.  
- When the stock pack sags, PulseShift seamlessly supplies supplemental current.  

<p align="center">
  <img src="assets/diagram.png" alt="PulseShift Diagram" width="500"/>
</p>

---

## ✅ Why PulseShift?
- 🔋 **Seamless extra range** — no mods to OEM wiring  
- ⚙️ **Open-source design** — schematics and parts list included  
- 💡 **Educational** — a living demo of energy-sharing principles  
- 🔧 **Scalable** — from scooters to other DC systems  

---

## 📂 Repository Structure
- `/hardware` — Schematics, wiring diagrams, BOM  
- `/firmware` — (optional) Any microcontroller logic  
- `/docs` — Guides, whitepapers, design notes  
- `/assets` — Logos, diagrams, media  

---

## 🌐 Join the Project
PulseShift is **open-source and community-driven**.  
- Share your builds  
- Contribute improvements  
- Adapt it for your own use case  

Together, we’re **liberating energy**.  

---
