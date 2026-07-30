# HPM-120 — Hybrid Plasma MHD 120 kN Engine
# Full Engineering Specification

---

## 1. DESIGN OVERVIEW

**Engine Type:** Hybrid Plasma-Assisted Magnetohydrodynamic (MHD) Air-Breathing Engine
**Designation:** HPM-120
**Target Thrust:** 120 kN (27,000 lbf)
**Operating Principle:** Turbine-free, compressor-free, blade-free propulsion

**Core Concept:**
Air is ingested through a non-rotating inlet, partially ionized via RF/microwave plasma,
mixed with fuel for high-temperature combustion, electromagnetically accelerated through
an MHD channel, and expelled through a variable electromagnetic nozzle.

---

## 2. FIRST-PRINCIPLES SIZING

### 2.1 Thrust Equation

```
F = ṁ_total × (V_e - V_0) + (P_e - P_0) × A_e
```

Where:
- F = 120,000 N
- ṁ_total = mass flow rate (air + fuel)
- V_e = exhaust velocity
- V_0 = flight velocity
- P_e = exit pressure
- A_e = exit area

### 2.2 Design Point Conditions

| Parameter              | Value              |
|------------------------|--------------------|
| Design altitude        | Sea level to 12 km |
| Design Mach number     | 0 to 0.85         |
| Ambient pressure (SL)  | 101.3 kPa         |
| Ambient temp (SL)      | 288 K             |
| Ambient density (SL)   | 1.225 kg/m³       |

### 2.3 Mass Flow Sizing

For a combined thermal-MHD engine at static/low-speed conditions:

Target exhaust velocity: V_e = 1,200 - 1,800 m/s (MHD-enhanced)
At static conditions (V_0 = 0):

```
ṁ = F / V_e
ṁ = 120,000 / 1,500 = 80 kg/s (at V_e = 1,500 m/s)
```

At Mach 0.8 cruise (V_0 ≈ 265 m/s):
```
ṁ = 120,000 / (1,500 - 265) = 97 kg/s
```

**Design mass flow rate: 80 - 100 kg/s air**

### 2.4 Intake Sizing

Intake velocity (subsonic diffuser): V_intake ≈ 150 m/s

```
A_intake = ṁ / (ρ × V_intake)
A_intake = 100 / (1.225 × 150) = 0.544 m²
D_intake = √(4 × A_intake / π) = 0.832 m
```

**Intake diameter: 0.85 m (round to practical dimension)**

### 2.5 Overall Engine Dimensions

| Dimension               | Value          |
|--------------------------|----------------|
| Intake outer diameter    | 0.85 m         |
| Maximum outer diameter   | 0.95 m         |
| Combustion chamber ID    | 0.50 m         |
| MHD channel ID           | 0.45 m         |
| Nozzle exit diameter     | 0.55 - 0.75 m |
| Total engine length      | 2.80 m         |
| Dry weight (est.)        | 400 - 550 kg   |

---

## 3. COMPONENT-BY-COMPONENT DIMENSIONAL DESIGN

### 3.1 SECTION 1: AIR INTAKE / DIFFUSER

```
                    ← 0.85 m →
                   ╔══════════╗
              ╔════╝          ╚════╗
         ╔════╝    DIFFUSER DUCT   ╚════╗
    ╔════╝         (converging)         ╚════╗
════╝                                        ╚════→ to ionization
    ← ─────────── 0.55 m length ──────────── →

CROSS-SECTION (looking into intake):

         ┌─────────────────┐
       ╱                     ╲
     ╱    ┌───────────┐       ╲
    │     │ CENTERBODY │       │   OD: 850 mm
    │     │  (cone)    │       │   Centerbody: 250 mm
     ╲    └───────────┘       ╱
       ╲                     ╱
         └─────────────────┘
```

