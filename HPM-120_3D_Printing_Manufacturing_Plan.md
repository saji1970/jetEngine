# HPM-120 — 3D Printing and Manufacturing Plan

---

## 1. MANUFACTURING STRATEGY OVERVIEW

The HPM-120 engine uses a hybrid manufacturing approach. Not all components can
be 3D printed — some require specialized processes (CVI, sintering, machining).

### Component Manufacturing Method Summary

| Component                  | Primary Method              | 3D Printable? |
|----------------------------|-----------------------------|---------------|
| Intake cowl                | Metal AM (Ti-6Al-4V EBM)   | YES           |
| Intake centerbody          | Metal AM (Ti-6Al-4V SLM)   | YES           |
| Diffuser duct              | Metal AM (Ti-6Al-4V EBM)   | YES           |
| Plasma chamber outer shell | Metal AM (IN718 DMLS)       | YES           |
| Plasma chamber liner       | CVI (C/SiC)                | NO            |
| RF waveguides              | CNC machining (copper)     | NO            |
| Plasma confinement coils   | Wound copper wire           | NO            |
| Fuel injector ring         | Metal AM (IN625 SLM)       | YES           |
| Fuel manifold              | Metal AM (316L SLM)        | YES           |
| Combustion liner           | CVI (C/SiC)                | NO            |
| Combustion outer shell     | Metal AM (IN718 DMLS)       | YES           |
| MHD channel walls          | CVI (C/SiC) + machining    | NO            |
| MHD electrodes             | Press-sinter + EDM (W-Cu)  | NO            |
| MHD insulators             | CNC machining (BN)         | NO            |
| MHD magnet cryostat        | Metal AM (304SS SLM)       | YES           |
| Nozzle inner wall          | CVI (C/SiC)                | NO            |
| Nozzle outer shell         | Metal AM (IN718 DMLS)       | YES           |
| Nozzle EM coil bobbins     | Metal AM (316L SLM)        | YES           |
| Mounting brackets          | Metal AM (IN718 DMLS)       | YES           |

**Summary: ~55% of components (by count) are 3D printable using metal AM.**

---

## 2. 3D PRINTING EQUIPMENT REQUIRED

### 2.1 Machines Needed

| Machine Type         | Material      | Build Vol. Needed   | Example Machines          |
|----------------------|---------------|---------------------|---------------------------|
| EBM (Electron Beam)  | Ti-6Al-4V     | 350×350×380 mm min | Arcam EBM Q20plus         |
| SLM / DMLS (Laser)   | Inconel 718   | 400×400×500 mm min | EOS M400-4, SLM 500      |
| SLM (Laser)          | Inconel 625   | 250×250×300 mm min | EOS M290, Renishaw AM500 |
| SLM (Laser)          | 316L SS       | 250×250×300 mm min | EOS M290, Trumpf TruPrint|
| SLM (Laser)          | 304 SS        | 500×500×500 mm min | SLM 800 (for cryostat)   |

**IMPORTANT:** These are industrial-grade metal additive manufacturing systems
costing $500K - $2M+ each. Desktop FDM/resin printers cannot produce functional
engine parts. Metal AM service bureaus (Protolabs, Materialise, Carpenter Additive,
Velo3D) can be contracted instead of purchasing machines.

### 2.2 Required Post-Processing Equipment

| Equipment                    | Purpose                    |
|------------------------------|----------------------------|
| Hot Isostatic Press (HIP)    | Close internal porosity    |
| Vacuum heat treatment furnace| Aging, stress relief       |
| Wire EDM                     | Precision cutting from plate|
| 5-axis CNC mill              | Finish machining           |
| CNC lathe                    | Cylindrical features       |
| Surface grinder              | Sealing faces              |
| Coordinate Measuring Machine | Dimensional inspection     |
| X-ray / CT scanner           | Internal defect inspection |
| Plasma spray system          | TBC application            |

---

## 3. DETAILED 3D PRINTING PROCEDURES

### 3.1 INTAKE COWL (Ti-6Al-4V, EBM)

