# HPM-120 — Hybrid Plasma MHD 120 kN Engine
# Full Engineering Specification (Rev. B — RDE Architecture)

---

## 1. DESIGN OVERVIEW

**Engine Type:** Rotating Detonation / Magnetohydrodynamic (MHD) Air-Breathing Engine
**Designation:** HPM-120
**Target Thrust:** 120 kN (27,000 lbf)
**Operating Principle:** Turbine-free, compressor-free, blade-free propulsion

**Core Concept:**
Air is ingested through a non-rotating inlet, detonated with fuel in a rotating detonation
annulus (pressure-gain combustion, no mechanical compressor), passed through an MHD
generator that extracts electrical power, then electromagnetically accelerated through a
self-powered MHD accelerator channel, and expelled through a conventional converging-
diverging nozzle.

**Architecture:**
Inlet --> Rotating Detonation Annulus --> MHD Generator --> MHD Accelerator --> C-D Nozzle

**Key Innovation:** The rotating detonation engine (RDE) annulus replaces both the plasma
ionization chamber and the steady-state combustion chamber. Detonation waves propagating
circumferentially at 1,500-2,000 m/s produce pressure-gain combustion (15-25 bar) without
any mechanical compressor. The MHD generator extracts sufficient electrical power from the
hot, ionized exhaust to drive the MHD accelerator, making the system self-sustaining after
a brief startup phase requiring only ~50 kW of external power.

---

## 2. FIRST-PRINCIPLES SIZING

### 2.1 Thrust Equation

```
F = m_total x (V_e - V_0) + (P_e - P_0) x A_e
```

Where:
- F = 120,000 N
- m_total = mass flow rate (air + fuel)
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
| Ambient density (SL)   | 1.225 kg/m3       |

### 2.3 Mass Flow Sizing

For a detonation-MHD engine at static/low-speed conditions:

Target exhaust velocity: V_e = 1,400 - 2,000 m/s (MHD-enhanced)
At static conditions (V_0 = 0):

```
m = F / V_e
m = 120,000 / 1,700 = 70.6 kg/s (at V_e = 1,700 m/s mid-range)
```

At Mach 0.8 cruise (V_0 ~ 265 m/s):
```
m = 120,000 / (1,700 - 265) = 83.6 kg/s
```

**Design mass flow rate: 80 - 100 kg/s air**

### 2.4 Intake Sizing

Intake velocity (subsonic diffuser): V_intake ~ 150 m/s

```
A_intake = m / (rho x V_intake)
A_intake = 100 / (1.225 x 150) = 0.544 m2
D_intake = sqrt(4 x A_intake / pi) = 0.832 m
```

**Intake diameter: 0.85 m (round to practical dimension)**

### 2.5 Overall Engine Dimensions

| Dimension               | Value          |
|--------------------------|----------------|
| Intake outer diameter    | 0.85 m         |
| Maximum outer diameter   | 0.90 m         |
| RDE annulus OD           | 0.50 m         |
| MHD channel              | 400 x 300 mm   |
| Nozzle exit diameter     | 0.50 - 0.65 m  |
| Total engine length      | 2.85 m         |
| Dry weight (est.)        | ~420 kg        |

---

## 3. COMPONENT-BY-COMPONENT DIMENSIONAL DESIGN

### 3.1 SECTION 1: AIR INTAKE / DIFFUSER

```
                    <-- 0.85 m -->
                   +==============+
              +====+              +====+
         +====+    DIFFUSER DUCT       +====+
    +====+         (converging)             +====+
====+                                            +====> to RDE annulus
    <-- ----------- 0.55 m length -------------- -->

CROSS-SECTION (looking into intake):

         +-------------------+
       /                       \
     /    +--------------+       \
    |     |  CENTERBODY  |       |   OD: 850 mm
    |     |   (cone)     |       |   Centerbody: 250 mm
     \    +--------------+       /
       \                       /
         +-------------------+
```

