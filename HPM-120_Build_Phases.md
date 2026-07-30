# HPM-120 — Phased Development Plan

---

## PHASE 1: PLASMA COMBUSTION DEMONSTRATOR (1–5 kN)

### Objective
Prove plasma ignition, plasma-fuel interaction, and combustion stability
in a small-scale non-rotating engine with no turbine or compressor.

### Scaled Dimensions

| Parameter              | Phase 1 Value      | Scale Factor |
|------------------------|--------------------|--------------|
| Thrust target          | 1 - 5 kN          | ~1/25        |
| Air mass flow          | 1 - 5 kg/s        | ~1/20        |
| Intake diameter        | 200 mm             | ~1/4         |
| Combustion chamber ID  | 120 mm             | ~1/4         |
| Combustion length      | 300 mm             | ~1/2.5       |
| Total engine length    | 800 mm             | ~1/4.5       |
| RF power               | 10 - 20 kW        | ~1/8         |
| Fuel flow              | 0.1 - 0.3 kg/s    | ~1/8         |

### What to Build

1. **Simple converging inlet** (Ti-6Al-4V or 316L, 3D printed)
2. **Single RF plasma torch** (2.45 GHz, 10-20 kW magnetron)
3. **Small combustion chamber** (Inconel 718, 3D printed, with TBC)
4. **Simple converging-diverging nozzle** (Inconel 625, 3D printed)
5. **No MHD section** in Phase 1 — thrust from thermal expansion only

### 3D Printable Components (Phase 1)

All structural metal parts fit within a standard EOS M290 build volume
(250 × 250 × 325 mm):

- Inlet: 200 mm OD × 150 mm long — **prints in one piece**
- Combustion chamber: 160 mm OD × 300 mm long — **prints in one piece**
- Nozzle: 180 mm OD × 200 mm long — **prints in one piece**
- Fuel injector ring: 130 mm OD × 20 mm wide — **prints in one piece**

### Phase 1 Bill of Materials

| Item                            | Qty | Est. Cost    |
|---------------------------------|-----|-------------|
| Inconel 718 powder (10 kg)      | 1   | $1,500      |
| Inconel 625 powder (5 kg)       | 1   | $800        |
| 316L powder (5 kg)              | 1   | $400        |
| AM build service (all parts)    | 1   | $15,000     |
| HIP + heat treat service        | 1   | $5,000      |
| CNC finishing service            | 1   | $8,000      |
| 2.45 GHz magnetron (20 kW)      | 1   | $3,000      |
| RF power supply + waveguide     | 1   | $8,000      |
| Fuel pump (electric, 5 bar)     | 1   | $2,000      |
| Thermocouples (Type K, 12 pcs)  | 1   | $500        |
| Pressure transducers (4 pcs)    | 1   | $2,000      |
| Data acquisition system          | 1   | $5,000      |
| Fuel tank + lines                | 1   | $1,000      |
| Test stand frame (welded steel)  | 1   | $3,000      |
| Load cell (10 kN)               | 1   | $1,500      |
| Safety equipment + fire suppress.| 1   | $5,000      |
| **TOTAL PHASE 1**               |     | **~$62,000** |

### Phase 1 Success Criteria

- [ ] Stable plasma ignition and sustained operation for > 60 seconds
- [ ] Fuel ignition via plasma (no spark plug)
- [ ] Stable combustion for > 30 seconds
- [ ] Measurable thrust > 500 N
- [ ] No structural failure or thermal runaway
- [ ] Combustion temperature > 1,500 K
- [ ] All data channels recorded successfully

---

## PHASE 2: TURBINE-FREE PROPULSION DEMONSTRATOR (10–20 kN)

### Objective
Demonstrate non-rotating compression, MHD flow interaction, and
electromagnetic nozzle effects at intermediate scale.

### Scaled Dimensions

| Parameter              | Phase 2 Value      |
|------------------------|--------------------|
| Thrust target          | 10 - 20 kN        |
| Air mass flow          | 8 - 15 kg/s       |
| Intake diameter        | 400 mm             |
| Combustion chamber ID  | 250 mm             |
| MHD channel            | 200 × 180 mm      |
| Total engine length    | 1,600 mm           |
| RF power               | 40 - 60 kW        |
| Magnetic field         | 1 - 2 T (copper)  |
| Electrical power       | 80 - 200 kW       |

### New Components vs Phase 1

- Larger combustion chamber (3D printed IN718, possibly 2 segments)
- Introduction of MHD channel (simplified, copper electromagnets)
- Electrode-insulator stack (W-Cu + BN, small scale)
- Electromagnetic nozzle (2-4 coil rings)
- Alkali seed injection system
- Water cooling system
- Higher-power RF system (3× magnetrons)

### Phase 2 Success Criteria

- [ ] Non-rotating inlet achieves > 1.5:1 pressure ratio at Mach 0.5+
- [ ] MHD interaction parameter > 0.1
- [ ] Measurable thrust increase from MHD acceleration (> 10%)
- [ ] EM nozzle demonstrates variable exit area
- [ ] Sustained operation > 120 seconds
- [ ] Total thrust > 10 kN measured on load cell

---

## PHASE 3: FULL-SCALE PROTOTYPE (50–120 kN)

### Objective
Build and test a full-scale HPM-120 engine at rated conditions.

### This is the full specification detailed in HPM-120_Engineering_Specification.md

### Phase 3 Key Milestones

1. **Detailed design review** — complete engineering drawings, FEA, CFD
2. **Long-lead procurement** — C/SiC liners (3-6 month lead), superconducting magnets
3. **Metal AM build campaign** — all IN718, Ti-6Al-4V, IN625, 316L parts
4. **Post-processing campaign** — HIP, heat treat, CNC, coating
5. **CMC liner delivery and coating**
6. **Sub-assembly integration** (6 modules)
7. **Final assembly**
8. **Cold flow test**
9. **Hot fire test** (incremental thrust buildup)
10. **Full thrust demonstration** (120 kN)
11. **Endurance testing**
12. **Design iteration based on test results**

---

## RECOMMENDED STARTING POINT

**Build Phase 1 first.** It is small enough to 3D print on a single
standard industrial metal AM machine, cheap enough to fund independently,
and answers the most fundamental question: can plasma-assisted combustion
work in a non-rotating engine architecture?

If Phase 1 succeeds, the data directly informs Phase 2 scaling.
If Phase 1 fails, you learn why before committing to a $2-4M prototype.

### Immediate Next Steps

1. Create detailed CAD model of Phase 1 components (SolidWorks, Fusion 360, or FreeCAD)
2. Run thermal-structural FEA on combustion chamber (Ansys, COMSOL, or OpenFOAM)
3. Contact metal AM service bureau for Phase 1 print quotes
4. Source a 20 kW 2.45 GHz magnetron system
5. Design and build test stand
6. Obtain necessary permits/clearances for hot-fire testing
7. Establish safety protocols (fuel handling, plasma, RF radiation, noise)
