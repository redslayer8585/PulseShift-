# PulseShift ⚡ — Single 40V Pack

**PulseShift** is an open, non-invasive way to run a mobility/EV controller from a **single 40V tool battery** (≈36V nominal) while enabling:
- A **High (Drive) path** via a buck/boost set just below the stock bus so it assists only under sag, protected by an **ideal-diode** (no backfeed).
- A **Low (Keep-Alive) path** via a **40→12V converter** feeding a diode-isolated **supercap bank** + indicator, so the controller/aux rails stay alive during swaps.

No series-stacking required. Chemistry-agnostic because packs never “see” each other.

---

## Wiring Diagram

[![PulseShift Wiring Diagram](docs/wiring-diagram.svg)](docs/wiring-diagram.svg)

**Legend**
- 🔴 High Path (Drive) — 40V → Buck/Boost (DROK) → Ideal Diode → Controller +
- 🔵 Low Path (Input) — 40V feed into 40→12V converter
- 🟡 12V Keep-Alive Rail — switch → diode → supercaps → 12V indicator
- ⚫ Common Ground — shared return, keep 12V isolated from HV rail

---

## How It Works (Bias Assist)

1. **Set the booster’s output just below the controller bus at rest.**  
   - 36V systems: set **≈ 36.0–39.5 V**  
   - 48V systems: **boost** to **≈ 48.5–52.5 V**  
   The ideal-diode prevents backfeeding the 40V pack. Under load, when the stock bus sags below the set-point, the booster **automatically contributes current**.

2. **Keep-Alive stays 12 V only.**  
   A “golf cart” 40→12 V reducer feeds a diode-isolated supercap bank to bridge swaps and power accessories/logic. The supercaps never see pack voltage.

---

## Quick Start

1. **Battery & adapter**
   - Use a fused 40V tool-battery adapter (e.g., Power Wheels-style sled), correct polarity.

2. **High Path (Drive)**
   - 40V → **DROK buck/boost** → **ideal-diode ORing** → controller + bus.
   - Set DROK OUT **just below** the bus voltage at rest (see above table).

3. **Low Path (Keep-Alive)**
   - 40V → **40→12 V converter** → **switch** → **diode** → **12–16 V supercap bank** → 12V indicator/aux.
   - This path powers logic/aux and holds the rail up during battery swaps.

4. **Swap procedure**
   - Flip **keep-alive switch OFF** → swap 40V battery → switch **ON** → ride.
   - The diode + supercap keep the 12V rail alive while the pack is out.

---

## Parameters & Requirements

- **Battery:** 40V tool pack (≈36V nominal). Smaller (18/20V max) packs will struggle here.
- **Booster (High Path):** Buck/boost 6–70 V, ≥20 A (DROK w/ LCD recommended).  
  Set ≈0.5–1.0 V **below** rest bus so it never charges the stock pack at idle.
- **Ideal Diode:** Low Rds(on), sized above expected **peak** controller current.
- **Low Path Converter:** 40→12 V reducer (often sold as “golf cart reducer”), ≥10–20 A if accessories are used.
- **Supercaps:** 12–16 V rated, **on 12 V rail only**, through a diode (hold-up only).

---

## Safety & Warnings

- 🔥 **High current/voltage:** Fuse both the 40V sled and the 12V rail. Use wiring/connectors rated above peak motor current.
- ⚡ **Polarity critical:** Double-check before power-up. The ideal-diode only protects the high path from backfeed, not reverse polarity.
- 🧯 **No cross-charging:** PulseShift isolates sources; do **not** attempt to charge packs through the bus.
- 🔋 **Supercap caution:** Never exceed voltage rating; keep them **off** the high-voltage path.
- 🛠️ Prototype project; build/use at your own risk.

---

## Notes on “Agnostic” Support

PulseShift’s topology is chemistry-agnostic because sources don’t interact directly.  
However, **this design expects a 40V pack** as the energy source. Smaller 18/20V-max drill packs are under-spec’d for this build and will sag or over-stress the booster.

---

## License

GPL-3.0 — open, remixable, and protected for the community. See [LICENSE](LICENSE).