```
PART DIMENSIONS: OD 850 mm, length 200 mm, wall 4 mm

BUILD ORIENTATION:
    ┌─────────────┐
    │             │  ← Cowl lip (up)
    │  ╱       ╲  │
    │╱           ╲│
    ╔═════════════╗  ← Build plate

    Print vertically, lip facing up
    Minimizes support structures on aerodynamic surfaces
```

**Step-by-Step:**

1. **Design for AM:**
   - Export STL/3MF from CAD with 0.05 mm chord tolerance
   - Add 0.5 mm stock allowance on all mating surfaces
   - Add 1.0 mm stock on sealing faces
   - Design self-supporting overhangs (< 45° from vertical)

2. **Build Preparation:**
   - Machine: Arcam EBM Q20plus (350 mm Ø build area)
   - NOTE: 850 mm cowl exceeds single-build capacity
   - Split into 2-3 segments with bolted flanges, or use SLM 800 (500×280×850 mm)
   - Powder: Ti-6Al-4V Grade 23, 45-106 μm, plasma atomized
   - Preheat: 730°C
   - Atmosphere: Vacuum (< 5 × 10⁻³ mbar)

3. **Build Parameters:**
   - Layer thickness: 70 μm
   - Beam current: 15 - 25 mA
   - Scan speed: 4,500 mm/s
   - Line offset: 0.2 mm
   - Contour passes: 3
   - Estimated build time: 40 - 60 hours per segment

4. **Post-Processing:**
   - Powder recovery (blast + sieve)
   - Wire EDM to separate from build plate
   - HIP: 920°C / 100 MPa / 2 hours (argon)
   - Stress relief: 650°C / 3 hours, furnace cool
   - CNC finish machining of mating surfaces to ±0.05 mm
   - Surface polish of airflow surfaces to Ra 1.6 μm
   - FPI (Fluorescent Penetrant Inspection) for surface cracks
   - CT scan for internal porosity

### 3.2 PLASMA CHAMBER OUTER SHELL (Inconel 718, DMLS)

```
PART DIMENSIONS: OD 550 mm, ID 510 mm, length 600 mm, wall 6 mm
                  Plus 6 waveguide port bosses and 4 coil mounting rings

BUILD ORIENTATION:
    │             │
    │  ┌─┐  ┌─┐  │  ← Waveguide ports (printed horizontal)
    │  └─┘  └─┘  │
    │             │
    ╔═════════════╗  ← Build plate

    Print vertically (axis vertical)
    Waveguide ports printed as horizontal holes with supports
```

**Step-by-Step:**

1. **Design for AM:**
   - Integrate cooling channels into wall (conformal cooling)
   - Design waveguide port flanges as printed features
   - Add support structure anchors at overhang locations
   - Include lifting points for handling
   - Wall: 6 mm minimum everywhere, 8 mm at bolt locations

2. **Build Preparation:**
   - Machine: EOS M400-4 (400 × 400 × 400 mm)
   - 600 mm length requires tilted build or sectioning
   - Alternative: Print in 2 halves (300 mm each) with welded joint
   - Powder: Inconel 718, 15-53 μm, gas atomized
   - Atmosphere: Argon (O₂ < 100 ppm)
   - Platform preheat: 80°C (standard for IN718)

3. **Build Parameters:**
   - Layer thickness: 40 μm
   - Laser power: 285 W (4 lasers simultaneously)
   - Scan speed: 960 mm/s
   - Hatch spacing: 0.11 mm
   - Stripe width: 10 mm
   - Contour: 2 passes at 150 W / 400 mm/s
   - Estimated build time: 80 - 120 hours per half

4. **Post-Processing:**
   - Wire EDM from build plate
   - HIP: 1,165°C / 100 MPa / 4 hours (argon)
   - Solution treat: 980°C / 1 hour, air cool (or faster)
   - Double age: 720°C/8hr → furnace cool to 620°C/8hr → air cool
   - If printed in halves: TIG weld using IN625 filler, re-HIP weld zone
   - CNC machine all mating faces, port faces, bolt holes
   - Surface finish: Ra 3.2 μm (general), Ra 0.8 μm (sealing faces)
   - Inspect: CT scan, FPI, dimensional CMM

### 3.3 FUEL INJECTOR RING (Inconel 625, SLM)

