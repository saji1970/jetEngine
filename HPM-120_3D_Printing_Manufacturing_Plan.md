# HPM-120 — 3D Printing and Manufacturing Plan

---

## 1. MANUFACTURING STRATEGY OVERVIEW

The HPM-120 engine uses a hybrid manufacturing approach based on the revised
Rotating Detonation Engine (RDE) architecture. The engine flow path is:

**Inlet → Rotating Detonation Annulus → MHD Generator → MHD Accelerator → C-D Nozzle**

Not all components can be 3D printed — some require specialized processes
(CVI, sintering, machining). The RDE-based design eliminates the separate
plasma ionization chamber, steady-state combustion chamber, RF waveguide
array, and plasma confinement coils of the earlier architecture, replacing
them with a compact rotating detonation annulus and split MHD stages.

### Component Manufacturing Method Summary

| Component                    | Primary Method              | 3D Printable? |
|------------------------------|-----------------------------|---------------|
| Intake cowl                  | Metal AM (Ti-6Al-4V EBM)   | YES           |
| Intake centerbody            | Metal AM (Ti-6Al-4V SLM)   | YES           |
| Diffuser duct                | Metal AM (Ti-6Al-4V EBM)   | YES           |
| RDE annulus outer shell      | Metal AM (IN718 DMLS)       | YES           |
| RDE annulus inner liner      | CVI (C/SiC)                | NO            |
| RDE injector face plate      | Metal AM (IN625 SLM)       | YES (ideal AM)|
| Plasma igniter waveguide (1x)| CNC machining (copper)     | NO            |
| MHD Generator channel walls  | CVI (C/SiC) + machining    | NO            |
| MHD Generator electrodes     | Press-sinter + EDM (W-Cu)  | NO            |
| MHD Generator insulators     | CNC machining (BN)         | NO            |
| MHD Generator cryostat       | Roll-form + weld (304SS)   | NO*           |
| MHD Accelerator channel walls| CVI (C/SiC) + machining    | NO            |
| MHD Accelerator electrodes   | Press-sinter + EDM (W-Cu)  | NO            |
| MHD Accelerator insulators   | CNC machining (BN)         | NO            |
| MHD Accelerator cryostat     | Roll-form + weld (304SS)   | NO*           |
| Nozzle inner wall            | CVI (C/SiC)                | NO            |
| Nozzle outer shell           | Metal AM (IN718 DMLS)       | YES           |
| Mounting brackets            | Metal AM (IN718 DMLS)       | YES           |

**Summary: ~45% of components (by count) are 3D printable using metal AM.**

*\*Cryostats could be AM-printed in 304SS but conventional roll-form + weld is
more practical and cost-effective at this size.*

---

## 2. 3D PRINTING EQUIPMENT REQUIRED

### 2.1 Machines Needed

| Machine Type         | Material      | Build Vol. Needed   | Example Machines          |
|----------------------|---------------|---------------------|---------------------------|
| EBM (Electron Beam)  | Ti-6Al-4V     | 350×350×380 mm min | Arcam EBM Q20plus         |
| SLM / DMLS (Laser)   | Inconel 718   | 400×400×500 mm min | EOS M400-4, SLM 500      |
| SLM (Laser)          | Inconel 625   | 250×250×300 mm min | EOS M290, Renishaw AM500 |

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
   - Machine: Arcam EBM Q20plus (350 mm dia build area)
   - NOTE: 850 mm cowl exceeds single-build capacity
   - Split into 2-3 segments with bolted flanges, or use SLM 800 (500x280x850 mm)
   - Powder: Ti-6Al-4V Grade 23, 45-106 um, plasma atomized
   - Preheat: 730 deg C
   - Atmosphere: Vacuum (< 5 x 10^-3 mbar)

3. **Build Parameters:**
   - Layer thickness: 70 um
   - Beam current: 15 - 25 mA
   - Scan speed: 4,500 mm/s
   - Line offset: 0.2 mm
   - Contour passes: 3
   - Estimated build time: 40 - 60 hours per segment

