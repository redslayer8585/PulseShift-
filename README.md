# PulseShift
![1000002996](https://github.com/user-attachments/assets/58b5ee72-980e-46b7-9ede-4695939550a3)

# ⚡ PulseShift  

**Unlimited range mobility, powered by hot-swappable tool batteries.**  

PulseShift is an open-source hardware project licensed under **GPL-3.0**. The goal: take a cheap, consumer-grade mobility scooter and free it from proprietary 10-mile battery packs — replacing them with an open system that runs on common **Ryobi / Bauer 40V tool batteries**, supercapacitors, and modular converters.  

If you’ve ever been burned by planned obsolescence, overpriced OEM packs, or “smart” BMS lockouts, this project is for you.  

---

## 🚀 Why PulseShift?  
- **Unlimited range** — hot-swap tool packs as you go.  
- **Open design** — GPL-licensed, fork it, extend it, make it yours.  
- **Modular wiring** — DROK converters, ideal diodes, cap banks, and 12V rails.  
- **Non-invasive** — designed to preserve warranties by avoiding frame/controller mods.  
- **Community-first** — not a secret hack, but a public blueprint anyone can repeat.  

---

## 📂 What’s Here  
- **Wiring Diagram/** — reference layouts for the booster, 12V accessory rail, supercap banks, and diode paths.  
- **README.md** — (you are here).  
- **LICENSE** — GPL-3.0, ensuring this project stays free and open.  

---

## 🛠️ Core Concepts  
- **Ryobi / Bauer 40V Packs** → swappable energy “cartridges” (4Ah–12Ah, fully modular).  
- **DROK CC/CV Converter** → manages output voltage just below OEM pack sag point.  
- **Ideal Diode OR-ing** → smooth, safe handoff between packs.  
- **12V Accessories Path** → golf cart-style buck + Schottky for lights, fans, and USB.  
- **Supercap Buffers** → optional keep-alive during swaps, smoothing ripple and surge.  

---

## ⚡ Quick Start  

### 🔩 Parts List (baseline build)  
- 1× **Vevor 3-wheel scooter** (or similar, 48V base pack).  
- 1× **Ryobi / Bauer battery adapter** (XT60 pigtail preferred).  
- 1–N× **Ryobi/Bauer 40V batteries** (4Ah, 6Ah, 9Ah, 12Ah).  
- 1× **DROK CC/CV Boost Converter** (20A, 0–60V output).  
- 1× **Golf cart-style 48→12V buck converter** (20A+ recommended).  
- 2× **Ideal diode modules** (industrial, low-drop).  
- 1× **Schottky diode** (≥20A) for the 12V rail.  
- (Optional) 1× **Supercap bank** (16V, 83F or 5.5V 30–50F modules).  
- XT60 connectors, 12–16 AWG silicone wire, fuse holders, heatshrink, M10 stainless inserts for mounting.  

### 🔌 High-Level Wiring Steps  
1. **Stock pack stays in place** → keep it as OEM baseline.  
2. **Add XT60 pigtail** to OEM pack leads.  
3. **Range boost path:**  
   - Ryobi/Bauer adapter → DROK (set ~1V below OEM nominal) → ideal diode → OEM battery line.  
   - This ensures OEM pack runs first, booster only kicks in on sag.  
4. **12V accessories path:**  
   - Ryobi/Bauer adapter → golf cart buck → Schottky diode → 12V accessory rail.  
5. **Optional supercap buffer:**  
   - Supercap across input rail → pre-charge resistor or NTC inline → acts as keep-alive during swaps.  
6. **Test and tune:**  
   - Verify DROK CV setting just under OEM pack voltage.  
   - Confirm diodes prevent back-feed.  
   - Confirm 12V rail is stable under accessory load.  

---

## 🔓 The Philosophy  
PulseShift exists because we refuse lock-ins.  

- **Desert Vape era**: making VG-heavy juice when OEM gear was junk.  
- **BYFO mods**: building mech tubes and PWM boards that outlived consumer junk.  
- **PulseShift**: scaling that same spirit into mobility and energy freedom.  

This project is proof that open knowledge + open tools let individuals build what corporations say is impossible.  

---

## 📜 License  
This project is licensed under the **GNU General Public License v3.0** — meaning it stays open, forkable, and free forever.