```
PART: Monolithic ring with 24 integrated injector nozzles

    ┌─────────────────────┐
    │  ○ ○ ○ ○ ○ ○ ○ ○   │  ← 24 injector orifices
    │  ╔═══════════════╗  │     (3 mm each)
    │  ║  FUEL CHANNEL ║  │
    │  ╚═══════════════╝  │  ← Internal manifold channel
    └─────────────────────┘     (printed as one piece)

    OD: 540 mm, ID: 500 mm, width: 30 mm
```

**This is an ideal 3D print candidate** — the internal fuel manifold channel
and 24 integrated swirl injectors would be extremely difficult to machine
conventionally but print well in metal AM.

**Step-by-Step:**

1. **Design for AM:**
   - Internal manifold: 20 mm ID circular channel, self-supporting (teardrop cross-section)
   - 24 injector passages: 4 mm ID with 45° swirl vanes (printed in place)
   - 3 mm orifice exits: may need post-drill for precise diameter
   - Include fuel inlet ports (2×, opposite sides, 12 mm ID)
   - O-ring grooves on mating faces (printed oversized, machined to final)

2. **Build:**
   - Machine: EOS M290 (250 × 250 × 325 mm) — ring fits within envelope
   - Print flat (ring plane horizontal)
   - Powder: Inconel 625, 15-45 μm
   - Layer: 40 μm, Laser: 300 W, Speed: 800 mm/s

3. **Post-Processing:**
   - Stress relief: 870°C / 1 hour
   - Ream/drill all 24 orifices to final 3.00 ±0.02 mm
   - Flow-test each injector: target ±3% uniformity
   - Pressure test manifold: 50 bar hydrostatic (2× operating)
   - Leak check: < 1 cc/min at 30 bar (helium)

### 3.4 COMBUSTION CHAMBER OUTER SHELL (Inconel 718, DMLS)

```
PART DIMENSIONS: OD 528 mm, ID 516 mm, length 800 mm
                  With 48 axial cooling channels in wall

COOLING CHANNEL CROSS-SECTION:
    ┌──────────────────────┐
    │ ████ ████ ████ ████  │  ← IN718 wall with channels
    │ ░░░░ ░░░░ ░░░░ ░░░░  │  ← Cooling channels (4×3 mm each)
    │ ████ ████ ████ ████  │     48 channels circumferential
    └──────────────────────┘
```

**Step-by-Step:**

1. **Design for AM:**
   - 48 axial cooling channels (4 × 3 mm, teardrop cross-section for AM)
   - Integrated inlet/outlet manifolds at each end
   - Flange interfaces with bolt holes (12× M12 each end)
   - Print in 2 segments (400 mm each) if machine Z-height limits

2. **Build:**
   - Machine: EOS M400-4 or SLM 500 HL
   - Print axis vertical
   - Parameters: same as plasma chamber shell (IN718)
   - Estimated build time: 100 - 140 hours per segment

3. **Post-Processing:**
   - Full IN718 HIP + heat treat cycle (see Section 3.2)
   - Flow test cooling channels: confirm no blockages
   - Pressure test: 40 bar hydrostatic
   - CNC machine flanges, bore ID to final dimension
   - Apply NiCrAlY bond coat (HVOF spray) to inner surface if liner clips contact metal

### 3.5 MHD CRYOSTAT HOUSING (304 Stainless Steel, SLM)

```
PART: Double-walled vacuum vessel for superconducting magnet coils
      OD 950 mm, ID ~580 mm, length 1,000 mm

CROSS-SECTION:
    ┌─────────────────────────┐
    │  ┌───────────────────┐  │
    │  │  VACUUM GAP       │  │  Outer wall: 4 mm 304SS
    │  │  ┌─────────────┐  │  │
    │  │  │ COIL SPACE  │  │  │  Inner wall: 4 mm 304SS
    │  │  │             │  │  │  Vacuum gap: 20 mm
    │  │  └─────────────┘  │  │
    │  └───────────────────┘  │
    └─────────────────────────┘
```

**NOTE:** At 950 mm OD, this is at the edge of current AM build envelopes.
Options:
- SLM 800 (500 × 280 × 850 mm) — requires sectioning
- Print in quadrants and weld
- Alternatively, fabricate conventionally (roll + weld 304SS sheet)