4. **Post-Processing:**
   - Powder recovery (blast + sieve)
   - Wire EDM to separate from build plate
   - HIP: 920 deg C / 100 MPa / 2 hours (argon)
   - Stress relief: 650 deg C / 3 hours, furnace cool
   - CNC finish machining of mating surfaces to +/-0.05 mm
   - Surface polish of airflow surfaces to Ra 1.6 um
   - FPI (Fluorescent Penetrant Inspection) for surface cracks
   - CT scan for internal porosity

### 3.2 RDE ANNULUS OUTER SHELL (Inconel 718, DMLS)

```
PART DIMENSIONS: OD 500 mm, length 400 mm, wall 6 mm
                  With integrated cooling channels and mounting flanges

BUILD ORIENTATION:
    │             │
    │  ┌───────┐  │  ← Mounting flange (top)
    │  │       │  │
    │  │ ANNUL │  │  ← Annular shell with conformal
    │  │       │  │     cooling channels in wall
    │  └───────┘  │
    ╔═════════════╗  ← Build plate

    Print vertically (axis vertical)
    Single piece build (fits EOS M400-4)
```

**Step-by-Step:**

1. **Design for AM:**
   - Integrate conformal cooling channels into wall
   - Design mounting flanges at both ends as printed features
   - Add support structure anchors at overhang locations
   - Include lifting points for handling
   - Wall: 6 mm minimum everywhere, 8 mm at bolt locations

2. **Build Preparation:**
   - Machine: EOS M400-4 (400 x 400 x 400 mm)
   - 500 mm OD shell fits within build envelope printed vertically
   - Print in one piece
   - Powder: Inconel 718, 15-53 um, gas atomized
   - Atmosphere: Argon (O2 < 100 ppm)
   - Platform preheat: 80 deg C (standard for IN718)

3. **Build Parameters:**
   - Layer thickness: 40 um
   - Laser power: 285 W (4 lasers simultaneously)
   - Scan speed: 960 mm/s
   - Hatch spacing: 0.11 mm
   - Stripe width: 10 mm
   - Contour: 2 passes at 150 W / 400 mm/s
   - Estimated build time: 60 - 90 hours

4. **Post-Processing:**
   - Wire EDM from build plate
   - HIP: 1,165 deg C / 100 MPa / 4 hours (argon)
   - Solution treat: 980 deg C / 1 hour, air cool (or faster)
   - Double age: 720 deg C/8hr, furnace cool to 620 deg C/8hr, air cool
   - CNC machine all mating faces, bolt holes
   - Surface finish: Ra 3.2 um (general), Ra 0.8 um (sealing faces)
   - Inspect: CT scan, FPI, dimensional CMM

### 3.3 RDE INJECTOR FACE PLATE (Inconel 625, SLM)

```
PART: Monolithic disc with 24 integrated impinging-jet fuel injectors
      and complex internal fuel manifold channels

    ┌─────────────────────────────┐
    │  ● ● ● ● ● ● ● ● ● ● ●   │  ← 24 doublet impinging-jet
    │  ╔═══════════════════════╗  │     injectors (2 mm orifice each)
    │  ║   FUEL MANIFOLD      ║  │
    │  ║   (teardrop channel)  ║  │  ← Internal manifold channel
    │  ╚═══════════════════════╝  │     20 mm ID, printed as one piece
    │                             │
    │  ←fuel inlet    fuel inlet→ │  ← 2x fuel inlet ports, 12 mm ID
    └─────────────────────────────┘

    OD: 500 mm, thickness: ~40 mm
```

**THIS IS THE STAR 3D PRINT PART** — the monolithic disc integrates 24
impinging-jet fuel injectors with a complex internal fuel manifold that would
be impossible to manufacture conventionally. Each injector features doublet
impinging jets with 2 mm orifices aimed at the annular gap between the RDE
inner and outer walls. The internal manifold uses a teardrop cross-section
(self-supporting for AM) and routes fuel from two inlet ports to all 24
injectors with uniform flow distribution.

**Step-by-Step:**