| Parameter                  | Dimension       |
|----------------------------|-----------------|
| Inlet outer diameter       | 850 mm          |
| Inlet inner hub diameter   | 250 mm          |
| Annular flow area          | 0.518 m²        |
| Diffuser length            | 550 mm          |
| Exit diameter (to plasma)  | 500 mm          |
| Wall thickness             | 4 mm            |
| Centerbody cone half-angle | 12°             |
| Material                   | Ti-6Al-4V       |
| Surface finish             | Ra 1.6 μm       |

**Design Features:**
- Fixed-geometry converging annular duct
- Central cone for shock management at high Mach
- Boundary layer bleed slots at 3 stations
- No rotating parts
- Pressure recovery target: 0.92 at Mach 0.85

### 3.2 SECTION 2: PLASMA IONIZATION CHAMBER

```
SIDE VIEW:

    ← ─────── 600 mm ──────── →
    ┌─────────────────────────┐
    │  RF WAVEGUIDE PORTS     │  ← 6 ports, circumferential
    │  ┌─┐  ┌─┐  ┌─┐  ┌─┐   │
    │  │P│  │P│  │P│  │P│   │  P = Plasma generation zone
    │  └─┘  └─┘  └─┘  └─┘   │
    │  MAGNETIC CONFINEMENT   │  ← Solenoid coils (external)
    └─────────────────────────┘
    ID: 500 mm    OD: 620 mm (including coils)

CROSS-SECTION:

         ┌────────────────┐
       ╱  ┌──────────────┐ ╲
     ╱  ╱   PLASMA ZONE    ╲  ╲
    │  │  ┌──────────────┐  │  │
    │  │  │  CORE FLOW   │  │  │   OD: 620 mm
    │  │  │  (air)       │  │  │   ID: 500 mm
    │  │  └──────────────┘  │  │   Plasma zone: 20 mm annular
     ╲  ╲                  ╱  ╱
       ╲  └──────────────┘ ╱
         └────────────────┘
    ← Magnetic coils (external) →
```

| Parameter                    | Dimension / Spec      |
|------------------------------|-----------------------|
| Chamber inner diameter       | 500 mm                |
| Chamber outer diameter       | 550 mm (wall)         |
| Overall OD (with coils)      | 620 mm                |
| Chamber length               | 600 mm                |
| Wall thickness               | 6 mm                  |
| RF waveguide ports           | 6 (circumferential)   |
| RF frequency                 | 2.45 GHz              |
| RF power per port            | 20 - 25 kW            |
| Total RF power               | 120 - 150 kW          |
| Magnetic confinement coils   | 4 solenoid rings      |
| Magnetic field strength      | 0.5 - 1.0 Tesla       |
| Target ionization fraction   | 5 - 15% of airflow    |
| Chamber material (inner)     | C/SiC composite        |
| Chamber material (outer)     | Inconel 718           |
| Liner material               | Hafnium oxide coated  |
| Max wall temperature         | 1,200 K               |
| Cooling                      | Regenerative fuel cool |

**RF Waveguide Specifications:**
- WR-340 rectangular waveguide (86.4 × 43.2 mm)
- 6 ports at 60° intervals
- Each port fed by 25 kW magnetron
- Waveguide material: Copper (C10100 OFHC)
- Waveguide wall thickness: 2.5 mm

**Magnetic Confinement Coils:**
- 4 coil sets, 120 mm spacing along axis
- Coil OD: 620 mm
- Coil ID: 560 mm
- Wire: Copper (water-cooled), 8 AWG
- Current: 200 - 500 A per coil
- Purpose: Confine plasma, prevent wall contact

### 3.3 SECTION 3: FUEL INJECTION SYSTEM

```
INJECTOR RING DETAIL (at plasma-combustion interface):

    CROSS-SECTION:
         ┌────────────────────┐
       ╱   ↙ ↙ ↙ ↙ ↙ ↙ ↙ ↙   ╲
     ╱    SWIRL INJECTOR RING     ╲
    │    ┌────────────────────┐    │
    │    │   FUEL MANIFOLD    │    │   OD: 520 mm
    │    └────────────────────┘    │   ID: 500 mm
     ╲    24 injection points    ╱
       ╲                        ╱
         └────────────────────┘

INJECTOR DETAIL (single):
    ┌───┐
    │ ○ │ ← 3 mm orifice
    │╱╲ │ ← swirl vanes (45° angle)
    │   │
    └─┬─┘
      │ ← fuel feed tube (6 mm OD, 4 mm ID)
```