| Parameter                  | Dimension       |
|----------------------------|-----------------|
| Inlet outer diameter       | 850 mm          |
| Inlet inner hub diameter   | 250 mm          |
| Annular flow area          | 0.518 m2        |
| Diffuser length            | 550 mm          |
| Exit diameter (to RDE)     | 500 mm          |
| Wall thickness             | 4 mm            |
| Centerbody cone half-angle | 12 deg          |
| Material                   | Ti-6Al-4V       |
| Surface finish             | Ra 1.6 um       |

**Design Features:**
- Fixed-geometry converging annular duct
- Central cone for shock management at high Mach
- Boundary layer bleed slots at 3 stations
- No rotating parts
- Pressure recovery target: 0.92 at Mach 0.85

### 3.2 SECTION 2: ROTATING DETONATION ANNULUS (RDE)

```
SIDE VIEW:

    <-- ---------- 400 mm ----------- -->
    +------------------------------------+
    | INJECTOR FACE PLATE (upstream end) |
    | o o o o o o o o o o o o  (24 inj.) |
    |                                    |
    | %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% | <-- C/SiC liner (5 mm) + ZrO2 TBC
    | ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ | <-- Cooling channels (3 mm)
    | ################################ | <-- Inconel 718 outer shell (6 mm)
    |                                    |
    |   ROTATING DETONATION ZONE         |   3,500 - 4,000 K
    |   (1-3 detonation waves            |   15 - 25 bar
    |    rotating at 1,500-2,000 m/s)    |
    |                                    |
    | ################################ |
    | ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ |
    | %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% |
    +------------------------------------+
    OD: 500 mm   ID: 350 mm

CROSS-SECTION (looking downstream):

         +---------------------+  <-- Outer shell (Inconel 718)
       /  +-------------------+  \
     /  /   +--------------+   \   \  <-- Cooling channels
    |  |  /                  \  |   |
    |  | |  DETONATION WAVE   | |   |  OD: 500 mm
    |  | |  --->  (rotating)  | |   |  ID: 350 mm
    |  | |  3500-4000 K       | |   |  Annular gap: 75 mm
    |  |  \                  /  |   |
     \  \   +--------------+   /   /  <-- C/SiC liner + ZrO2 TBC
       \  +-------------------+  /
         +---------------------+

INJECTOR FACE PLATE DETAIL (looking downstream):

         +---------------------+
       /    o   o   o   o   o    \
     /   o                   o     \
    |  o    +-------------+    o   |
    | o     |  CENTERBODY |     o  |   24 impinging-jet injectors
    |  o    |   (inner)   |    o   |   at face plate
     \   o                   o     /
       \    o   o   o   o   o    /
         +---------------------+
    o = fuel/air impinging-jet injector pair
```

| Parameter                    | Dimension / Spec       |
|------------------------------|------------------------|
| Annulus outer diameter       | 500 mm                 |
| Annulus inner diameter       | 350 mm                 |
| Annular gap width            | 75 mm                  |
| Annulus length               | 400 mm                 |
| Overall OD (with shell)      | 528 mm                 |
| Number of detonation waves   | 1 - 3 (self-organizing)|
| Wave rotational speed        | 1,500 - 2,000 m/s     |
| Peak detonation temperature  | 3,500 - 4,000 K       |
| Chamber pressure             | 15 - 25 bar            |
| Pressure gain ratio          | 15:1 - 25:1           |
| Inner liner thickness        | 5 mm (C/SiC)          |
| Liner coating                | ZrO2 TBC (0.3 mm)     |
| Cooling channel gap          | 3 mm                   |
| Outer shell thickness        | 6 mm (Inconel 718)    |
| Number of cooling channels   | 48 axial channels      |
| Cooling channel dimensions   | 4 mm x 3 mm           |
| Liner material               | C/SiC composite        |
| Outer shell material         | Inconel 718            |
| Cooling medium               | Fuel (regenerative)    |
| Max wall temperature         | 1,400 K               |
| Residence time               | < 1 ms (detonation)   |
| Fuel type                    | Jet-A / JP-8           |

