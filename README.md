# Reservoir Engineering Simulation – Water & CO₂ Injection (MRST)

This project simulates **Enhanced Oil Recovery (EOR)** in a synthetic 2D reservoir using simultaneous **water** and **CO₂ injection**.

Built with the [MRST (MATLAB Reservoir Simulation Toolbox)](https://www.sintef.no/projectweb/mrst/), this model demonstrates three-phase flow behavior using the `ThreePhaseBlackOilModel`.

---

## 🎯 Objectives

- Model a synthetic reservoir with basic rock and fluid properties.
- Inject water and CO₂ from different locations.
- Track oil displacement and visualize saturation evolution.
- Serve as a portfolio project for reservoir engineering candidates.

---

## 🛠️ Model Setup

- **Grid**: 60 × 40 cells (600 × 400 m)
- **Cell Size**: 10 × 10 m
- **Rock**:
  - Porosity: 0.2
  - Permeability: 100 mD
- **Fluids** (Three-Phase):
  - Water: μ = 1 cP, ρ = 1000 kg/m³
  - Oil: μ = 5 cP, ρ = 700 kg/m³
  - CO₂: μ = 0.06 cP, ρ = 600 kg/m³

---

## 🔁 Simulation Strategy

- **Initial Pressure**: 100 bar
- **Initial Saturation**: 100% oil-filled
- **Injectors**:
  - Water: top-left corner
  - CO₂: top-right corner
- **Producer**: middle of bottom boundary
- **Schedule**: 10 timesteps over 200 days

---

## 📊 Result – Time Step 10

At timestep 10, the injected fluids have migrated through the reservoir, displacing oil toward the producer.

![Water_CO₂](Water_CO₂ _t10.png)

- Left: Water Saturation
- Middle: Oil Saturation
- Right: CO₂ Saturation

---

## ▶️ How to Run

1. Install MRST 2025a and ensure these modules are loaded:
   ```matlab
   mrstModule add ad-core ad-blackoil mrst-gui
   ```
2. Open `water_co2_injection_simulation.m` and run.

---

## 📁 Files

- `water_co2_injection_simulation.m`: Main simulation script
- `Water_CO₂ _t10.png`: Final saturation plots
- `README.md`: Project overview

---

## 📌 Notes

- Uses **ThreePhaseBlackOilModel** from MRST.
- Ideal for **portfolio, academic demonstrations**, or **interviews** in upstream oil & gas.