**Recommendation: Conventional fabrication** for the cryostat is more practical
and cost-effective than AM. Use 304SS sheet (4 mm), roll-formed, TIG welded.

### 3.6 NOZZLE OUTER SHELL (Inconel 718, DMLS)

```
PART: Converging-diverging nozzle outer structure
      Entry: ~480 mm OD, Exit: ~770 mm OD, Length: 650 mm
      With 8 EM coil mounting rings and cooling channels
```

**Step-by-Step:**

1. **Design for AM:**
   - Integrated coil mounting bosses (8 rings)
   - Cooling channels in wall (regenerative fuel circuit)
   - Print in 2 halves (converging + diverging), bolt/weld at throat

2. **Build:** Same parameters as other IN718 parts

3. **Post-Processing:**
   - Full HIP + heat treat
   - Machine throat to precise contour (±0.1 mm)
   - Surface finish throat region: Ra 0.8 μm

---

## 4. NON-3D-PRINTED COMPONENT MANUFACTURING

### 4.1 C/SiC Liners (Plasma, Combustion, MHD, Nozzle)

These are the most specialized components. They require outsourcing to a CMC
(Ceramic Matrix Composite) manufacturer or building a CVI facility.

**Manufacturing Sequence:**

```
Step 1: FIBER PREFORM
   Carbon fiber (T300 or T800) woven into 2D or 3D preform
   Shape: cylindrical tubes, thickness 5-8 mm
   Weave: 0°/90° plain weave or 5-harness satin

Step 2: PREFORM TOOLING
   Graphite mandrel machined to inner diameter
   Preform wrapped/laid on mandrel

Step 3: CVI PROCESSING
   Reactor conditions:
   - Gas: CH₃SiCl₃ (MTS) + H₂ carrier
   - Temperature: 1,000 - 1,100°C
   - Pressure: 5 - 30 kPa
   - Duration: 100 - 500 hours per cycle
   - Multiple cycles to reach ~85-90% theoretical density

Step 4: SEAL COAT
   Final SiC CVD seal coat (50-100 μm) to close surface porosity

Step 5: MACHINING
   Diamond grinding to final dimensions
   Tolerances: ±0.2 mm typical for CMC

Step 6: COATING
   Environmental Barrier Coat (EBC):
   - Si bond coat (75 μm) — plasma spray
   - Mullite or BSAS intermediate (125 μm) — plasma spray
   - ZrO₂ top coat (300-500 μm) — APS or EB-PVD
```

**Lead time: 3 - 6 months per liner set**

### 4.2 W-Cu Electrodes (MHD Section)

```
Step 1: W powder (1-5 μm) pressed into electrode shapes
        Press pressure: 200-400 MPa

Step 2: Pre-sinter W skeleton at 1,200°C in H₂ atmosphere
        Creates porous W framework (~60% dense)

Step 3: Cu infiltration at 1,150°C in H₂ atmosphere
        Liquid Cu wicks into W pores
        Final density: >98% theoretical

Step 4: EDM (Wire Electrical Discharge Machining)
        Cut to final electrode dimensions
        Surface finish: Ra 1.6 μm on contact faces

Step 5: Dimensional inspection and conductivity test
```

Quantity: 40 electrode pairs (80 pieces total)
Each electrode: ~25 × 350 × 8 mm

### 4.3 BN Insulators (MHD Section)

```
Step 1: Procure hot-pressed BN billets (Grade AX05 or equivalent)
Step 2: CNC machine to insulator segment shapes
        - Diamond tooling recommended
        - Dry machining (no coolant — BN is moisture-sensitive)
Step 3: Dimensional check: ±0.05 mm on mating faces
Step 4: Bake out: 300°C / 4 hours in vacuum (remove moisture)
```

Quantity: 40 insulator segments
Each: ~25 × 350 × 5 mm

### 4.4 Superconducting Magnet Coils (MHD Section)

**This is a specialist procurement item.** NbTi superconducting coils capable
of producing 2-4 T over a 450 × 350 mm bore at 1 m length require:

- NbTi multifilamentary wire (Cu:SC ratio ~2:1)
- Wound on stainless steel bobbin
- Epoxy impregnated (vacuum)
- Persistent current joints
- Cryostat integration