| Parameter                    | Dimension / Spec       |
|------------------------------|------------------------|
| Injector ring diameter       | 500 mm (on chamber ID) |
| Number of injectors          | 24 (at 15° intervals)  |
| Injector orifice diameter    | 3.0 mm                 |
| Fuel feed tube OD            | 6 mm                   |
| Fuel feed tube ID            | 4 mm                   |
| Swirl angle                  | 45°                    |
| Fuel manifold ring OD        | 540 mm                 |
| Fuel manifold ring ID        | 520 mm                 |
| Fuel manifold tube diameter  | 20 mm ID               |
| Fuel type                    | Jet-A or JP-8          |
| Fuel flow rate               | 1.8 - 2.5 kg/s         |
| Fuel pressure (at injector)  | 15 - 25 bar            |
| Injector material            | Inconel 625            |
| Manifold material            | 316L stainless steel   |

### 3.4 SECTION 4: PLASMA COMBUSTION CHAMBER

```
SIDE VIEW:

    ← ──────── 800 mm ──────── →
    ┌──────────────────────────┐
    │ ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ │ ← C/SiC inner liner (5 mm)
    │ ░░░░░░░░░░░░░░░░░░░░░░ │ ← Cooling channel gap (3 mm)
    │ ████████████████████████ │ ← Inconel 718 outer shell (6 mm)
    │                          │
    │   COMBUSTION ZONE        │   2,500 - 3,200 K
    │   (plasma + fuel + air)  │
    │                          │
    │ ████████████████████████ │
    │ ░░░░░░░░░░░░░░░░░░░░░░ │
    │ ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ │
    └──────────────────────────┘
    ID: 500 mm   OD: 528 mm (liner + cooling + shell)

CROSS-SECTION:

         ┌───────────────────┐  ← Outer shell (Inconel 718)
       ╱ ┌─────────────────┐  ╲
     ╱ ╱ ┌───────────────┐  ╲  ╲  ← Cooling channels
    │ │ ╱   COMBUSTION     ╲ │  │
    │ │ │    ZONE           │ │  │  OD: 528 mm
    │ │ │  2500-3200 K      │ │  │  ID: 500 mm
    │ │ ╲                  ╱ │  │
     ╲ ╲ └───────────────┘  ╱  ╱  ← C/SiC liner
       ╲ └─────────────────┘  ╱
         └───────────────────┘
```

| Parameter                    | Dimension / Spec       |
|------------------------------|------------------------|
| Inner diameter               | 500 mm                 |
| Outer diameter (complete)    | 528 mm                 |
| Length                        | 800 mm                 |
| Inner liner thickness        | 5 mm (C/SiC)          |
| Cooling channel gap          | 3 mm                   |
| Outer shell thickness        | 6 mm (Inconel 718)    |
| Number of cooling channels   | 48 axial channels      |
| Cooling channel dimensions   | 4 mm × 3 mm           |
| Peak gas temperature         | 2,500 - 3,200 K       |
| Chamber pressure             | 8 - 15 bar            |
| Liner material               | C/SiC composite        |
| Liner coating                | ZrO₂ TBC (0.3 mm)    |
| Outer shell material         | Inconel 718            |
| Cooling medium               | Fuel (regenerative)    |
| Residence time               | 2 - 4 ms              |
| Flame stabilization          | Plasma-assisted        |

### 3.5 SECTION 5: MHD ACCELERATOR CHANNEL