1. **Design for AM:**
   - Internal manifold: 20 mm ID channel, self-supporting (teardrop cross-section)
   - 24 injector passages: doublet impinging-jet geometry, 2 mm orifice exits
   - Orifices aimed radially into annular gap
   - May need post-drill/ream for precise orifice diameter
   - Include fuel inlet ports (2x, opposite sides, 12 mm ID)
   - O-ring grooves on mating faces (printed oversized, machined to final)

2. **Build:**
   - Machine: EOS M290 (250 x 250 x 325 mm) — 500 mm disc exceeds envelope
   - Option A: Split into 2 halves, print on M290, weld/braze at centerline
   - Option B: Print full disc on EOS M400-4 (400 x 400 mm) — fits with margin
   - Print flat (disc plane horizontal)
   - Powder: Inconel 625, 15-45 um
   - Layer: 40 um, Laser: 300 W, Speed: 800 mm/s
   - Estimated build time: 30 - 50 hours

3. **Post-Processing:**
   - Stress relief: 870 deg C / 1 hour
   - Ream/drill all 24 orifice pairs to final 2.00 +/-0.02 mm
   - Flow-test each injector: target +/-3% uniformity across all 24
   - Pressure test manifold: 50 bar hydrostatic (2x operating)
   - Leak check: < 1 cc/min at 30 bar (helium)
   - CNC machine mating face and O-ring grooves

### 3.4 NOZZLE OUTER SHELL (Inconel 718, DMLS)

```
PART: Converging-diverging nozzle outer structure (simplified)
      Entry: ~480 mm OD, Exit: ~770 mm OD, Length: 650 mm
      With 2 optional EM coil mounting bosses and cooling channels

NOTE: Simplified vs. old design — no 8 EM coil mounting rings.
      Just 2 optional EM coil bosses for boundary layer control.
```

**Step-by-Step:**

1. **Design for AM:**
   - 2 optional coil mounting bosses (vs. 8 rings in old design)
   - Cooling channels in wall (regenerative fuel circuit)
   - Print single piece or 2 halves (converging + diverging), bolt/weld at throat

2. **Build:** Same parameters as other IN718 parts (see Section 3.2)

3. **Post-Processing:**
   - Full HIP + heat treat (see Section 3.2)
   - Machine throat to precise contour (+/-0.1 mm)
   - Surface finish throat region: Ra 0.8 um

### 3.5 MOUNTING BRACKETS (Inconel 718, DMLS)

```
PART: Forward and aft engine mounting brackets
      Topology-optimized for AM — lightweight with complex load paths
```

**Step-by-Step:**

1. **Design for AM:**
   - Topology-optimized geometry
   - Self-supporting where possible
   - Integrated bolt inserts

2. **Build:**
   - Machine: EOS M290 or M400-4
   - Parameters: same as other IN718 parts
   - Estimated build time: 10 - 20 hours per bracket

3. **Post-Processing:**
   - Full HIP + heat treat
   - CNC machine mounting interfaces
   - Inspect: CT scan, FPI, CMM

---

## 4. NON-3D-PRINTED COMPONENT MANUFACTURING

### 4.1 C/SiC Liners (RDE Annulus, MHD Generator, MHD Accelerator, Nozzle)

These are the most specialized components. They require outsourcing to a CMC
(Ceramic Matrix Composite) manufacturer or building a CVI facility.

**Manufacturing Sequence:**

```
Step 1: FIBER PREFORM
   Carbon fiber (T300 or T800) woven into 2D or 3D preform
   Shape: cylindrical tubes / annular segments, thickness 5-8 mm
   Weave: 0/90 deg plain weave or 5-harness satin

Step 2: PREFORM TOOLING
   Graphite mandrel machined to inner diameter
   Preform wrapped/laid on mandrel

Step 3: CVI PROCESSING
   Reactor conditions:
   - Gas: CH3SiCl3 (MTS) + H2 carrier
   - Temperature: 1,000 - 1,100 deg C
   - Pressure: 5 - 30 kPa
   - Duration: 100 - 500 hours per cycle
   - Multiple cycles to reach ~85-90% theoretical density

Step 4: SEAL COAT
   Final SiC CVD seal coat (50-100 um) to close surface porosity

Step 5: MACHINING
   Diamond grinding to final dimensions
   Tolerances: +/-0.2 mm typical for CMC

Step 6: COATING
   Environmental Barrier Coat (EBC):
   - Si bond coat (75 um) — plasma spray
   - Mullite or BSAS intermediate (125 um) — plasma spray
   - ZrO2 top coat (300-500 um) — APS or EB-PVD
```

