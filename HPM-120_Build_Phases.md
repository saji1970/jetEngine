# HPM-120 — Phased Development Plan (RDE Architecture)

---

## Architecture Overview

**Revised flow path:** Inlet → Rotating Detonation Annulus → MHD Generator → MHD Accelerator → C-D Nozzle

Key architectural changes from the previous plasma-combustion baseline:

- **No mechanical compressor.** Rotating detonation provides self-compression (15-25 bar pressure gain across the detonation front), eliminating all rotating machinery.
- **Self-sustaining MHD power cycle.** The MHD generator extracts electrical power from the high-enthalpy exhaust and feeds it directly to the MHD accelerator — no external power required after startup.
- **Startup power only ~50 kW.** External power is needed only to initiate the detonation wave and bootstrap the MHD cycle.
- **Higher operating temperature.** Detonation temperatures reach 3,500-4,000 K (vs. ~2,000 K in the previous deflagration-based design).
- **RF plasma system reduced to a small igniter only.** A single low-power magnetron initiates detonation; the previous multi-magnetron RF sustainer system is eliminated.

---

## PHASE 1: RDE DEMONSTRATOR (1–5 kN)

### Objective
Prove rotating detonation combustion in a bladeless engine — the enabling
technology that makes the entire HPM-120 concept feasible.

### Scaled Dimensions

| Parameter                  | Phase 1 Value        | Notes                         |
|----------------------------|----------------------|-------------------------------|
| Thrust target              | 1 - 5 kN            | Detonation-driven only        |
| RDE annulus OD             | 120 mm               | 3D printed IN718              |
| RDE annulus ID             | 80 mm                | 20 mm annular gap             |
| RDE annulus length         | 100 mm               |                               |
| Inlet diameter             | 200 mm OD            | Converging, 316L or Ti-6Al-4V |
| Total engine length        | ~600 mm              | Compact, no MHD section       |
| Igniter power              | 5 kW                 | Single 2.45 GHz magnetron     |
| Detonation pressure gain   | 5:1 - 15:1           | Self-compression              |
| Detonation temperature     | > 2,500 K            | Target for subscale           |

### What to Build

1. **Simple converging inlet** (316L or Ti-6Al-4V, 3D printed), 200 mm OD
2. **Small RDE annulus**: 120 mm OD, 80 mm ID, 100 mm long (IN718, 3D printed)
3. **Integrated fuel injector face plate** (IN625, 3D printed) — distributes fuel/oxidizer into annular gap
4. **Simple converging-diverging nozzle** (IN625, 3D printed)
5. **Small plasma igniter** for detonation initiation (single 5 kW 2.45 GHz magnetron)
6. **No MHD section** in Phase 1 — thrust from detonation pressure gain and thermal expansion only

### 3D Printable Components (Phase 1)

All structural metal parts fit within a standard EOS M290 build volume
(250 x 250 x 325 mm):

- Inlet: 200 mm OD — **prints in one piece**
- RDE annulus + injector face plate: 120 mm OD x 100 mm long — **prints in one piece**
- C-D nozzle — **prints in one piece**

### Phase 1 Bill of Materials

| Item                                         | Qty | Est. Cost     |
|----------------------------------------------|-----|---------------|
| Inconel 718 powder (10 kg)                   | 1   | $1,500        |
| Inconel 625 powder (5 kg)                    | 1   | $800          |
| 316L powder (5 kg)                           | 1   | $400          |
| AM build service (all parts)                 | 1   | $15,000       |
| HIP + heat treat service                     | 1   | $5,000        |
| CNC finishing service                        | 1   | $8,000        |
| 5 kW 2.45 GHz magnetron (igniter)           | 1   | $4,000        |
| High-speed pressure transducers (8 pcs)      | 1   | $6,000        |
| Fuel pump + fuel system                      | 1   | $3,000        |
| Standard instrumentation (TC, pressure)      | 1   | $5,000        |
| Test stand + safety equipment                | 1   | $8,000        |
| Data acquisition system (high-speed, >1 MHz) | 1   | $5,000        |
| Miscellaneous                                | 1   | $3,300        |
| **TOTAL PHASE 1**                            |     | **~$65,000**  |

### Phase 1 Success Criteria

- [ ] Stable rotating detonation sustained > 60 seconds
- [ ] Detonation wave speed > 1,000 m/s (measured by high-speed pressure transducers)
- [ ] Pressure gain > 5:1 across detonation front
- [ ] Measurable thrust > 500 N
- [ ] No structural failure or thermal runaway
- [ ] Detonation temperature > 2,500 K
- [ ] Fuel injection uniformity confirmed
- [ ] All data channels recorded successfully

---

## PHASE 2: RDE + MHD DEMONSTRATOR (10–20 kN)

