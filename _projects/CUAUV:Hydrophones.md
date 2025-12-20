---
layout: project
title: ENGRD 2210 Portfolio Assignment
description: Thermodynamic Analysis of a Copeland ZR34K3E Scroll Compressor 
image: /assets/images/Compressor.jpg
---

## Thermodynamic Analysis of a Copeland ZR34K3E-PFJ Scroll Compressor


This portfolio entry analyzes a **specific commercial thermodynamic device** using **manufacturer performance data** and the **mass, energy, and entropy balance equations** developed in ENGRD 2210. The goal is to connect thermodynamic theory directly to real engineered hardware.

---

## 1. Device Overview

The Copeland ZR34K3E-PFJ is a **hermetic scroll compressor** widely used in residential air-conditioning systems. Scroll compressors are favored over reciprocating compressors due to their smoother compression process, lower vibration, and improved efficiency.


**Key manufacturer specifications (datasheet):**

| Parameter | Value |
|---------|------|
| Approved refrigerant | R-407C |
| Nominal cooling capacity | 27,000 BTU/hr (7.9 kW) |
| Electrical input power | 2.58 kW |
| Coefficient of performance (COP) | 3.05 |
| Displacement | 8.03 m³/hr |
| Compressor type | Hermetic scroll |

*Sources: Copeland Scroll Compressor distributor datasheets and Elektronika-SA technical data.*

---

## 2. Qualitative Description of Operation

A scroll compressor consists of two interleaved spiral scrolls:
- One fixed scroll
- One orbiting scroll

As the orbiting scroll moves, refrigerant vapor is trapped in crescent-shaped pockets. These pockets gradually decrease in volume, compressing the vapor smoothly until it exits at high pressure near the center.


Unlike piston compressors, this process:
- Eliminates suction and discharge valves
- Reduces pressure pulsations
- Lowers entropy generation
- Improves reliability and efficiency

---

## 3. Control Volume and System Diagram

The compressor is modeled as a **steady-flow control volume**.


**Interactions:**
- **Mass flow:** Refrigerant vapor enters and exits
- **Work:** Electrical work input to the motor
- **Heat:** Heat rejected to surroundings due to inefficiencies

**Assumptions:**
- Steady-state operation  
- Negligible kinetic and potential energy changes  
- Single inlet and single outlet  

---

## 4. Mass Balance

For a steady-flow control volume:

\[
\sum \dot{m}_{in} = \sum \dot{m}_{out}
\]

\[
\dot{m}_{in} = \dot{m}_{out} = \dot{m}
\]

The datasheet does not list mass flow rate directly. It can be estimated using displacement and suction vapor density.

Using:
- Displacement: 8.03 m³/hr  
- Volumetric efficiency (typical): 0.75  
- R-407C suction vapor density (typical): 11 kg/m³  

\[
\dot{m} \approx \frac{8.03}{3600} \times 0.75 \times 11 \approx 0.018 \ \text{kg/s}
\]

This is a **derived value**, not directly provided by the manufacturer.

---

## 5. Energy Balance (First Law)

### General steady-flow energy balance:

\[
0 = \dot{Q} - \dot{W} + \dot{m}(h_1 - h_2)
\]

Rearranged for compressor work input:

\[
\dot{W}_{in} = \dot{m}(h_2 - h_1) + \dot{Q}_{loss}
\]

From datasheet:
\[
\dot{W}_{in} = 2.58 \ \text{kW}
\]

Using R-407C property tables under typical A/C conditions:
- \( h_1 \approx 410 \ \text{kJ/kg} \)
- \( h_2 \approx 450 \ \text{kJ/kg} \)

\[
\dot{m}(h_2 - h_1) = 0.018 \times (450 - 410) \approx 0.72 \ \text{kW}
\]

The remaining input power is lost due to:
- Motor inefficiency
- Mechanical friction
- Heat transfer to ambient

---

## 6. Entropy Balance (Second Law)

The steady-state entropy balance is:

\[
0 = \sum \frac{\dot{Q}}{T} + \dot{m}(s_1 - s_2) + \dot{S}_{gen}
\]

Because compression is irreversible and heat is transferred across a finite temperature difference:

\[
\dot{S}_{gen} > 0
\]

Scroll compressors reduce entropy generation by:
- Maintaining continuous compression
- Minimizing leakage
- Avoiding valve throttling losses

---

## 7. Performance Metric

The coefficient of performance is defined as:

\[
COP = \frac{\dot{Q}_{cooling}}{\dot{W}_{in}}
\]

Using manufacturer values:

\[
COP = \frac{7.9}{2.58} \approx 3.05
\]

This matches the reported datasheet COP, validating the analysis.

---

## 8. Effect of Operating Conditions

### Increased Outdoor Ambient Temperature

Higher ambient temperature raises condenser pressure, increasing the required pressure ratio across the compressor.

**Thermodynamic consequences:**
- Increased \( h_2 - h_1 \)
- Increased compressor work
- Increased entropy generation
- Reduced COP

If power increases to 3.0 kW while cooling capacity remains constant:

\[
COP = \frac{7.9}{3.0} \approx 2.63
\]

This represents a **~14% efficiency reduction**, consistent with real air-conditioning behavior on hot days.

---

## 9. Engineering Significance

This analysis demonstrates how:
- Manufacturer datasheets encode thermodynamic behavior
- Control-volume equations predict real device performance
- The Second Law explains efficiency limits
- Design choices directly affect entropy generation

This same framework applies broadly to HVAC, aerospace thermal systems, and energy engineering.

---

## 10. Sources

- Copeland ZR34K3E-PFJ performance data:  
  https://copelandscrollcompressor.com/ZR34K3E-PFJ-details.php
- Elektronika-SA technical datasheet:  
  https://www.elektronika-sa.com.pl/en/products/refrigeration/compressors/scroll/zr/ZR34K3E-PFJ/v/ZR34K3E-PFJ
- ASHRAE refrigerant property tables (R-407C)



