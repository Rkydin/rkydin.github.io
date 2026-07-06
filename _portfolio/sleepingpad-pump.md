---
title: "UltraLight Sleeping Pad Pump"
excerpt: "Compact, lightweight inflator for backpacking sleeping pads."
category: "Outdoor Gear"
collection: portfolio
layout: portfolio
author_profile: true
share: false
header:
  teaser: /images/sleepingpad-pump/v3-full-assembly.jpg
---

<style>
.page__share {
  display: none !important;
}
</style>

**Project Duration:** November 2025 - Present
**Status:** V3 in progress

## Project Overview

Designed and built a portable, ultralight pump for inflating sleeping pads during backpacking trips. The pump is now on its third revision — moving from off-the-shelf electronics and a simple single-piece shell toward a custom PCB and a sealed, three-piece housing.

## Design Requirements

* **Under 100 g total** — this is the line for the pump to count as genuinely "ultralight."
* **As cheap as possible without sacrificing performance** — not just cheap for its own sake.
* **Durable enough for repeated outdoor use** — UV exposure, moisture, and general pack abuse.

## V3: Custom PCB, Sealed Three-Piece Housing

<div style="margin: 30px 0;">
  <img src="/images/sleepingpad-pump/v3-full-assembly.jpg" alt="V3 full assembly render" style="width: 100%; max-width: 600px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>V3 full assembly</em></p>
</div>

V3 replaces v2's off-the-shelf blower fan and USB-C trigger board with a custom coreless motor and 3D-printed impeller driven by a custom-designed PCB. The fan is now **inline with the inlet and outlet** instead of diverted off to the side. The housing was already sealed, but air now has to cross one more wall to leak — the middle spacer piece between the top and bottom covers — making the assembly harder to leak through than before.

### Housing Design

<div style="margin: 30px 0;">
  <img src="/images/sleepingpad-pump/v3-exploded-bom.jpg" alt="V3 exploded view with parts callouts" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Exploded view — top cover, impeller, mating spacer, PCB, USB-C breakout, motor, bottom cover</em></p>
</div>

The housing splits into three 3D-printed parts:

* **Top cover** — the inlet, seats the impeller.
* **Middle piece (mating spacer)** — suspends the motor, fan, and PCB in the center of the assembly. It does three jobs at once: adds structural rigidity, seals against the top and bottom covers, and keeps the electronics physically isolated from the fan and airflow path.
* **Bottom cover** — the outlet and structural base.

Where the top, middle, and bottom sections meet, the parts sandwich together — that contact point is what makes this housing meaningfully harder to leak air through than a simpler shell.

Printed in **PETG** instead of PLA: PLA degrades under UV exposure and over time, while PETG is more chemically resistant and more durable — a better fit for something that lives in a backpack and goes outside.

### Custom Electronics

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 20px; margin: 30px 0;">
  <div>
    <img src="/images/sleepingpad-pump/v3-pcb-front.png" alt="V3 PCB front, component view" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>PCB — front (component side)</em></p>
  </div>
  <div>
    <img src="/images/sleepingpad-pump/v3-pcb-back.png" alt="V3 PCB back, trace view" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>PCB — back (traces)</em></p>
  </div>
</div>

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 20px; margin: 30px 0;">
  <div>
    <img src="/images/sleepingpad-pump/v3-pcb-layout.png" alt="V3 PCB layout / routing view" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>PCB layout and routing</em></p>
  </div>
  <div>
    <img src="/images/sleepingpad-pump/v3-pcb-schematic.png" alt="V3 circuit schematic" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Circuit schematic</em></p>
  </div>
</div>

V2 leaned on an off-the-shelf USB-C PD trigger board to avoid designing a custom PCB. V3 replaces that with a purpose-built 2-layer board (designed in KiCad) that takes USB-C VBUS/GND directly and handles:

* **Overcurrent protection** — a polyfuse on the input.
* **Motor kickback protection** — an SS34 flyback diode across the motor terminals.
* **Power smoothing** — 220 µF, 10 µF, and 0.1 µF capacitors to reduce motor-induced voltage dips and noise.
* **USB-C power detection** — CC1/CC2 pull-down resistors so the port negotiates power correctly without a data connection.