**Fuel Injection System (Integrated into RDE Face Plate):**

| Parameter                    | Dimension / Spec       |
|------------------------------|------------------------|
| Injector type                | Impinging-jet pairs    |
| Number of injectors          | 24 (at 15 deg intervals)|
| Injector orifice diameter    | 3.0 mm                 |
| Fuel feed tube OD            | 6 mm                   |
| Fuel feed tube ID            | 4 mm                   |
| Fuel manifold ring OD        | 540 mm                 |
| Fuel manifold ring ID        | 520 mm                 |
| Fuel manifold tube diameter  | 20 mm ID               |
| Fuel flow rate               | 2.0 - 3.0 kg/s        |
| Fuel pressure (at injector)  | 25 - 40 bar            |
| Injector material            | Inconel 625            |
| Manifold material            | 316L stainless steel   |

**Plasma Igniter (for initial detonation only):**

| Parameter                    | Dimension / Spec       |
|------------------------------|------------------------|
| Igniter type                 | Microwave plasma spark |
| Number of igniters           | 1                      |
| Magnetron power              | 5 kW                   |
| Magnetron frequency          | 2.45 GHz               |
| Waveguide                    | WR-340 (single port)   |
| Purpose                      | Initiate first detonation wave only |
| Operating duration           | < 5 seconds (startup)  |

**Design Features:**
- Detonation waves are self-sustaining once initiated; no continuous ignition needed
- Pressure-gain combustion eliminates the need for a mechanical compressor
- At static conditions, RDE generates its own compression (15-25 bar vs 1-3 bar in old design)
- Annular geometry naturally supports circumferentially rotating detonation waves
- Film cooling injected at inner and outer walls downstream of face plate
- May require UHTC materials (HfC, ZrB2) or active transpiration cooling if C/SiC proves insufficient at 4,000 K

### 3.3 SECTION 3: MHD GENERATOR

```
SIDE VIEW:

    <-- ------------- 600 mm -------------- -->
    +==========================================+
    |  N [--]  N [--]  N [--]  N [--]  N [--] | <-- Magnet array (top)
    |    [--]    [--]    [--]    [--]    [--]  |
    | +--------------------------------------+ |
    | | + ELECTRODE (anode)    [24 pairs]     | |
    | |--------------------------------------| |
    | |         MHD GENERATOR CHANNEL        | | 400 x 300 mm
    | |     (hot ionized exhaust flow -->)    | |
    | |     J x B force = DRAG (extracts     | |
    | |     kinetic energy as electricity)   | |
    | |--------------------------------------| |
    | | - ELECTRODE (cathode)                | |
    | +--------------------------------------+ |
    |    [--]    [--]    [--]    [--]    [--]  | <-- Magnet array (bottom)
    |  S [--]  S [--]  S [--]  S [--]  S [--] |
    +==========================================+

    Overall OD: 850 mm (including magnets + cryostat)

CROSS-SECTION:

    +-------------------------------+
    |       CRYOSTAT (304SS)        |
    |    +---------------------+    |
    |    | MAGNET ASSY NbTi    |    |
    |    |  +---------------+  |    |
    |  +-|--+               +--|--+ |
    |  |+|  |               |  |-|  |  Electrodes (W-Cu 80/20)
    |  | |  | MHD GENERATOR |  | |  |  Channel: 400 x 300 mm
    |  | |  |   CHANNEL     |  | |  |  (rectangular)
    |  |+|  |               |  |-|  |
    |  +-|--+               +--|--+ |
    |    |  +---------------+  |    |
    |    | MAGNET ASSEMBLY     |    |
    |    +---------------------+    |
    |       CRYOSTAT (304SS)        |
    +-------------------------------+
         850 mm overall OD
```