```
SIDE VIEW:

    ← ──────────── 1,000 mm ──────────── →
    ╔══════════════════════════════════════╗
    ║  N ┌──┐  N ┌──┐  N ┌──┐  N ┌──┐   ║ ← Magnet array (top)
    ║    └──┘    └──┘    └──┘    └──┘    ║
    ║ ┌──────────────────────────────────┐║
    ║ │ + ELECTRODE (anode)              │║
    ║ │──────────────────────────────────│║
    ║ │         MHD CHANNEL              │║ 450 mm ID
    ║ │     (ionized exhaust flow →)     │║
    ║ │──────────────────────────────────│║
    ║ │ - ELECTRODE (cathode)            │║
    ║ └──────────────────────────────────┘║
    ║    ┌──┐    ┌──┐    ┌──┐    ┌──┐    ║ ← Magnet array (bottom)
    ║  S └──┘  S └──┘  S └──┘  S └──┘   ║
    ╚══════════════════════════════════════╝

    Overall OD: 950 mm (including magnets + cryostat)

CROSS-SECTION:

    ┌─────────────────────────────┐
    │      MAGNET ASSEMBLY        │
    │    ┌─────────────────┐      │
    │    │   N    N    N   │      │
    │  ┌─┼─────────────────┼─┐   │
    │  │+│                 │-│   │  Electrodes
    │  │ │   MHD CHANNEL   │ │   │  450 mm × 350 mm
    │  │+│   (rect/oval)   │-│   │  (rectangular)
    │  └─┼─────────────────┼─┘   │
    │    │   S    S    S   │      │
    │    └─────────────────┘      │
    │      MAGNET ASSEMBLY        │
    └─────────────────────────────┘
         950 mm overall OD
```

| Parameter                    | Dimension / Spec          |
|------------------------------|---------------------------|
| Channel type                 | Faraday segmented         |
| Channel cross-section        | Rectangular 450 × 350 mm |
| Channel hydraulic diameter   | ~394 mm                   |
| Channel length               | 1,000 mm                  |
| Overall outer diameter       | 950 mm (with magnets)     |
| Number of electrode pairs    | 40 (segmented Faraday)    |
| Electrode spacing            | 25 mm                     |
| Electrode material           | Tungsten-copper (W-Cu)    |
| Electrode thickness          | 8 mm                      |
| Insulator material           | Boron nitride (BN)        |
| Insulator thickness          | 5 mm between segments     |
| Magnetic field strength      | 2 - 4 Tesla               |
| Magnet type                  | Superconducting NbTi coils|
| Coil current                 | 8,000 - 12,000 A          |
| Cryostat outer diameter      | 950 mm                    |
| Cryostat coolant             | Liquid nitrogen (LN2)     |
| Channel wall material        | C/SiC with ZrO₂ TBC      |
| Channel wall thickness       | 8 mm                      |
| Gas temperature at entry     | 2,500 - 3,000 K           |
| Gas conductivity required    | > 10 S/m (seeded)         |
| Seed material                | Cesium or potassium salt  |
| Seed injection rate          | 0.5 - 1.0% of mass flow  |
| Electrical power extracted   | 0 kW (accelerator mode)   |
| Electrical power input       | 200 - 800 kW             |

**MHD Operating Mode:**
This is an MHD ACCELERATOR (not generator). Electrical current is driven
through the ionized gas perpendicular to the magnetic field. The J × B
Lorentz force accelerates the gas axially, increasing exhaust velocity.

### 3.6 SECTION 6: ELECTROMAGNETIC NOZZLE

```
SIDE VIEW:

    ← ────────── 650 mm ─────────── →
    ┌────┐                           ╱
    │    │                         ╱
    │    │    CONVERGING         ╱     DIVERGING
    │    │      ╲             ╱      (EM-shaped)
    │    │        ╲    ○    ╱
    │    │          ╲ THROAT╱
    │    │        ╱    ○    ╲
    │    │      ╱             ╲
    │    │    CONVERGING         ╲
    │    │                         ╲
    └────┘                           ╲

    Entry: 450 × 350 mm (from MHD)
    Throat: 300 mm diameter (circular transition)
    Exit: 550 - 750 mm diameter (variable via EM field)

EM COIL ARRANGEMENT:

    ┌──╥──╥──╥──╥──╥──╥──┐
    │  ║  ║  ║  ║  ║  ║  │  ← 8 EM coil rings
    │  ║  ║  ║  ╲╱  ║  ║  │     along nozzle length
    │  ║  ║  ║  ╱╲  ║  ║  │
    │  ║  ║  ║  ║  ║  ║  │
    └──╨──╨──╨──╨──╨──╨──┘
```