**Recommend procurement from:** Bruker Magnets, ASG Superconductors, or
Cryomagnetics Inc. Custom magnet design and fabrication.

**Alternative for Phase 1/2 prototype:** Use conventional copper electromagnets
(water-cooled) accepting lower field (1-2 T) and higher power consumption.
Much simpler to build, dramatically lowers project risk.

---

## 5. ASSEMBLY SEQUENCE

### Phase 1: Sub-Assembly Build

```
SUB-ASSEMBLY 1: INTAKE MODULE
├── 3D print intake cowl segments (Ti-6Al-4V)
├── 3D print centerbody (Ti-6Al-4V)
├── HIP + heat treat
├── CNC finish machine
├── Bolt/weld segments together
├── Install boundary layer bleed tubes
└── Dimensional inspection

SUB-ASSEMBLY 2: PLASMA IONIZATION MODULE
├── 3D print outer shell (IN718)
├── HIP + heat treat + machine
├── Manufacture C/SiC liner (CVI)
├── Apply EBC + TBC to liner
├── Machine RF waveguides (copper)
├── Wind magnetic confinement coils
├── Install liner into shell (spring clip mounts)
├── Install waveguides into ports
├── Install coils on shell exterior
├── Pressure test cooling circuits
└── Electrical test coils + waveguides

SUB-ASSEMBLY 3: FUEL INJECTION MODULE
├── 3D print injector ring (IN625)
├── Stress relief
├── Drill/ream orifices
├── Flow test all 24 injectors
├── Pressure test manifold
└── Leak test

SUB-ASSEMBLY 4: COMBUSTION MODULE
├── 3D print outer shell (IN718)
├── HIP + heat treat + machine
├── Manufacture C/SiC liner (CVI)
├── Apply EBC + TBC to liner
├── Install liner (compliant mounts)
├── Pressure test cooling channels
└── Hydrostatic proof test

SUB-ASSEMBLY 5: MHD ACCELERATOR MODULE
├── Manufacture C/SiC channel walls (CVI)
├── Apply TBC coatings
├── Press-sinter + EDM W-Cu electrodes (80 pcs)
├── Machine BN insulators (40 pcs)
├── Assemble electrode-insulator stack into channel
├── Build or procure cryostat housing
├── Wind or procure superconducting coils
├── Assemble coils into cryostat
├── Install MHD channel into cryostat bore
├── Leak test cryostat
├── Electrical test coils
├── Cool down test with LN2
└── Verify magnetic field map

SUB-ASSEMBLY 6: NOZZLE MODULE
├── 3D print outer shell halves (IN718)
├── HIP + heat treat + machine
├── Manufacture C/SiC inner liner (CVI)
├── Apply TBC
├── Wind EM coils on bobbins
├── Install liner into shell
├── Install EM coils
├── Connect cooling circuits
└── Flow test
```

### Phase 2: Final Assembly

```
FINAL ASSEMBLY SEQUENCE:

Step 1: Install intake module on assembly fixture
           Fixture: horizontal rail, engine axis horizontal

Step 2: Mate plasma module to intake
           Interface: bolted flange (12× M12, A-286 bolts)
           Seal: Inconel X-750 C-seal
           Torque: 85 N·m

Step 3: Install fuel injector ring at plasma-combustion interface
           Interface: clamped between flanges
           Seal: metal C-seals both sides

Step 4: Mate combustion module
           Interface: bolted flange (12× M12)
           Seal: Inconel C-seal
           Connect fuel cooling lines (combustion → injector return)

Step 5: Mate MHD accelerator module
           Interface: bolted flange (16× M16 — heavier loads)
           Seal: ceramic rope packing + metal C-seal
           Align MHD channel with combustion exit (±0.5 mm)

Step 6: Mate nozzle module
           Interface: bolted flange (12× M12)
           Seal: metal C-seal
           Connect EM coil power cables
           Connect nozzle cooling lines

Step 7: Install mounting brackets
           Forward: Station 400 mm (plasma module)
           Aft: Station 2,800 mm (MHD module)

Step 8: Connect all external systems
           - RF power cables (6×) to plasma module
           - Fuel supply lines to injector + cooling circuits
           - Water cooling lines to MHD + RF
           - LN2 lines to cryostat
           - EM coil power cables (nozzle)
           - MHD electrode power buses
           - Magnet power supply cables
           - All sensor cables (thermocouples, pressure, flow)
           - ECU harness

Step 9: Leak test all fluid circuits
           - Fuel: 50 bar He leak test
           - Water: 15 bar hydrostatic
           - LN2: vacuum + He leak on cryostat

Step 10: Electrical continuity and insulation test
           - All coils: resistance + Hi-pot
           - All electrodes: resistance + insulation
           - All sensors: signal check

Step 11: Weight and CG measurement

Step 12: Ready for test cell installation
```