| Parameter                    | Dimension / Spec          |
|------------------------------|---------------------------|
| Channel type                 | Faraday segmented         |
| Channel cross-section        | Rectangular 400 x 300 mm  |
| Channel hydraulic diameter   | ~343 mm                   |
| Channel length               | 600 mm                    |
| Overall outer diameter       | 850 mm (with magnets)     |
| Number of electrode pairs    | 24 (segmented Faraday)    |
| Electrode spacing            | 25 mm                     |
| Electrode material           | Tungsten-copper (W-Cu 80/20) |
| Electrode thickness          | 8 mm                      |
| Insulator material           | Boron nitride (BN)        |
| Insulator thickness          | 5 mm between segments     |
| Magnetic field strength      | 2 - 4 Tesla               |
| Magnet type                  | Superconducting NbTi coils|
| Coil current                 | 8,000 - 12,000 A          |
| Cryostat outer diameter      | 850 mm                    |
| Cryostat material            | 304 stainless steel       |
| Cryostat coolant             | Liquid nitrogen (LN2)     |
| Channel wall material        | C/SiC with ZrO2 TBC       |
| Channel wall thickness       | 8 mm                      |
| Gas temperature at entry     | 3,500 - 4,000 K           |
| Gas conductivity required    | > 10 S/m (seeded)         |
| Seed material                | Cesium or potassium salt  |
| Seed injection rate          | 0.5 - 1.0% of mass flow  |
| Electrical power extracted   | 300 - 600 kW              |
| Electrical power output to   | MHD Accelerator (Sec. 4)  |

**MHD Operating Mode:**
This section operates as an MHD GENERATOR. The hot, ionized exhaust gas
from the RDE (3,500-4,000 K with alkali seeding) flows through the channel
perpendicular to the magnetic field. The J x B Lorentz force acts as drag on
the gas, decelerating it slightly while converting kinetic energy into
electrical energy. This extracted power (300-600 kW) is fed directly to the
downstream MHD accelerator, creating a self-sustaining closed-loop system.

**Notes:**
- Higher gas temperatures from the RDE (vs. 2,500-3,000 K in old design)
  naturally produce higher gas conductivity, improving generator efficiency
- Alkali seeding is still required but is more effective at these temperatures
- Generator efficiency target: 15-25%
- Enthalpy extraction ratio: 5-10% of flow enthalpy

### 3.4 SECTION 4: MHD ACCELERATOR CHANNEL

```
SIDE VIEW:

    <-- --------------- 800 mm ---------------- -->
    +===============================================+
    |  N [--]  N [--]  N [--]  N [--]  N [--] N[--]| <-- Magnet array (top)
    |    [--]    [--]    [--]    [--]    [--]   [--]|
    | +-------------------------------------------+ |
    | | + ELECTRODE (anode)        [32 pairs]     | |
    | |-------------------------------------------| |
    | |         MHD ACCELERATOR CHANNEL           | | 400 x 300 mm
    | |     (ionized exhaust flow -->)             | |
    | |     J x B force = THRUST (accelerates     | |
    | |     gas axially using generator power)    | |
    | |-------------------------------------------| |
    | | - ELECTRODE (cathode)                     | |
    | +-------------------------------------------+ |
    |    [--]    [--]    [--]    [--]    [--]   [--]| <-- Magnet array (bottom)
    |  S [--]  S [--]  S [--]  S [--]  S [--] S[--]|
    +===============================================+

    Overall OD: 900 mm (including magnets + cryostat)

CROSS-SECTION:

    +--------------------------------+
    |        CRYOSTAT (304SS)        |
    |    +----------------------+    |
    |    |  MAGNET ASSY NbTi    |    |
    |    |  +-----------------+ |    |
    |  +-|--+                 +-|--+ |
    |  |+|  |                 | |-|  |  Electrodes (W-Cu 80/20)
    |  | |  | MHD ACCELERATOR | | |  |  Channel: 400 x 300 mm
    |  | |  |    CHANNEL      | | |  |  (rectangular)
    |  |+|  |                 | |-|  |
    |  +-|--+                 +-|--+ |
    |    |  +-----------------+ |    |
    |    |  MAGNET ASSEMBLY     |    |
    |    +----------------------+    |
    |        CRYOSTAT (304SS)        |
    +--------------------------------+
          900 mm overall OD
```