| Parameter                    | Dimension / Spec       |
|------------------------------|------------------------|
| Nozzle type                  | Converging-diverging   |
| Nozzle length                | 650 mm                 |
| Entry cross-section          | 450 × 350 mm (rect)   |
| Throat diameter              | 300 mm (circular)      |
| Exit diameter                | 550 - 750 mm (variable)|
| Expansion ratio              | 3.4:1 to 6.25:1       |
| Number of EM coil rings      | 8                      |
| EM coil current              | 500 - 2,000 A          |
| EM field at nozzle           | 0.5 - 1.5 Tesla        |
| Nozzle wall material         | C/SiC composite        |
| Nozzle wall thickness        | 6 mm                   |
| Outer shell                  | Inconel 718 (4 mm)     |
| Thermal barrier coating      | ZrO₂ (0.5 mm)         |
| Throat temperature           | 2,200 - 2,800 K        |
| Exit gas temperature         | 1,200 - 1,800 K        |
| Cooling                      | Film + regenerative     |

---

## 4. COMPLETE ENGINE ASSEMBLY — DIMENSIONAL SUMMARY

```
FULL ENGINE SIDE VIEW (to scale proportions):

←0.55m→←──0.60m──→←────0.80m────→←──────1.00m──────→←──0.65m──→
┌──────┬──────────┬──────────────┬───────────────────┬──────────┐
│      │          │              │                   │     ╱    │
│ INLET│ PLASMA   │  COMBUSTION  │  MHD ACCELERATOR  │ NOZZLE   │
│      │ IONIZ.   │  CHAMBER     │                   │     ╲    │
│      │          │              │                   │          │
└──────┴──────────┴──────────────┴───────────────────┴──────────┘
│←────────────────── 3,600 mm total ──────────────────────────→│

HEIGHT/WIDTH PROFILE:

    Intake          Plasma    Combustion      MHD           Nozzle
    850mm           620mm      528mm          950mm         750mm
     ╱╲              ██          ██         ████████        ╱  ╲
    ╱  ╲             ██          ██         ████████       ╱    ╲
   ╱    ╲            ██          ██         ████████      ╱      ╲
   ╲    ╱            ██          ██         ████████      ╲      ╱
    ╲  ╱             ██          ██         ████████       ╲    ╱
     ╲╱              ██          ██         ████████        ╲  ╱
```

| Section              | Length (mm) | Max OD (mm) | Mass (kg) |
|----------------------|-------------|-------------|-----------|
| Air intake/diffuser  | 550         | 850         | 35        |
| Plasma ionization    | 600         | 620         | 65        |
| Fuel injection ring  | 30          | 540         | 8         |
| Combustion chamber   | 800         | 528         | 45        |
| MHD accelerator      | 1,000       | 950         | 180       |
| EM nozzle            | 650         | 750         | 55        |
| **Subtotal (core)**  | **3,630**   | **950**     | **388**   |
| Mounting/structure   | —           | —           | 40        |
| Wiring/plumbing      | —           | —           | 25        |
| Sensors/ECU          | —           | —           | 15        |
| Coolant/LN2 system   | —           | —           | 30        |
| **TOTAL ENGINE**     | **3,630**   | **950**     | **498**   |

---

## 5. SUPPORT SYSTEMS

### 5.1 Electrical Power System

| Component                    | Specification          |
|------------------------------|------------------------|
| RF generators (6×)           | 25 kW each, 2.45 GHz  |
| MHD power supply             | 200 - 800 kW DC       |
| EM nozzle coil drivers (8×)  | 10 kW each             |
| Magnet coil power supply     | 50 kW (ramping)        |
| Control electronics          | 5 kW                   |
| Cooling pumps                | 15 kW                  |
| **Total electrical demand**  | **420 - 1,050 kW**     |

