# HPM-120 — Materials and Metallurgy Guide

---

## 1. MATERIALS SUMMARY BY COMPONENT

### Master Materials List

| # | Component              | Primary Material        | Secondary/Coating       | Max Temp (K) |
|---|------------------------|-------------------------|-------------------------|-------------|
| 1 | Intake cowl            | Ti-6Al-4V (Grade 5)    | —                       | 600         |
| 2 | Intake centerbody      | Ti-6Al-4V              | Ceramic TBC optional    | 800         |
| 3 | Diffuser duct          | Ti-6Al-4V              | —                       | 600         |
| 4 | Plasma chamber walls   | Inconel 718             | HfO₂ inner coating     | 1,200       |
| 5 | Plasma chamber liner   | C/SiC composite         | —                       | 1,800       |
| 6 | RF waveguides          | C10100 OFHC Copper      | —                       | 400         |
| 7 | Magnetic coils (plasma)| Copper (water-cooled)   | Kapton insulation       | 400         |
| 8 | Fuel injectors         | Inconel 625             | —                       | 1,100       |
| 9 | Fuel manifold          | 316L Stainless Steel    | —                       | 700         |
| 10| Combustion liner       | C/SiC composite         | ZrO₂ TBC (0.3 mm)     | 1,800       |
| 11| Combustion outer shell | Inconel 718             | —                       | 1,100       |
| 12| MHD channel walls      | C/SiC composite         | ZrO₂ TBC (0.5 mm)     | 1,800       |
| 13| MHD electrodes         | W-Cu composite (80/20)  | —                       | 1,500       |
| 14| MHD insulators         | Boron Nitride (BN)      | —                       | 1,800       |
| 15| MHD magnet coils       | NbTi superconductor     | Cryostat (SS304)        | < 10 (cryo) |
| 16| MHD cryostat           | 304 Stainless Steel     | MLI insulation          | 77 - 300    |
| 17| Nozzle inner wall      | C/SiC composite         | ZrO₂ TBC (0.5 mm)     | 1,800       |
| 18| Nozzle outer shell     | Inconel 718             | —                       | 1,000       |
| 19| Nozzle EM coils        | Copper (water-cooled)   | Ceramic insulation      | 500         |
| 20| Mounting brackets      | Inconel 718             | —                       | 900         |
| 21| Fasteners throughout   | A-286 or Inconel 718    | —                       | 900         |
| 22| Seals                  | Inconel X-750 (C-seals) | —                       | 1,000       |

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

**Used in:** Plasma chamber outer, combustion shell, nozzle shell, mounts

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

**Used in:** Fuel injectors

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

**Used in:** Plasma liner, combustion liner, MHD channel walls, nozzle inner wall

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

**Used in:** RF waveguides

| Property              | Value              |
|-----------------------|--------------------|
| Density               | 8,940 kg/m³        |
| Electrical conductivity| 101% IACS         |
| Thermal conductivity  | 391 W/m·K          |
| Yield strength        | 69 MPa (annealed)  |
| Max service temp      | 400 K (under load) |

**Manufacturing:** CNC machined from bar stock (not 3D printed)

### 2.6 Tungsten-Copper (W-Cu 80/20) Composite

**Used in:** MHD electrodes

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

**Used in:** MHD channel insulators

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

**Used in:** Fuel manifold, non-critical structural parts

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

**Used in:** Inner surface of combustion chamber, MHD channel, nozzle

| Property              | Value              |
|-----------------------|--------------------|
| Thermal conductivity  | 1.5 - 2.0 W/m·K   |
| CTE                   | 10 × 10⁻⁶ /K     |
| Max surface temp      | 1,500 K            |
| Coating thickness     | 0.3 - 0.5 mm       |

**Application Method:**
- Air Plasma Spray (APS) for thick coatings
- Electron Beam Physical Vapor Deposition (EB-PVD) for thin, strain-tolerant coatings
- Bond coat: NiCrAlY (0.1 mm) applied first via HVOF spray

---

## 3. THERMAL BARRIER AND COATING SYSTEM

```
WALL CROSS-SECTION (combustion/MHD/nozzle):

HOT GAS SIDE (2,500 - 3,200 K)
    │
    ▼
┌──────────────────────┐
│  ZrO₂ TBC (0.3-0.5mm)│  ← Thermal barrier
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

Total wall thickness: 15 - 23 mm
```

---

## 4. MATERIAL COMPATIBILITY AND JOINING

### Joining Methods Between Dissimilar Materials

| Joint                          | Method                         |
|--------------------------------|--------------------------------|
| Ti-6Al-4V to Inconel 718      | Diffusion bonding or bolted    |
| C/SiC to Inconel 718          | Mechanical (spring clips/seals)|
| Inconel 718 to Inconel 718    | TIG weld (Inconel 625 filler)  |
| W-Cu electrodes to BN         | Mechanical (clamped)           |
| 316L to Inconel               | TIG weld (309L filler)         |
| C/SiC to ZrO₂ TBC            | Plasma spray (direct)          |

### Critical Notes on Material Selection

1. **C/SiC degrades in steam-rich environments.** Combustion of hydrocarbon fuel
   produces H₂O. The SiC matrix reacts with H₂O above 1,200°C to form Si(OH)₄
   gas. The ZrO₂ TBC and environmental barrier coating (EBC) are essential.

2. **Inconel 718 loses strength above 700°C.** For regions exceeding this, use
   Haynes 230 (max 1,150°C) or Inconel 625 as alternatives.

3. **Alkali seed contamination.** K or Cs salts used for MHD conductivity seeding
   are corrosive to some materials. W-Cu electrodes and BN insulators are
   resistant. Ni-superalloy surfaces in the MHD section need protective coatings.

4. **Thermal expansion mismatch.** C/SiC (CTE ~3 × 10⁻⁶/K) vs Inconel 718
   (CTE ~13 × 10⁻⁶/K) creates severe mismatch. Use compliant seals (Inconel
   X-750 C-seals or ceramic rope packing) at all liner-to-shell interfaces.
   Never bond them rigidly.

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