### Objective
Demonstrate a self-powering MHD generator-accelerator cycle behind a
rotating detonation engine — proving the complete HPM-120 thermodynamic
cycle at intermediate scale.

### Scaled Dimensions

| Parameter                  | Phase 2 Value        | Notes                            |
|----------------------------|----------------------|----------------------------------|
| Thrust target              | 10 - 20 kN          |                                  |
| RDE annulus OD             | 250 mm               | Scaled up from Phase 1           |
| RDE annulus ID             | 180 mm               | 35 mm annular gap                |
| Intake diameter            | 400 mm OD            |                                  |
| Total engine length        | ~1,400 mm            | Includes MHD sections            |
| Magnetic field             | 1 - 2 T              | Copper coils for prototype       |
| Electrical power (internal)| 80 - 200 kW          | Generated by MHD generator       |
| Startup power (external)   | ~50 kW               | Needed only for bootstrap        |

### New Components vs Phase 1

- **Larger RDE annulus**: 250 mm OD, 180 mm ID (3D printed IN718, possibly 2 segments)
- **MHD generator channel** (simplified, copper electromagnets) — extracts electrical power from high-enthalpy exhaust
- **MHD accelerator channel** (powered by generator output) — provides electromagnetic thrust augmentation
- **Electrode-insulator stack** (W-Cu electrodes + BN insulators)
- **Alkali seed injection system** — enhances exhaust conductivity for MHD interaction
- **Water cooling system** — required for MHD electrodes and channel walls at 3,500-4,000 K exhaust temperatures

### Phase 2 Success Criteria

- [ ] Stable rotating detonation at design conditions
- [ ] MHD generator produces > 100 kW from exhaust
- [ ] MHD accelerator shows measurable thrust increase (> 10%) when powered by generator
- [ ] Self-sustaining power cycle demonstrated (generator powers accelerator without external input)
- [ ] Sustained operation > 120 seconds
- [ ] Total thrust > 10 kN measured on load cell

---

## PHASE 3: FULL-SCALE PROTOTYPE (50–120 kN)

### Objective
Build and test a full-scale HPM-120 engine at rated conditions using the
complete RDE-based architecture.

### This is the full specification detailed in HPM-120_Engineering_Specification.md

### Full HPM-120 Spec

- **Superconducting magnets** (2-4 Tesla) replacing Phase 2 copper coils
- **Full C/SiC liners with TBC** for sustained operation at 3,500-4,000 K
- **Full regenerative cooling** system
- **Design target:** 120 kN thrust
- **Estimated cost:** $1.5M - $3.5M

### Phase 3 Key Milestones

1. **Detailed design review** — complete engineering drawings, FEA, CFD for RDE + MHD architecture
2. **Long-lead procurement** — C/SiC liners (3-6 month lead), superconducting magnets
3. **Metal AM build campaign** — all IN718, Ti-6Al-4V, IN625, 316L parts
4. **Post-processing campaign** — HIP, heat treat, CNC, coating
5. **CMC liner delivery and coating**
6. **Sub-assembly integration** (inlet, RDE, MHD generator, MHD accelerator, nozzle)
7. **Final assembly**
8. **Cold flow test**
9. **Hot fire test** (incremental thrust buildup)
10. **Full thrust demonstration** (120 kN)
11. **Endurance testing**
12. **Design iteration based on test results**

---

## RECOMMENDED STARTING POINT

**Build Phase 1 (RDE demonstrator) first.** It is small enough to 3D print
on a single standard industrial metal AM machine, cheap enough to fund
independently, and answers the most fundamental question: can rotating
detonation combustion provide reliable pressure-gain combustion at the
conditions needed for a bladeless jet engine?

This is the enabling technology that makes the whole concept feasible. Without
confirmed pressure-gain detonation, the downstream MHD cycle has no viable
energy source.

If Phase 1 succeeds, the data directly informs Phase 2 scaling and MHD
integration. If Phase 1 fails, you learn why before committing to a $1.5-3.5M
full-scale prototype.

### Immediate Next Steps

1. Create detailed CAD model of Phase 1 RDE annulus and injector face plate (SolidWorks, Fusion 360, or FreeCAD)
2. Run detonation CFD to validate annular gap dimensions and injector geometry
3. Run thermal-structural FEA on RDE annulus (Ansys, COMSOL, or OpenFOAM)
4. Contact metal AM service bureau for Phase 1 print quotes
5. Source a 5 kW 2.45 GHz magnetron for igniter
6. Source high-speed pressure transducers (>1 MHz sample rate) for detonation wave tracking
7. Design and build test stand with blast containment
8. Obtain necessary permits/clearances for hot-fire testing
9. Establish safety protocols (fuel handling, detonation hazards, RF radiation, noise)
