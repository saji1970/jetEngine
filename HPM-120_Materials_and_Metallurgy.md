# HPM-120 — Materials and Metallurgy Guide

---

## 1. MATERIALS SUMMARY BY COMPONENT

### Engine Architecture

Inlet → Rotating Detonation Annulus → MHD Generator → MHD Accelerator → C-D Nozzle

### Master Materials List

| # | Component | Primary Material | Secondary/Coating | Max Temp (K) |
|---|---|---|---|---|
| 1 | Intake cowl | Ti-6Al-4V (Grade 5) | — | 600 |
| 2 | Intake centerbody | Ti-6Al-4V | — | 800 |
| 3 | Diffuser duct | Ti-6Al-4V | — | 600 |
| 4 | RDE outer shell | Inconel 718 | — | 1,100 |
| 5 | RDE inner liner | C/SiC composite | ZrO₂ TBC (0.5 mm) + EBC | 1,800 |
| 6 | RDE injector face plate | Inconel 625 | — | 1,100 |
| 7 | Plasma igniter waveguide (1x) | C10100 OFHC Copper | — | 400 |
| 8 | MHD Generator channel walls | C/SiC composite | ZrO₂ TBC (0.5 mm) | 1,800 |
| 9 | MHD Generator electrodes | W-Cu composite (80/20) | — | 1,500 |
| 10 | MHD Generator insulators | Boron Nitride (BN) | — | 1,800 |
| 11 | MHD Generator magnet coils | NbTi superconductor | Cryostat (SS304) | <10 (cryo) |
| 12 | MHD Generator cryostat | 304 Stainless Steel | MLI insulation | 77-300 |
| 13 | MHD Accelerator channel walls | C/SiC composite | ZrO₂ TBC (0.5 mm) | 1,800 |
| 14 | MHD Accelerator electrodes | W-Cu composite (80/20) | — | 1,500 |
| 15 | MHD Accelerator insulators | Boron Nitride (BN) | — | 1,800 |
| 16 | MHD Accelerator magnet coils | NbTi superconductor | Cryostat (SS304) | <10 (cryo) |
| 17 | MHD Accelerator cryostat | 304 Stainless Steel | MLI insulation | 77-300 |
| 18 | Nozzle inner wall | C/SiC composite | ZrO₂ TBC (0.5 mm) | 1,800 |
| 19 | Nozzle outer shell | Inconel 718 | — | 1,000 |
| 20 | Mounting brackets | Inconel 718 | — | 900 |
| 21 | Fasteners | A-286 or Inconel 718 | — | 900 |
| 22 | Seals | Inconel X-750 (C-seals) | — | 1,000 |

---

## 2. DETAILED MATERIAL SPECIFICATIONS

### 2.1 Titanium Ti-6Al-4V (Grade 5)

**Used in:** Intake cowl, centerbody, diffuser duct

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 4,430 kg/m³        |
| Yield strength        | 880 MPa            |
| UTS                   | 950 MPa            |
| Elastic modulus       | 114 GPa            |
| Max service temp      | 600 K (315°C)      |
| Thermal conductivity  | 6.7 W/m·K          |
| CTE                   | 8.6 × 10⁻⁶ /K    |
| Melting point         | 1,933 K            |

**Composition:**
- Ti: Balance (~90%)
- Al: 5.5 - 6.75%
- V: 3.5 - 4.5%
- Fe: < 0.3%
- O: < 0.2%

**3D Printing Parameters (EBM / SLM):**
- Powder size: 45 - 106 μm (EBM) or 15 - 45 μm (SLM)
- Layer thickness: 50 - 100 μm
- Build temperature: 700°C (EBM preheat)
- Atmosphere: Vacuum (EBM) or Argon (SLM)
- Post-processing: HIP at 920°C / 100 MPa / 2 hr
- Heat treatment: Stress relief 650°C / 3 hr, furnace cool

### 2.2 Inconel 718

**Used in:** RDE annulus outer shell, nozzle outer shell, mounting brackets, fasteners

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 8,190 kg/m³        |
| Yield strength (RT)   | 1,035 MPa          |
| Yield strength (650°C)| 860 MPa            |
| UTS (RT)              | 1,240 MPa          |
| Elastic modulus       | 200 GPa            |
| Max service temp      | 980 K (700°C)      |
| Thermal conductivity  | 11.4 W/m·K         |
| CTE                   | 13.0 × 10⁻⁶ /K   |
| Melting range         | 1,533 - 1,609 K    |