| Parameter                    | Dimension / Spec          |
|------------------------------|---------------------------|
| Channel type                 | Faraday segmented         |
| Channel cross-section        | Rectangular 400 x 300 mm  |
| Channel hydraulic diameter   | ~343 mm                   |
| Channel length               | 800 mm                    |
| Overall outer diameter       | 900 mm (with magnets)     |
| Number of electrode pairs    | 32 (segmented Faraday)    |
| Electrode spacing            | 25 mm                     |
| Electrode material           | Tungsten-copper (W-Cu 80/20) |
| Electrode thickness          | 8 mm                      |
| Insulator material           | Boron nitride (BN)        |
| Insulator thickness          | 5 mm between segments     |
| Magnetic field strength      | 2 - 4 Tesla               |
| Magnet type                  | Superconducting NbTi coils|
| Coil current                 | 8,000 - 12,000 A          |
| Cryostat outer diameter      | 900 mm                    |
| Cryostat material            | 304 stainless steel       |
| Cryostat coolant             | Liquid nitrogen (LN2)     |
| Channel wall material        | C/SiC with ZrO2 TBC       |
| Channel wall thickness       | 8 mm                      |
| Gas temperature at entry     | 3,000 - 3,500 K           |
| Gas conductivity required    | > 10 S/m (seeded)         |
| Electrical power input       | 300 - 600 kW              |
| Power source                 | MHD Generator (Sec. 3)    |

**MHD Operating Mode:**
This is an MHD ACCELERATOR. Electrical current (supplied by the upstream MHD
generator) is driven through the ionized gas perpendicular to the magnetic field.
The J x B Lorentz force accelerates the gas axially, increasing exhaust velocity
by 200-500 m/s beyond what thermal expansion alone provides. The system is
self-powered: no external electrical supply is needed after startup.

**Power Balance:**
- MHD Generator output: 300 - 600 kW
- MHD Accelerator input: 300 - 600 kW
- Power conditioning losses: ~5-10%
- Net external power (steady state): 0 kW
- Startup external power: ~50 kW (to initiate detonation, ramp magnets)

### 3.5 SECTION 5: CONVERGING-DIVERGING NOZZLE

```
SIDE VIEW:

    <-- ------------ 500 mm ------------- -->
    +------+                               /
    |      |                             /
    |      |    CONVERGING             /     DIVERGING
    |      |      \                  /
    |      |        \      o       /
    |      |          \ THROAT   /
    |      |        /      o       \
    |      |      /                  \
    |      |    CONVERGING             \
    |      |                             \
    +------+                               \

    Entry: 400 x 300 mm (from MHD accelerator)
    Throat: 280 mm diameter (circular transition)
    Exit: 500 - 650 mm diameter

OPTIONAL EM COIL ARRANGEMENT:

    +-----+-----+-----+-----+-----+
    |     ||     |     |     ||     |  <-- 2 EM coil rings (optional)
    |     ||     |  \  /  |  ||     |      for minor flow shaping
    |     ||     |  /  \  |  ||     |
    |     ||     |     |     ||     |
    +-----+-----+-----+-----+-----+
```

| Parameter                    | Dimension / Spec       |
|------------------------------|------------------------|
| Nozzle type                  | Converging-diverging   |
| Nozzle length                | 500 mm                 |
| Entry cross-section          | 400 x 300 mm (rect)    |
| Throat diameter              | 280 mm (circular)      |
| Exit diameter                | 500 - 650 mm           |
| Expansion ratio              | 3.2:1 to 5.4:1        |
| Number of EM coil rings      | 2 (optional)           |
| EM coil current              | 500 - 1,000 A          |
| EM field at nozzle           | 0.2 - 0.5 Tesla        |
| Nozzle wall material         | C/SiC composite        |
| Nozzle wall thickness        | 6 mm                   |
| Outer shell                  | Inconel 718 (4 mm)     |
| Thermal barrier coating      | ZrO2 (0.5 mm)          |
| Throat temperature           | 2,400 - 3,000 K        |
| Exit gas temperature         | 1,200 - 1,800 K        |
| Cooling                      | Film cooling at throat  |