### Bill of Materials (V3)

| Component | Qty | Cost | Weight | Purpose |
|---|---|---|---|---|
| Custom 2-layer PCB | 1 | $6.14 | ~2.4 g | Electrical integration |
| USB-C breakout | 1 | $2.95 | 1.3 g | Power input |
| 8520 coreless motor | 1 | $2.45 | ~5.0 g | Fan drive |
| Polyfuse | 1 | $0.38 | ~0.2 g | Overcurrent protection |
| Flyback diode | 1 | $0.64 | 0.064 g | Motor kickback protection |
| Capacitors | 3 | $0.98 | ~0.45 g | Power filtering |
| PETG printed parts | 4 | $0.60 | 21.24 g | Housing/structure |
| M2 screws | 3 | $1.42 | ~0.78 g | Assembly fastening |
| **Total** | | **$15.56** | **~31.44 g** | |

## Design Evolution

### V1 — Early Prototype

Initial working prototype with a basic nozzle attachment.

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 30px 0;">
  <div>
    <img src="/images/sleepingpad-pump/pump.png" alt="Early prototype - front" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Early prototype - front view</em></p>
  </div>
  <div>
    <img src="/images/sleepingpad-pump/pumpback.png" alt="Early prototype - back" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Early prototype - back view</em></p>
  </div>
</div>

<div style="margin: 30px 0;">
  <img src="/images/sleepingpad-pump/nozzle.png" alt="Nozzle CAD design" style="width: 100%; max-width: 600px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>CAD model of initial nozzle design</em></p>
</div>

### V2 — Off-the-Shelf Electronics

Refined design with an interchangeable nozzle system, USB-C charging, and a single-piece PLA housing — but built around an off-the-shelf blower fan and USB-C trigger board rather than custom electronics.

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 30px 0;">
  <div>
    <img src="/images/sleepingpad-pump/thermarestfront.png" alt="Final pump with Thermarest nozzle - front" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>V2 with Thermarest nozzle</em></p>
  </div>
  <div>
    <img src="/images/sleepingpad-pump/thermarestback.png" alt="Final pump - back view" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Back view showing USB-C port</em></p>
  </div>
</div>

<div style="margin: 30px 0;">
  <img src="/images/sleepingpad-pump/expedfront.png" alt="Pump with Exped nozzle" style="width: 100%; max-width: 600px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Alternative nozzle for Exped valves</em></p>
</div>

**V2 Bill of Materials**

| Component | Part / Spec | Qty | Cost | Weight | Why This Spec |
|---|---|---|---|---|---|
| Blower fan | Wathai 30×10mm, 5V, 9500 RPM, 1.85 CFM, 29 dBA | 1 | $5.00 | ~4.75 g | 5V USB-compatible, compact, integrated fan + motor + housing |
| USB-C trigger module | USB-C PD trigger board | 1 | $6.00 | ~0.46 g | Off-the-shelf power board; avoids custom PCB for V1 |
| Printed casing | PLA printed housing | 1 | $0.32 | 12.69 g | Cheap, fast to print, good enough for first prototype |
| **Total** | | | **$11.32** | **~17.9 g** | |

## Final Specifications

**Weight:**
* V3 total: ~31.44 g — comfortably under the 100 g ultralight requirement.
* For reference, ~30 g is roughly: 6 nickels, 12 US pennies, 1½ AA batteries, 6 sheets of paper, or 30 g of feathers.

**Cost:**
* V3: $15.56 (up from $11.32 in V2 — the difference buys a sealed housing and a custom PCB instead of an off-the-shelf trigger board).

**Performance:**
* Inflation time: ~12 minutes for a medium sleeping pad.
* Power: USB-C.
* Compatible with Thermarest and Exped valves.

## Technologies Used

* SolidWorks CAD modeling
* Custom PCB design (KiCad) — schematic capture, layout, and routing
* Centrifugal impeller design
* 3D printing (PETG)
* USB-C power circuitry — overcurrent protection, motor kickback protection, power filtering
* Fan selection and airflow optimization

## Future Improvements

* Validate the sandwich seal with section-view inspection.
* Keep chasing weight and cost down without giving up the sealed housing.
* Additional nozzle designs for other valve types.