**Components requiring CVI C/SiC:**
- RDE annulus inner liner
- MHD Generator channel walls
- MHD Accelerator channel walls
- Nozzle inner wall

**Lead time: 3 - 6 months per liner set**

### 4.2 W-Cu Electrodes (MHD Generator + MHD Accelerator)

```
Step 1: W powder (1-5 um) pressed into electrode shapes
        Press pressure: 200-400 MPa

Step 2: Pre-sinter W skeleton at 1,200 deg C in H2 atmosphere
        Creates porous W framework (~60% dense)

Step 3: Cu infiltration at 1,150 deg C in H2 atmosphere
        Liquid Cu wicks into W pores
        Final density: >98% theoretical

Step 4: EDM (Wire Electrical Discharge Machining)
        Cut to final electrode dimensions
        Surface finish: Ra 1.6 um on contact faces

Step 5: Dimensional inspection and conductivity test
```

Quantity:
- MHD Generator: 48 electrodes (24 pairs)
- MHD Accelerator: 64 electrodes (32 pairs)
- **Total: 112 electrode pieces**

Each electrode: ~25 x 350 x 8 mm

### 4.3 BN Insulators (MHD Generator + MHD Accelerator)

```
Step 1: Procure hot-pressed BN billets (Grade AX05 or equivalent)
Step 2: CNC machine to insulator segment shapes
        - Diamond tooling recommended
        - Dry machining (no coolant — BN is moisture-sensitive)
Step 3: Dimensional check: +/-0.05 mm on mating faces
Step 4: Bake out: 300 deg C / 4 hours in vacuum (remove moisture)
```

Quantity:
- MHD Generator: 24 insulator segments
- MHD Accelerator: 32 insulator segments
- **Total: 56 insulator pieces**

Each: ~25 x 350 x 5 mm

### 4.4 Superconducting Magnet Coils (MHD Generator + MHD Accelerator)

**This is a specialist procurement item.** Two sets of NbTi superconducting
coils are required — one for the MHD Generator and one for the MHD Accelerator.
Each must produce 2-4 T over its respective bore. Requirements:

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

### 4.5 MHD Cryostats (304 Stainless Steel, Roll-Form + Weld)

```
PART: Double-walled vacuum vessels for superconducting magnet coils
      One for MHD Generator, one for MHD Accelerator

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

**Recommendation: Conventional fabrication** for the cryostats is more practical
and cost-effective than AM. Use 304SS sheet (4 mm), roll-formed, TIG welded.
Both cryostats follow the same process.

### 4.6 Plasma Igniter Waveguide (1x, Copper, CNC)

A single small plasma igniter replaces the previous 6x RF waveguide array.
CNC machined from copper bar stock. This is a minor component compared to the
old RF system.

---

## 5. ASSEMBLY SEQUENCE

### Phase 1: Sub-Assembly Build

```
SUB-ASSEMBLY 1: INTAKE MODULE (same as previous design)
├── 3D print intake cowl segments (Ti-6Al-4V)
├── 3D print centerbody (Ti-6Al-4V)
├── HIP + heat treat
├── CNC finish machine
├── Bolt/weld segments together
├── Install boundary layer bleed tubes
└── Dimensional inspection