**Design Features:**
- Conventional bell nozzle geometry (proven, reliable)
- Rectangular-to-circular transition from MHD channel to nozzle throat
- EM coils are optional and provide only minor flow-shaping capability
- No variable geometry required; fixed expansion ratio sized for design point
- Film cooling at throat region using bypass air or fuel

---

## 4. COMPLETE ENGINE ASSEMBLY -- DIMENSIONAL SUMMARY

```
FULL ENGINE SIDE VIEW (to scale proportions):

<-0.55m-><--0.40m--><----0.60m----><------0.80m------><--0.50m-->
+--------+----------+-------------+-------------------+----------+
|        |          |             |                   |     /    |
| INLET  |   RDE    | MHD GENERA- | MHD ACCELERATOR   | C-D     |
|        | ANNULUS  |    TOR      |                   | NOZZLE   |
|        |          |             |                   |     \    |
+--------+----------+-------------+-------------------+----------+
|<---------------------- 2,850 mm total ------------------------>|

HEIGHT/WIDTH PROFILE:

    Intake       RDE        MHD Gen.       MHD Accel.      Nozzle
    850mm       528mm       850mm          900mm          650mm
     /\          ##           ####          ######          /  \
    /  \         ##           ####          ######         /    \
   /    \        ##           ####          ######        /      \
   \    /        ##           ####          ######        \      /
    \  /         ##           ####          ######         \    /
     \/          ##           ####          ######          \  /

FLOW PATH SCHEMATIC:

  AIR --> [INLET] --> [RDE ANNULUS] --> [MHD GEN] --> [MHD ACCEL] --> [C-D NOZZLE] --> EXHAUST
           diffuse   detonate/burn    extract kW    add velocity      expand
           0.85m OD  15-25 bar        300-600 kW    J x B thrust      280mm throat
                     3,500-4,000 K    (elect. out)  (elect. in)       500-650mm exit
                              |                            ^
                              |   ALKALI SEED (K/Cs 0.5-1%)
                              +---- ELECTRICAL POWER LOOP -+
                                   (self-sustaining)
```

| Section                | Length (mm) | Max OD (mm) | Mass (kg) |
|------------------------|-------------|-------------|-----------|
| Air intake/diffuser    | 550         | 850         | 35        |
| Rotating detonation    | 400         | 528         | 55        |
| MHD generator          | 600         | 850         | 120       |
| MHD accelerator        | 800         | 900         | 130       |
| C-D nozzle             | 500         | 650         | 30        |
| **Subtotal (core)**    | **2,850**   | **900**     | **370**   |
| Mounting/structure     | --          | --          | 20        |
| Wiring/plumbing        | --          | --          | 12        |
| Sensors/ECU            | --          | --          | 8         |
| Coolant/LN2 system     | --          | --          | 10        |
| **TOTAL ENGINE**       | **2,850**   | **900**     | **~420**  |

---

## 5. SUPPORT SYSTEMS

### 5.1 Electrical Power System

| Component                    | Specification             |
|------------------------------|---------------------------|
| MHD generator output         | 300 - 600 kW (self-gen.)  |
| MHD accelerator input        | 300 - 600 kW (from gen.)  |
| Power conditioning/inverter  | 95% efficient             |
| Plasma igniter (startup)     | 5 kW, 2.45 GHz magnetron  |
| Magnet coil power supply     | 50 kW (startup ramping)   |
| Control electronics          | 5 kW                      |
| Cooling pumps                | 10 kW                     |
| EM nozzle coils (optional)   | 5 kW (if installed)       |
| **Startup power demand**     | **~50 kW** (external)     |
| **Steady-state ext. power**  | **~15 kW** (controls/aux) |

**Power source options (startup only -- much simpler than old design):**
- Small gas turbine APU generator (50 kW class)
- Ground power cart (for ground testing)
- Aircraft electrical bus (if installed on aircraft)
- Battery pack (~50 kWh for 10-minute startup/transition)