**Composition:**
- Ni: 50 - 55%
- Cr: 17 - 21%
- Fe: Balance (~18%)
- Nb + Ta: 4.75 - 5.50%
- Mo: 2.8 - 3.3%
- Ti: 0.65 - 1.15%
- Al: 0.2 - 0.8%

**3D Printing Parameters (DMLS / SLM):**
- Powder size: 15 - 45 μm
- Layer thickness: 20 - 40 μm
- Laser power: 280 - 400 W
- Scan speed: 800 - 1,200 mm/s
- Hatch spacing: 0.10 - 0.12 mm
- Build atmosphere: Argon (O₂ < 100 ppm)
- Post-processing: HIP at 1,165°C / 100 MPa / 4 hr
- Heat treatment:
  - Solution: 980°C / 1 hr / air cool
  - Age: 720°C / 8 hr → furnace cool to 620°C / 8 hr → air cool

### 2.3 Inconel 625

**Used in:** RDE injector face plate

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 8,440 kg/m³        |
| Yield strength        | 490 MPa            |
| UTS                   | 965 MPa            |
| Max service temp      | 1,100 K (815°C)    |
| Thermal conductivity  | 9.8 W/m·K          |

**Composition:**
- Ni: 58% min
- Cr: 20 - 23%
- Mo: 8 - 10%
- Nb + Ta: 3.15 - 4.15%

**3D Printing Parameters (SLM):**
- Powder size: 15 - 45 μm
- Layer thickness: 20 - 40 μm
- Laser power: 250 - 370 W
- Post-processing: Stress relief 870°C / 1 hr

### 2.4 C/SiC Composite (Carbon fiber / Silicon Carbide matrix)

**Used in:** RDE annulus inner liner, MHD Generator channel walls, MHD Accelerator channel walls, nozzle inner wall

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 2,100 - 2,500 kg/m³|
| Tensile strength      | 250 - 400 MPa      |
| Compressive strength  | 400 - 600 MPa      |
| Max service temp      | 1,800 K (1,500°C)  |
| Thermal conductivity  | 15 - 40 W/m·K      |
| CTE                   | 2 - 4 × 10⁻⁶ /K   |
| Oxidation resistance  | Good with coating   |

**Manufacturing Methods:**
- NOT suitable for standard metal 3D printing
- Made via Chemical Vapor Infiltration (CVI):
  1. Carbon fiber preform woven/laid up to shape
  2. Preform placed in CVI reactor
  3. Methyltrichlorosilane (MTS) gas infiltrated at 1,000 - 1,100°C
  4. SiC matrix deposited within fiber preform
  5. Process repeated until target density reached (~85-95%)
  6. Typical cycle: 100 - 500 hours per infiltration cycle
  7. Final machining to tolerance

- Alternative: Polymer Infiltration and Pyrolysis (PIP)
  1. Carbon preform infiltrated with polycarbosilane
  2. Pyrolyzed at 1,200 - 1,400°C
  3. Multiple cycles (6-10) to reach target density

**Suppliers:** Safran Ceramics, CoorsTek, GE CMC facilities

### 2.5 C10100 OFHC Copper

**Used in:** Plasma igniter waveguide (1x)

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 8,940 kg/m³        |
| Electrical conductivity| 101% IACS         |
| Thermal conductivity  | 391 W/m·K          |
| Yield strength        | 69 MPa (annealed)  |
| Max service temp      | 400 K (under load) |

**Manufacturing:** CNC machined from bar stock (not 3D printed)

### 2.6 Tungsten-Copper (W-Cu 80/20) Composite

**Used in:** MHD Generator electrodes, MHD Accelerator electrodes

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 15,200 kg/m³       |
| Electrical conductivity| 40% IACS          |
| Thermal conductivity  | 180 W/m·K          |
| Hardness              | 260 HV             |
| Max service temp      | 1,500 K            |

**Manufacturing:**
- Press and sinter: W powder skeleton sintered, Cu infiltrated
- Cannot be conventionally melted (W melts at 3,695 K, Cu at 1,358 K)
- Shape via EDM (Electrical Discharge Machining) after sintering

### 2.7 Boron Nitride (BN) — Hot-Pressed

**Used in:** MHD Generator channel insulators, MHD Accelerator channel insulators

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 1,900 kg/m³        |
| Dielectric strength   | 40 kV/mm           |
| Max service temp      | 1,800 K (inert)    |
| Thermal conductivity  | 30 W/m·K (∥ press) |
| Electrical resistivity| > 10¹⁴ Ω·cm       |

**Manufacturing:** CNC machined from hot-pressed BN billets
- Supplier: Saint-Gobain, Momentive, Kennametal

### 2.8 316L Stainless Steel