**Power source options:**
- Gas turbine APU generator (for prototype testing)
- Onboard turbo-generator driven by bleed exhaust
- High-density battery pack (for short-duration test)

### 5.2 Cooling System

| Circuit        | Coolant  | Flow Rate    | ΔT        |
|----------------|----------|-------------|-----------|
| Combustion     | Jet fuel | 2.5 kg/s    | +200 K    |
| MHD channel    | Water    | 5.0 kg/s    | +80 K     |
| Magnets        | LN2      | 1.0 L/min   | 77 K      |
| RF waveguides  | Water    | 2.0 kg/s    | +40 K     |
| Nozzle         | Fuel film| 0.5 kg/s    | +150 K    |

### 5.3 Fuel System

| Parameter              | Value           |
|------------------------|-----------------|
| Fuel type              | Jet-A / JP-8    |
| Max fuel flow          | 2.5 kg/s        |
| Fuel pump pressure     | 30 bar          |
| Fuel pump type         | Electric gear   |
| Fuel pump power        | 8 kW            |
| Fuel filter            | 10 μm nominal   |

---

## 6. PERFORMANCE ESTIMATES

| Parameter                    | Value               |
|------------------------------|---------------------|
| Thrust (static, SL)         | 120 kN              |
| Thrust (Mach 0.8, 10 km)    | 80 - 100 kN (est.) |
| Specific impulse (Jet-A)    | 1,200 - 1,800 s     |
| Air mass flow                | 80 - 100 kg/s       |
| Fuel mass flow               | 1.8 - 2.5 kg/s      |
| Exhaust velocity             | 1,200 - 1,800 m/s   |
| Combustion temperature       | 2,500 - 3,200 K     |
| Thermal efficiency           | 30 - 45%            |
| Overall electrical power     | 420 - 1,050 kW      |
| Thrust-to-weight ratio       | ~24:1               |
| SFC (kg/kN·hr)              | 54 - 75             |

### CRITICAL PHYSICS NOTES

1. **Electrical power is the dominant challenge.** The 250-400 kW figure from early
   estimates is likely an underestimate. MHD acceleration of 80-100 kg/s of partially
   ionized gas through a 2-4 T field to add 300-600 m/s velocity requires on the
   order of 500-1,000 kW or more, depending on channel efficiency.

2. **Gas conductivity is critical.** Air combustion products at 2,500-3,000 K have
   electrical conductivity of only ~1-5 S/m. Alkali seed (potassium or cesium
   compounds at 0.5-1% mass fraction) is needed to raise this to 10-50 S/m for
   effective MHD interaction.

3. **Magnetic field strength determines MHD performance.** The J × B body force
   scales with B². Going from 2 T to 4 T quadruples the force per unit current
   density, but requires superconducting magnets with cryogenic infrastructure.

4. **Non-rotating compression is the hardest unsolved problem.** Without a
   mechanical compressor, the engine relies entirely on ram compression (requires
   forward velocity) and MHD/plasma effects for pressure rise. At static/low-speed
   conditions, chamber pressure will be low (~1-3 bar), severely limiting
   combustion performance. This engine may require a minimum forward velocity
   (like a ramjet) or a separate launch/boost system.

---

## 7. MOUNTING AND STRUCTURAL INTERFACES

```
MOUNTING FRAME:

    ┌──────────────────────────────────────────┐
    │  ┌──┐                            ┌──┐   │
    │  │M1│     FORWARD MOUNT          │M2│   │  ← 2 forward mounts
    │  └──┘                            └──┘   │
    │           ENGINE CORE                    │
    │  ┌──┐                            ┌──┐   │
    │  │M3│     AFT MOUNT              │M4│   │  ← 2 aft mounts
    │  └──┘                            └──┘   │
    └──────────────────────────────────────────┘

Mount points: 4× M16 bolts, Inconel 718
Forward mount location: Station 400 mm (on plasma chamber)
Aft mount location: Station 2,800 mm (on MHD housing)
Mount load rating: 50 kN each (200 kN total, 1.67× safety factor)
```