**Self-Sustaining Operation:**
Once the RDE is running and exhaust is flowing through the MHD generator,
the system generates its own power for the MHD accelerator. No continuous
external power supply of 400-1,000 kW is needed (major improvement over
old architecture). Only auxiliary systems (controls, cooling pumps, sensors)
require external power during steady-state operation.

### 5.2 Cooling System

| Circuit         | Coolant   | Flow Rate    | Delta-T   |
|-----------------|-----------|-------------|-----------|
| RDE annulus     | Jet fuel  | 3.0 kg/s    | +250 K    |
| MHD gen channel | Water     | 4.0 kg/s    | +80 K     |
| MHD accel chan. | Water     | 5.0 kg/s    | +80 K     |
| Magnets (gen)   | LN2       | 0.8 L/min   | 77 K      |
| Magnets (accel) | LN2       | 1.0 L/min   | 77 K      |
| Nozzle throat   | Fuel film | 0.5 kg/s    | +200 K    |

### 5.3 Fuel System

| Parameter              | Value           |
|------------------------|-----------------|
| Fuel type              | Jet-A / JP-8    |
| Max fuel flow          | 3.0 kg/s        |
| Fuel pump pressure     | 45 bar          |
| Fuel pump type         | Electric gear   |
| Fuel pump power        | 12 kW           |
| Fuel filter            | 10 um nominal   |

**Note:** Higher fuel pump pressure (45 bar vs. old 30 bar) required because
RDE chamber pressure is 15-25 bar; fuel must be injected at pressure above
chamber pressure for proper atomization and to prevent flashback.

### 5.4 Alkali Seed System

| Parameter              | Value                |
|------------------------|----------------------|
| Seed material          | K2CO3 or CsOH       |
| Seed fraction          | 0.5 - 1.0% mass flow|
| Seed flow rate         | 0.4 - 1.0 kg/s      |
| Injection location     | RDE exit / MHD gen inlet |
| Seed tank capacity     | 30 min operation     |
| Seed recovery          | Electrostatic precipitator (downstream, optional) |

---

## 6. PERFORMANCE ESTIMATES

| Parameter                    | Value                  |
|------------------------------|------------------------|
| Thrust (static, SL)          | 120 kN                 |
| Thrust (Mach 0.8, 10 km)     | 90 - 110 kN            |
| Air mass flow                 | 80 - 100 kg/s          |
| Fuel mass flow                | 2.0 - 3.0 kg/s         |
| Exhaust velocity              | 1,400 - 2,000 m/s      |
| Detonation temperature        | 3,500 - 4,000 K        |
| Chamber pressure (RDE)        | 15 - 25 bar            |
| MHD generator output          | 300 - 600 kW           |
| MHD accelerator input         | 300 - 600 kW           |
| External power (startup)      | ~50 kW                 |
| External power (steady-state) | ~15 kW (aux only)      |
| Thermal efficiency            | 35 - 50%               |
| Thrust-to-weight ratio        | ~29:1                  |
| SFC (kg/kN*hr)                | 42 - 55                |

### CRITICAL PHYSICS NOTES

1. **RDE detonation stability is the key challenge.** Maintaining continuous rotating
   detonation waves in the annular channel requires precise fuel/air mixing, injection
   timing, and thermal management. Wave mode transitions (1-wave to 2-wave to 3-wave)
   can cause thrust oscillations. Deflagration-to-detonation transition (DDT) must be
   reliable at startup. This is an active area of research with no production RDE
   engines yet flying.

2. **Extreme temperatures (4,000 K) stress materials beyond C/SiC limits.** The peak
   detonation temperature of 3,500-4,000 K exceeds the long-term capability of C/SiC
   composites (~1,600 K continuous). The detonation wave is transient (microsecond
   exposure at any point), which helps, but hot spots and thermal cycling will limit
   liner life. UHTC materials (HfC, ZrB2) or active transpiration cooling may be needed
   for production durability.