---

## 6. TESTING SEQUENCE

### Cold Flow Testing
1. Air flow through engine at ambient temperature
2. Measure pressure drops across each section
3. Verify mass flow capacity (target: 100 kg/s at sea level conditions)
4. Check for leaks under flow

### Plasma Ignition Testing
1. Reduce air flow to 10-20% of design
2. Energize RF system at low power (10%)
3. Verify plasma ignition (optical + electrical diagnostics)
4. Gradually increase RF power
5. Map plasma density vs. RF power and airflow

### Combustion Testing
1. Establish stable plasma
2. Introduce fuel at 10% flow
3. Achieve ignition
4. Increase fuel flow incrementally
5. Monitor combustion stability, temperatures, pressures
6. Target: stable combustion at 50% thrust conditions

### MHD Testing
1. Cool down superconducting magnets (or energize copper magnets)
2. Verify magnetic field in channel
3. With hot combustion gas flowing, inject alkali seed
4. Measure gas conductivity
5. Apply MHD accelerator voltage
6. Measure thrust increment from MHD acceleration

### Full Engine Testing
1. Ramp all systems to 25% → 50% → 75% → 100% thrust
2. Measure thrust on calibrated test stand
3. Record all parameters
4. Endurance run at rated thrust

### Test Instrumentation Required

| Measurement            | Sensor Type             | Quantity |
|------------------------|-------------------------|----------|
| Thrust                 | Load cell (200 kN)      | 1        |
| Chamber pressure       | Piezo transducers       | 8        |
| Temperature (gas path) | Type B thermocouples    | 24       |
| Temperature (structure)| Type K thermocouples    | 48       |
| Air mass flow          | Venturi + diff. pressure| 1        |
| Fuel mass flow         | Coriolis meter          | 1        |
| Plasma density         | Langmuir probes         | 4        |
| Magnetic field         | Hall probes             | 8        |
| Exhaust velocity       | Pitot rake              | 1        |
| Vibration              | Accelerometers          | 6        |
| Gas composition        | Mass spectrometer       | 1        |

---

## 7. BUILD COST ESTIMATE (PROTOTYPE)

| Category                        | Estimated Cost (USD)   |
|---------------------------------|------------------------|
| Metal AM printing (all parts)   | $150,000 - $300,000    |
| C/SiC CMC liners (4 sets)      | $200,000 - $500,000    |
| Superconducting magnets         | $300,000 - $800,000    |
| RF power system (6× magnetrons)| $50,000 - $100,000     |
| MHD power supply                | $100,000 - $200,000    |
| Cryogenic system (LN2)         | $50,000 - $100,000     |
| Sensors and instrumentation     | $80,000 - $150,000     |
| ECU and control software        | $50,000 - $100,000     |
| Post-processing (HIP, HT, CNC) | $100,000 - $200,000    |
| Assembly and integration        | $80,000 - $150,000     |
| Test facility and stand         | $200,000 - $500,000    |
| Contingency (25%)               | $340,000 - $775,000    |
| **TOTAL PROTOTYPE**             | **$1.7M - $3.9M**      |

**NOTES:**
- Using copper electromagnets instead of superconducting magnets saves $200-600K
  but limits MHD performance (1-2 T instead of 2-4 T)
- Cost assumes contracting AM builds to service bureaus, not buying machines
- Does not include engineering labor, design, or simulation costs
- A Phase 1 (1-5 kN demonstrator) could be built for $200K - $500K