**Used in:** Non-critical structural parts

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 7,990 kg/m³        |
| Yield strength        | 290 MPa            |
| UTS                   | 560 MPa            |
| Max service temp      | 700 K              |

**3D Printing Parameters (SLM):**
- Powder size: 15 - 45 μm
- Layer thickness: 20 - 50 μm
- Laser power: 200 - 370 W
- Build atmosphere: Argon or Nitrogen
- Post-processing: Stress relief 650°C / 2 hr

### 2.9 ZrO₂ Thermal Barrier Coating (Yttria-Stabilized Zirconia, 8YSZ)

**Used in:** Inner surface of RDE annulus liner, MHD Generator channel walls, MHD Accelerator channel walls, nozzle inner wall

| Property              | Value              |
|-----------------------|--------------------|
| Thermal conductivity  | 1.5 - 2.0 W/m·K   |
| CTE                   | 10 × 10⁻⁶ /K     |
| Max surface temp      | 1,500 K            |
| Coating thickness     | 0.5 mm             |

**Application Method:**
- Air Plasma Spray (APS) for thick coatings
- Electron Beam Physical Vapor Deposition (EB-PVD) for thin, strain-tolerant coatings
- Bond coat: NiCrAlY (0.1 mm) applied first via HVOF spray

### 2.10 UHTC — Ultra-High Temperature Ceramics (Future Upgrade Path)

The Rotating Detonation Annulus produces gas temperatures of 3,500 - 4,000 K, which
exceed the service limits of C/SiC (1,800 K). While the baseline design relies on
TBC + EBC + regenerative cooling to keep wall temperatures within C/SiC limits, UHTC
materials are identified as potential future upgrades if thermal management proves
insufficient.

**HfC (Hafnium Carbide):**

| Property              | Value              |
|-----------------------|--------------------|
| Melting point         | 4,232 K            |
| Density               | 12,200 kg/m³       |
| Thermal conductivity  | 20 W/m·K           |
| Hardness              | 26 GPa (Vickers)   |

- Candidate for RDE throat regions and annulus hot-side liners
- Extremely high melting point enables operation near detonation temperatures
- Brittle; requires careful structural design or composite reinforcement (e.g., HfC-SiC)

**ZrB₂ (Zirconium Diboride):**

| Property              | Value              |
|-----------------------|--------------------|
| Max service temp      | ~2,500 K           |
| Density               | 6,100 kg/m³        |
| Thermal conductivity  | 60 W/m·K           |
| Oxidation resistance  | Good with SiC additive (ZrB₂-SiC) |

- Oxidation-resistant when combined with 20 vol% SiC particulate
- Forms protective ZrO₂ + SiO₂ glassy layer in oxidizing environments
- Candidate for RDE annulus liner upgrade if C/SiC proves marginal

**Note:** Both HfC and ZrB₂ are currently limited by manufacturing maturity and cost.
Spark Plasma Sintering (SPS) is the preferred densification route. These materials
should be considered Phase 2 upgrades pending thermal validation of the C/SiC baseline.

---

## 3. THERMAL BARRIER AND COATING SYSTEM

```
WALL CROSS-SECTION (RDE annulus / MHD channels / nozzle):

HOT GAS SIDE (3,500 - 4,000 K in RDE; 2,500 - 3,200 K in MHD/nozzle)
    │
    ▼
┌──────────────────────┐
│  ZrO₂ TBC (0.5 mm)  │  ← Thermal barrier
├──────────────────────┤
│  EBC layer           │  ← Environmental barrier (RDE: mandatory)
│  (0.05 - 0.1 mm)    │
├──────────────────────┤
│  NiCrAlY bond coat   │  ← Oxidation barrier (0.1 mm)
│  (0.1 mm)            │
├──────────────────────┤
│  C/SiC liner         │  ← Structural + insulating (5-8 mm)
│  (5 - 8 mm)          │
├──────────────────────┤
│  Cooling channel     │  ← Fuel or water (3-4 mm gap)
│  (3 - 4 mm)          │
├──────────────────────┤
│  Inconel 718 shell   │  ← Pressure vessel (4-6 mm)
│  (4 - 6 mm)          │
└──────────────────────┘
    │
    ▼
COLD SIDE (~400 - 600 K)

Total wall thickness: 16 - 24 mm
```

**RDE-specific coating notes:** The RDE annulus liner requires a full EBC (Environmental
Barrier Coating) system in addition to the ZrO₂ TBC. The EBC typically consists of a
mullite or rare-earth silicate layer (e.g., Yb₂Si₂O₇) applied between the bond coat
and the TBC. This prevents steam-induced recession of the SiC matrix at elevated
temperatures. All MHD and nozzle sections also benefit from EBC but may operate with
TBC-only at reduced gas temperatures.