3. **MHD generator-accelerator power balance is critical.** The MHD generator must
   extract 300-600 kW from the exhaust flow while the gas retains sufficient velocity
   and ionization for the downstream MHD accelerator to function. Extracting too much
   power in the generator will slow the gas excessively and reduce net thrust. The
   enthalpy extraction ratio must be carefully optimized (target 5-10%).

4. **Superconducting magnets near hot gas paths remain challenging.** The NbTi
   superconducting coils must be maintained below ~10 K while the gas channel a few
   hundred millimeters away is at 3,000-4,000 K. Thermal insulation and cryostat
   design are critical. Cryocooler power consumption and LN2 boil-off must be
   accounted for in the overall system design.

5. **Alkali seed recovery and environmental impact.** Cesium and potassium compounds
   exhausted into the atmosphere raise environmental concerns. A seed recovery system
   (electrostatic precipitator or cyclone separator downstream of the nozzle) may be
   required for operational use. Seed cost is also a consideration for sustained
   operations.

6. **Pressure-gain advantage eliminates the static thrust problem.** Unlike the old
   architecture (which relied on ram compression and produced only 1-3 bar at static
   conditions), the RDE produces 15-25 bar chamber pressure even at zero forward
   velocity. This eliminates the need for a minimum flight speed (ramjet limitation)
   and allows true static thrust generation. This is the single most important
   advantage of the revised architecture.

---

## 7. MOUNTING AND STRUCTURAL INTERFACES

```
MOUNTING FRAME:

    +----------------------------------------------+
    |  +--+                                +--+    |
    |  |M1|     FORWARD MOUNT             |M2|    |  <-- 2 forward mounts
    |  +--+                                +--+    |
    |           ENGINE CORE                        |
    |  +--+                                +--+    |
    |  |M3|     AFT MOUNT                  |M4|    |  <-- 2 aft mounts
    |  +--+                                +--+    |
    +----------------------------------------------+

Mount points: 4x M16 bolts, Inconel 718
Forward mount location: Station 500 mm (on RDE annulus housing)
Aft mount location: Station 2,350 mm (on MHD accelerator housing)
Mount load rating: 50 kN each (200 kN total, 1.67x safety factor)
```

---

## 8. COMPARISON: OLD ARCHITECTURE vs. NEW ARCHITECTURE

```
OLD (Rev. A):
  Inlet -> Plasma Ionization -> Combustion Chamber -> MHD Accelerator -> EM Nozzle
  3,630 mm | 950 mm OD | ~498 kg | 420-1,050 kW external power | 1-3 bar chamber

NEW (Rev. B):
  Inlet -> RDE Annulus -> MHD Generator -> MHD Accelerator -> C-D Nozzle
  2,850 mm | 900 mm OD | ~420 kg | ~50 kW startup only | 15-25 bar chamber
```

| Parameter                | Old (Rev. A)    | New (Rev. B)    | Change       |
|--------------------------|-----------------|-----------------|--------------|
| Total length             | 3,630 mm        | 2,850 mm        | -21%         |
| Max OD                   | 950 mm          | 900 mm          | -5%          |
| Dry weight               | ~498 kg         | ~420 kg         | -16%         |
| Chamber pressure         | 1 - 3 bar       | 15 - 25 bar     | +8x to +12x |
| Combustion temp          | 2,500-3,200 K   | 3,500-4,000 K   | +30%         |
| External power (steady)  | 420-1,050 kW    | ~15 kW (aux)    | -97%         |
| External power (startup) | 420-1,050 kW    | ~50 kW          | -88%         |
| T/W ratio                | ~24:1           | ~29:1           | +21%         |
| SFC (kg/kN*hr)           | 54 - 75         | 42 - 55         | -25%         |
| Thrust (Mach 0.8)        | 80-100 kN       | 90-110 kN       | +12%         |
| Exhaust velocity         | 1,200-1,800 m/s | 1,400-2,000 m/s | +15%         |
| Core sections            | 6               | 5               | -1           |
| Static thrust capable    | Limited         | Full            | Major gain   |