SUB-ASSEMBLY 2: RDE MODULE
│   (replaces old plasma ionization + fuel injection + combustion modules)
├── 3D print RDE annulus outer shell (IN718)
├── 3D print RDE injector face plate (IN625)
├── HIP + heat treat all printed parts
├── CNC finish machine mating faces
├── Receive C/SiC annulus inner liner from CVI supplier
├── Apply EBC + TBC to liner
├── Install liner into outer shell (compliant mounts)
├── Install injector face plate (bolted, sealed)
├── Install small plasma igniter (1x)
├── Pressure test cooling circuits
└── Flow test all 24 injectors

SUB-ASSEMBLY 3: MHD GENERATOR MODULE
├── Receive C/SiC channel walls from CVI supplier
├── Apply TBC coatings
├── Press-sinter + EDM W-Cu electrodes (48 pcs)
├── CNC machine BN insulators (24 pcs)
├── Assemble electrode-insulator stack into channel
├── Fabricate cryostat (roll + weld 304SS)
├── Procure/wind superconducting coils
├── Assemble coils into cryostat
├── Install MHD channel into cryostat bore
├── Leak test cryostat
├── Electrical test coils
├── LN2 cooldown test
└── Verify magnetic field map

SUB-ASSEMBLY 4: MHD ACCELERATOR MODULE (similar to #3 but larger)
├── Same process as MHD Generator module
├── 64 electrodes (vs. 48 for generator)
├── 32 insulators (vs. 24 for generator)
├── Larger cryostat
├── Assemble electrode-insulator stack
├── Install channel into cryostat bore
├── Leak test, electrical test, LN2 cooldown
└── Verify magnetic field map

SUB-ASSEMBLY 5: NOZZLE MODULE (simplified vs. old design)
├── 3D print outer shell (IN718) — single piece or 2 halves
├── HIP + heat treat + machine
├── Receive C/SiC inner liner from CVI supplier
├── Apply TBC
├── Optional: wind 2 EM coils on bosses
├── Install liner into shell
├── Connect cooling circuits
└── Flow test
```

### Phase 2: Final Assembly

```
FINAL ASSEMBLY SEQUENCE:

Step 1:  Mount intake module on assembly fixture
            Fixture: horizontal rail, engine axis horizontal

Step 2:  Mate RDE module to intake
            Interface: bolted flange (12x M12, A-286 bolts)
            Seal: Inconel X-750 C-seal
            Torque: 85 N-m

Step 3:  Mate MHD Generator module to RDE module
            Interface: bolted flange (12x M12)
            Seal: ceramic rope packing + metal C-seal
            Align MHD channel with RDE exit (+/-0.5 mm)

Step 4:  Mate MHD Accelerator module to MHD Generator
            Interface: bolted flange (16x M16 — heavier loads)
            Seal: ceramic rope packing + metal C-seal
            Align channels (+/-0.5 mm)

Step 5:  Mate nozzle module to MHD Accelerator
            Interface: bolted flange (12x M12)
            Seal: metal C-seal
            Connect optional EM coil power cables
            Connect nozzle cooling lines

Step 6:  Install mounting brackets
            Forward: on RDE module
            Aft: on MHD Accelerator module

Step 7:  Connect all external systems
            - Fuel supply lines to RDE injector + cooling circuits
            - Water cooling lines to MHD modules
            - LN2 lines to both cryostats
            - MHD Generator electrode power buses
            - MHD Accelerator electrode power buses
            - Magnet power supply cables (2 sets)
            - Plasma igniter power cable (1x)
            - Optional EM coil power cables (nozzle)
            - All sensor cables (thermocouples, pressure, flow)
            - ECU harness

Step 8:  Leak test all fluid circuits
            - Fuel: 50 bar He leak test
            - Water: 15 bar hydrostatic
            - LN2: vacuum + He leak on both cryostats

Step 9:  Electrical continuity and insulation test
            - All magnet coils: resistance + Hi-pot
            - All electrodes: resistance + insulation
            - All sensors: signal check

Step 10: Weight and CG measurement

Step 11: Ready for test cell installation
```

---

## 6. TESTING SEQUENCE

### Cold Flow Testing
1. Air flow through engine at ambient temperature
2. Measure pressure drops across each section
3. Verify mass flow capacity (target: 100 kg/s at sea level conditions)
4. Check for leaks under flow

### Detonation Ignition Testing
1. Reduce air flow to 10-20% of design
2. Introduce fuel at low flow rate
3. Energize plasma igniter (1x, low power)
4. Verify detonation wave initiation (high-frequency pressure transducers)
5. Confirm rotating detonation wave propagation direction and stability

### RDE Characterization
1. Gradually increase fuel and air flow rates
2. Measure detonation wave speed (target: near Chapman-Jouguet velocity)
3. Measure pressure gain across RDE annulus
4. Map stability envelope (fuel/air ratio, mass flow, wave count)
5. Monitor thermal loads on annulus liner and outer shell
6. Verify injector recovery and refill between wave passes

### MHD Generator Testing
1. Cool down generator superconducting magnets (or energize copper magnets)
2. Verify magnetic field strength and uniformity in channel
3. With hot detonation exhaust flowing, inject alkali seed material
4. Measure gas electrical conductivity
5. Measure open-circuit voltage and short-circuit current
6. Load electrodes and measure power extraction
7. Verify electrode/insulator thermal margins

### MHD Accelerator Testing
1. Cool down accelerator superconducting magnets
2. Route extracted power from generator to accelerator electrodes
3. Apply MHD accelerator voltage across channel
4. Measure thrust increment from MHD acceleration
5. Optimize power transfer between generator and accelerator stages

### Full Engine Testing
1. Ramp all systems to 25% → 50% → 75% → 100% thrust
2. Measure thrust on calibrated test stand
3. Record all parameters (temperatures, pressures, wave speeds, power flows)
4. Verify overall pressure gain from detonation cycle

### Endurance Run
1. Sustained operation at rated thrust
2. Monitor for thermal drift, erosion, electrode degradation
3. Target initial endurance: 30 minutes continuous

### Test Instrumentation Required

| Measurement            | Sensor Type                | Quantity |
|------------------------|----------------------------|----------|
| Thrust                 | Load cell (200 kN)         | 1        |
| RDE wave pressure      | High-freq piezo (>500 kHz) | 8        |
| Chamber pressure       | Piezo transducers           | 8        |
| Temperature (gas path) | Type B thermocouples       | 24       |
| Temperature (structure)| Type K thermocouples       | 48       |
| Air mass flow          | Venturi + diff. pressure   | 1        |
| Fuel mass flow         | Coriolis meter             | 1        |
| Magnetic field         | Hall probes                | 16       |
| MHD voltage/current    | Electrode monitors         | 16       |
| Exhaust velocity       | Pitot rake                 | 1        |
| Vibration              | Accelerometers             | 6        |
| Gas composition        | Mass spectrometer          | 1        |

---

## 7. BUILD COST ESTIMATE (PROTOTYPE)

| Category                        | Estimated Cost (USD)   |
|---------------------------------|------------------------|
| Metal AM printing (all parts)   | $120,000 - $250,000    |
| C/SiC CMC liners (5 sets)      | $250,000 - $600,000    |
| Superconducting magnets (2 sets)| $400,000 - $1,000,000  |
| MHD power conditioning          | $80,000 - $150,000     |
| Cryogenic system (LN2)         | $60,000 - $120,000     |
| Sensors and instrumentation     | $100,000 - $180,000    |
| ECU and control software        | $60,000 - $120,000     |
| Post-processing (HIP, HT, CNC) | $80,000 - $180,000     |
| Assembly and integration        | $80,000 - $150,000     |
| Test facility and stand         | $200,000 - $500,000    |
| Contingency (25%)               | $360,000 - $810,000    |
| **TOTAL PROTOTYPE**             | **$1.8M - $4.1M**      |

**NOTES:**
- Using copper electromagnets instead of superconducting saves $200-600K
  but limits MHD performance to 1-2 T (vs. 2-4 T superconducting)
- Cost assumes contracting AM builds to service bureaus, not buying machines
- No separate RF power system cost (old design was $50-100K for 6x magnetrons;
  new design requires only ~$4K for a single small plasma igniter)
- Does not include engineering labor, design, or simulation costs