---

## 4. MATERIAL COMPATIBILITY AND JOINING

### Joining Methods Between Dissimilar Materials

| Joint                          | Method                         |
|--------------------------------|--------------------------------|
| Ti-6Al-4V to Inconel 718      | Diffusion bonding or bolted    |
| C/SiC to Inconel 718          | Mechanical (spring clips/seals)|
| Inconel 718 to Inconel 718    | TIG weld (Inconel 625 filler)  |
| W-Cu electrodes to BN         | Mechanical (clamped)           |
| C/SiC to ZrO₂ TBC            | Plasma spray (direct)          |
| Inconel 625 to Inconel 718    | TIG weld (Inconel 625 filler)  |

### Critical Notes on Material Selection

1. **C/SiC at RDE detonation temperatures (3,500 - 4,000 K).** The Rotating
   Detonation Annulus produces gas temperatures far exceeding C/SiC service limits
   (1,800 K). The TBC + EBC + regenerative cooling system must reduce wall
   temperatures below 1,800 K. If thermal analysis shows insufficient margin,
   fallback options include:
   - UHTC liners (HfC or ZrB₂-SiC) for the annulus hot-side
   - Active transpiration cooling through porous C/SiC walls
   - Hybrid designs with UHTC face layer bonded to C/SiC structural backing

2. **RDE thermal cycling.** Detonation waves rotate through the annulus at
   approximately 1,500 - 2,000 Hz, creating rapid thermal cycling on the annulus
   walls. This is far more severe than steady-state combustion loading. All annulus
   liner materials and coatings must be validated for thermal fatigue resistance
   under pulsed heating at these frequencies. Coating adhesion under cyclic thermal
   shock is a primary failure mode to monitor.

3. **C/SiC degrades in steam-rich environments.** Combustion of hydrocarbon fuel
   produces H₂O. The SiC matrix reacts with H₂O above 1,200°C to form Si(OH)₄
   gas. The ZrO₂ TBC and environmental barrier coating (EBC) are essential,
   especially in the RDE annulus where both temperature and steam partial pressure
   are highest.

4. **Inconel 718 loses strength above 700°C.** For regions exceeding this, use
   Haynes 230 (max 1,150°C) or Inconel 625 as alternatives. The RDE outer shell
   operates at up to 1,100 K (827°C), which is above the standard IN718 limit of
   980 K. Active cooling of the outer shell or substitution with Haynes 230 may
   be required if regenerative cooling is insufficient.

5. **Alkali seed contamination.** K or Cs salts used for MHD conductivity seeding
   (in both the MHD Generator and MHD Accelerator) are corrosive to some materials.
   W-Cu electrodes and BN insulators are resistant. Ni-superalloy surfaces in the
   MHD sections need protective coatings.

6. **Thermal expansion mismatch.** C/SiC (CTE ~3 × 10⁻⁶/K) vs Inconel 718
   (CTE ~13 × 10⁻⁶/K) creates severe mismatch. Use compliant seals (Inconel
   X-750 C-seals or ceramic rope packing) at all liner-to-shell interfaces.
   Never bond them rigidly. This applies at all C/SiC-to-IN718 joints: RDE
   annulus, MHD Generator, MHD Accelerator, and nozzle.

---

## 5. MATERIAL SOURCING NOTES

| Material            | Example Suppliers                           | Form          |
|---------------------|---------------------------------------------|---------------|
| Ti-6Al-4V powder    | AP&C, Carpenter Additive, LPW Technology    | Powder 15-106μm|
| Inconel 718 powder  | EOS, Carpenter, Praxair Surface Tech        | Powder 15-53μm |
| Inconel 625 powder  | EOS, SLM Solutions materials                | Powder 15-53μm |
| 316L powder         | EOS, Renishaw, Sandvik Osprey               | Powder 15-53μm |
| C/SiC preforms      | Safran Ceramics, Albany Int'l (preforms)     | Preforms       |
| W-Cu blanks         | Plansee, Mi-Tech Metals, Midwest Tungsten   | Sintered billets|
| BN billets          | Saint-Gobain (Combat BN), Momentive         | Hot-pressed    |
| ZrO₂ spray powder  | Oerlikon Metco, Praxair                     | Spray powder   |
| NbTi superconductor | Bruker EAS, Luvata, SuperOx                 | Wire/tape      |
| HfC powder          | American Elements, ALB Materials             | Powder (UHTC)  |
| ZrB₂ powder        | H.C. Starck, American Elements              | Powder (UHTC)  |
