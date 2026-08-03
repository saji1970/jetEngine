# HPM-120 Equipment Requirements & 3D Printing Feasibility

---

## Part 1: Complete Equipment List

### A. Metal Additive Manufacturing (3D Printing) Systems

| Machine | Technology | Materials | Build Volume (mm) | Est. Cost | Purpose |
|---------|-----------|-----------|-------------------|-----------|---------|
| **EOS M400-4** | LPBF (4-laser) | Inconel 718, 625 | 400×400×400 | $1.5-2.0M | RDE shell, nozzle shell, injector plate |
| **SLM Solutions 800** | LPBF (quad laser) | Inconel, Ti | 500×280×850 | $1.5-2.5M | Large single-piece intake, nozzle |
| **Arcam EBM Q20plus** | Electron Beam Melting | Ti-6Al-4V | 350×380 (dia×h) | $1.0-1.5M | Intake cowl, diffuser (Ti parts) |
| **EOS M290** | LPBF (single laser) | Inconel, GRCop, 316L | 250×250×325 | $0.5-0.8M | Phase 1 parts (all fit), small components |
| **Velo3D Sapphire XC** | LPBF (non-contact recoater) | Inconel, Ti | 600×550 (dia×h) | $2.0-3.0M | Full-size nozzle in one print, low-angle overhangs |

**For Phase 1 only:** A single EOS M290 ($500-800K) is sufficient — all Phase 1 parts (120 mm OD RDE annulus) fit within its 250×250×325 mm build volume.

**Alternative to buying machines — Use service bureaus:**

| Service Bureau | Capabilities | Location | Typical Lead Time |
|---------------|-------------|----------|-------------------|
| **Protolabs / 3D Hubs** | Inconel, Ti, SS, Al | Global | 2-4 weeks |
| **Carpenter Additive** | Inconel 718/625, GRCop-42, Ti | USA | 3-6 weeks |
| **Velo3D (contract)** | Large-format Inconel, Ti | USA | 4-8 weeks |
| **EOS Direct Metal** | Full EOS material library | Germany/USA | 3-6 weeks |
| **Burloak Technologies** | Inconel, Ti, Al, specialty | Canada | 3-6 weeks |
| **Elementum 3D** | GRCop-42, RAM alloys | USA | 4-8 weeks |
| **Materialise** | Inconel, Ti, SS, Al | Belgium/USA | 2-5 weeks |
| **TRUMPF** | Inconel, Ti, precious metals | Germany | 4-8 weeks |

**Recommendation:** For Phase 1-2, use service bureaus. Invest in own machines only at Phase 3 volume production.

---

### B. Post-Processing Equipment

| Equipment | Purpose | Est. Cost | Alternative |
|-----------|---------|-----------|-------------|
| **Hot Isostatic Press (HIP)** | Close internal porosity in all AM parts | $500K-2M | Outsource: Bodycote, Quintus, Metal Technology Co. ($500-2,000/batch) |
| **Vacuum Furnace** (1,200°C rated) | Heat treatment, stress relief, aging | $150K-400K | Outsource: Solar Atmospheres, Ipsen ($300-1,000/batch) |
| **Wire EDM** | Cut parts from build plate, precision profiles | $100K-300K | Outsource: Any precision machine shop ($50-200/hr) |
| **5-Axis CNC Mill** | Finish machining sealing faces, bolt holes, bores | $200K-600K | Outsource: Any aerospace-certified shop ($80-150/hr) |
| **CNC Lathe** | Cylindrical features, annulus bores | $100K-300K | Outsource ($60-120/hr) |
| **Surface Grinder** | Flat sealing faces, electrode surfaces | $30K-80K | Outsource ($40-80/hr) |
| **Coordinate Measuring Machine (CMM)** | Dimensional inspection (±0.01 mm capable) | $80K-250K | Outsource ($100-300/part) |
| **CT Scanner (Industrial)** | Non-destructive internal inspection of AM parts | $300K-1M | Outsource: Nikon Metrology, Zeiss ($200-500/scan) |
| **Fluorescent Penetrant Inspection (FPI)** | Surface crack detection | $5K-20K | Outsource ($50-150/part) |

---

### C. Ceramic & Composite Manufacturing

| Equipment | Purpose | Est. Cost | Notes |
|-----------|---------|-----------|-------|
| **CVI Reactor** | C/SiC liner fabrication | $1-5M | **Must outsource** — Safran Ceramics, CoorsTek, GE CMC |
| **Graphite Mandrel Tooling** | Fiber preform shaping | $10-50K per set | Custom tooling for each liner geometry |
| **Diamond Grinding Station** | C/SiC final machining | $50K-150K | Can outsource to ceramic machining shops |
| **Air Plasma Spray (APS)** | ZrO₂ / GZO TBC coatings | $80K-200K | Outsource: Praxair, Oerlikon Metco ($100-500/m²) |
| **HVOF Spray System** | NiCrAlY bond coat application | $100K-250K | Often bundled with APS outsourcing |
| **EB-PVD System** | Columnar TBC, Ir coatings | $2-5M | **Must outsource** — Chromalloy, Pratt & Whitney Coatings |

---

### D. Refractory Metal & Advanced Alloy Equipment

These are needed for the advanced alloys from the metallurgy document (W-Re-HfC, RHEA, Nb-Si, etc.):

| Equipment | Purpose | Est. Cost | Notes |
|-----------|---------|-----------|-------|
| **Spark Plasma Sintering (SPS)** | W-Re-HfC, HEA consolidation | $200K-500K | FCT Systeme (Germany), Thermal Technology (USA) |
| **Vacuum Arc Melter (VAR)** | Nb-Si, Co-Re, HEA ingot melting | $150K-400K | Button melter $20-50K (lab scale) |
| **Planetary Ball Mill** | Mechanical alloying of powder blends | $20K-60K | Retsch PM400, Fritsch Pulverisette |
| **Powder Sieve / Classifier** | Sorting AM & PM powders to spec | $5K-20K | Standard lab equipment |
| **Glove Box (Ar atmosphere)** | Handling O₂-sensitive powders (W, Mo, Nb, Ti) | $15K-50K | MBraun, Vacuum Atmospheres Co. |
| **Pack Cementation Furnace** | Silicide coatings on Nb-Si parts | $30K-80K | Modified tube furnace with gas handling |
| **Sinker EDM** | Machining W, Mo, HEA parts (too hard for CNC) | $80K-200K | Makino, Sodick, Mitsubishi |
| **Diamond Grinding / Lapping** | Surface finishing on refractory metals | $20K-60K | Blanchard grinder or surface grinder with diamond wheel |

---

### E. Electrode & Insulator Manufacturing

| Equipment | Purpose | Est. Cost | Notes |
|-----------|---------|-----------|-------|
| **Hydraulic Press** (200-400 MPa) | W powder compaction for electrodes | $30K-100K | Standard PM press |
| **H₂ Atmosphere Furnace** | W skeleton sintering + Cu infiltration | $80K-200K | Must handle 1,200°C in H₂ safely |
| **Cu Infiltration Furnace** | Liquid Cu wicking into W skeleton at 1,150°C | Same as above | Combined with sintering furnace |
| **CNC with Diamond Tooling** | BN insulator machining (dry, no coolant) | $100K-250K | Any precision CNC with dust extraction |

---

### F. Magnet & Cryogenic Systems

| Equipment | Purpose | Est. Cost | Notes |
|-----------|---------|-----------|-------|
| **Superconducting Magnet Coils** (2 sets) | MHD field generation (2-4 T) | $200K-500K/set | Procure from Bruker, ASG, Cryomagnetics |
| **Cryostat Fabrication** | Double-wall 304SS vacuum vessels | $20K-60K/set | Welded fabrication, any precision sheet metal shop |
| **LN₂ Dewar & Transfer Lines** | Cryogenic coolant storage & delivery | $10K-30K | Standard cryogenic supply (Linde, Air Liquide) |
| **Cryogenic Instrumentation** | Temperature sensors, level gauges, relief valves | $10K-25K | Lakeshore, Omega |
| **Phase 1-2 Alternative: Copper Electromagnets** | 1-2 T field (lower performance, much simpler) | $10K-30K/set | Wound copper coil + water cooling, saves $300K+ |

---

### G. Test & Instrumentation

| Equipment | Purpose | Est. Cost | Notes |
|-----------|---------|-----------|-------|
| **Thrust Stand / Load Cell** | Measure engine thrust | $5K-20K | Custom frame + calibrated load cells |
| **High-Speed Pressure Transducers** (8+) | Detonation wave tracking (>100 kHz response) | $6K-12K | PCB Piezotronics, Kulite |
| **High-Speed DAQ** (>1 MHz sample rate) | Capture detonation wave data | $5K-15K | NI PXI, Dewesoft |
| **Thermocouples** (Type K, B, R) | Temperature mapping across engine | $2K-5K | Type B/R for >1,200°C zones |
| **Pyrometer (IR)** | Non-contact surface temperature (TBC surface) | $3K-10K | FLIR, Optris |
| **High-Speed Camera** (>100,000 fps) | Detonation wave visualization | $20K-80K | Photron, Phantom (can rent for $2-5K/week) |
| **Mass Flow Meters** | Fuel, water, seed, LN₂ flow monitoring | $3K-8K | Coriolis type for accuracy |
| **Engine Control Unit (ECU)** | Real-time engine control | $5K-15K | Custom PLC or FPGA-based |
| **Fuel System** (pump, regulator, tank) | Jet-A delivery at 25-40 bar | $3K-8K | Aerospace fuel system components |
| **Water Cooling System** | MHD channel cooling circuit | $5K-15K | Pump, heat exchanger, reservoir |
| **Test Cell / Blast Shield** | Safety enclosure for engine testing | $10K-50K | Reinforced concrete or steel plate |
| **Fire Suppression** | Safety | $3K-10K | CO₂ or dry chemical system |

---

### H. Quality & Metrology

| Equipment | Purpose | Est. Cost | Notes |
|-----------|---------|-----------|-------|
| **Scanning Electron Microscope (SEM)** | Microstructure, coating, powder analysis | $200K-500K | Outsource: University labs ($50-200/hr) |
| **X-Ray Diffractometer (XRD)** | Phase identification in alloys & coatings | $150K-400K | Outsource: $50-100/sample |
| **Optical Emission Spectrometer (OES)** | Alloy composition verification | $30K-80K | Outsource: $20-50/sample |
| **Hardness Tester** (Vickers/Rockwell) | Material verification | $5K-20K | Essential for in-house QC |
| **Universal Testing Machine** | Tensile, compression, bend tests | $30K-100K | Outsource: $100-300/test |
| **Thermal Conductivity Tester** (Laser Flash) | Coating & alloy thermal properties | $100K-300K | Outsource: Netzsch ($200-500/sample) |

---

## Part 2: 3D Printing Feasibility — Every Component

### Summary Table

| Component | 3D Printable? | Technology | Material | Confidence | Notes |
|-----------|:------------:|-----------|----------|:----------:|-------|
| Intake Cowl | **YES** | EBM / LPBF | Ti-6Al-4V | High | Split into 2-3 segments if >350 mm |
| Intake Centerbody | **YES** | LPBF | Ti-6Al-4V | High | Single piece, standard build |
| Diffuser Duct | **YES** | EBM / LPBF | Ti-6Al-4V | High | Straightforward geometry |
| RDE Outer Shell | **YES** | LPBF | Inconel 718 | High | Integrated cooling channels — AM ideal |
| RDE Injector Face | **YES** | LPBF | Inconel 625 | High | Best case for AM — complex internal manifold |
| RDE Inner Liner | **NO** | CVI | C/SiC | N/A | Ceramic composite, not metal AM |
| RDE Inner Liner (W-Re) | **PARTIAL** | LPBF/EBM | W-3Re-HfC | Low | Experimental; see details below |
| MHD Channel Walls | **NO** | CVI | C/SiC | N/A | Ceramic composite |
| MHD Electrodes (W-Cu) | **NO** | Press-sinter-infiltrate | W-Cu 80/20 | N/A | Cu melts during W sintering in AM |
| MHD Electrodes (Graded) | **PARTIAL** | Multi-material AM | W-La₂O₃/Cu | Very Low | Multi-material AM not mature |
| MHD Insulators | **NO** | CNC from billet | Boron Nitride | N/A | Ceramic, not metal AM |
| Nozzle Outer Shell | **YES** | LPBF | Inconel 718 | High | Standard Inconel print |
| Nozzle Inner Wall | **NO** | CVI | C/SiC | N/A | Ceramic composite |
| Mounting Brackets | **YES** | LPBF | Inconel 718 | High | Topology-optimized for AM |
| Cryostats | **NO** | Roll + TIG weld | 304 SS | N/A | Sheet metal forming is simpler and cheaper |
| Magnet Coils | **NO** | Wire winding | NbTi | N/A | Procured component |
| Plasma Igniter | **NO** | CNC | OFHC Copper | N/A | Single simple part |
| Cooling Manifolds | **YES** | LPBF | 316L SS | High | Complex plumbing — AM advantage |
| Seals (C-seals) | **NO** | Stamped/formed | Inconel X-750 | N/A | Thin spring elements, buy from vendor |

### Printable vs. Non-Printable Breakdown

```
┌──────────────────────────────────────────────────┐
│           HPM-120 3D PRINTING BREAKDOWN          │
├──────────────────────────────────────────────────┤
│                                                  │
│   3D PRINTABLE (~45% of part count)              │
│   ████████████████████░░░░░░░░░░░░░░░░░░░░░░░░  │
│                                                  │
│   Components:                                    │
│   • Intake cowl (Ti-6Al-4V)                      │
│   • Intake centerbody (Ti-6Al-4V)                │
│   • Diffuser duct (Ti-6Al-4V)                    │
│   • RDE outer shell + cooling channels (IN718)   │
│   • RDE injector face plate (IN625)              │
│   • Nozzle outer shell (IN718)                   │
│   • Mounting brackets (IN718)                    │
│   • Cooling manifolds (316L)                     │
│                                                  │
│   MUST BE CONVENTIONALLY MADE (~55%)             │
│   ░░░░░░░░░░░░░░░░░░░░████████████████████████  │
│                                                  │
│   Components:                                    │
│   • C/SiC liners (CVI process)                   │
│   • W-Cu electrodes (press-sinter-infiltrate)    │
│   • BN insulators (CNC from billet)              │
│   • Superconducting magnets (wound wire)         │
│   • Cryostats (sheet metal + weld)               │
│   • C-seals (stamped spring metal)               │
│   • TBC coatings (plasma spray / EB-PVD)         │
│                                                  │
└──────────────────────────────────────────────────┘
```

---

## Part 3: 3D Printing the Advanced Metallurgy Alloys

Can the 7 advanced alloys from `HPM-120_Advanced_Metallurgy.md` be 3D printed?

### Alloy 1: W-3Re-0.5HfC — EXPERIMENTAL, NOT PRODUCTION READY

**Current status of W 3D printing:**
- Pure tungsten LPBF has been demonstrated in research labs (2020-2025)
- Major challenges: W's extremely high melting point (3,695 K) requires >1,000 W lasers
- W is prone to cracking during AM due to high DBTT and residual stresses
- W-Re LPBF has been attempted at ORNL and a few European labs

**What would be needed:**
- High-power LPBF system (>1,000 W fiber laser)
- Pre-heated build plate at 400-600°C (reduces thermal stress, prevents cracking)
- Specialized atmosphere control (O₂ < 10 ppm — W oxidizes above 400°C)
- Pre-alloyed W-3Re-0.5HfC spherical powder (gas atomized or PREP atomized)
  - This powder does NOT currently exist commercially
  - Would need custom atomization run (~$50K-100K for small batch)

**Verdict:** Not viable for production in 2025-2026. Continue with SPS + HIP route (proven). Revisit in 3-5 years as high-temperature AM matures.

---

### Alloy 2: Nb-22Ti-16Si-5Cr-2Hf-2Al — POSSIBLE BUT CHALLENGING

**Current status:**
- Nb alloy LPBF has been demonstrated (Nb-based C103 alloy printed by Castheon/Relativity Space)
- Nb₅Si₃ intermetallic formation during AM is unpredictable — rapid solidification changes eutectic morphology
- Cracking is a concern due to the brittle Nb₅Si₃ phase

**What would be needed:**
- Standard LPBF system (Inconel-capable, 400W+ laser)
- Pre-alloyed Nb-Ti-Si-Cr-Hf-Al spherical powder
  - Plasma atomization (PREP or electrode induction gas atomization)
  - Custom atomization run: ~$30K-60K
- Build plate preheat: 200-400°C
- Extensive parameter development (scan strategy to control solidification rate and prevent Nb₅Si₃ cracking)
- Post-build HIP mandatory (1,500°C / 150 MPa)

**Verdict:** Feasible for R&D prototypes. The cast + hot-extrusion route gives a more predictable microstructure for production parts. AM could enable complex geometries (conformal cooling) not possible with casting.

---

### Alloy 3: NbMoTaW-Re RHEA — DEMONSTRATED IN RESEARCH

**Current status:**
- Refractory HEA LPBF has been published by multiple research groups (2021-2024)
- NbMoTaW (without Re) has been successfully printed via LPBF and Directed Energy Deposition (DED)
- Main challenge: cracking due to extreme residual stresses from high melting point

**What would be needed:**
- High-power LPBF (>500 W laser, preferably 1,000 W)
- Pre-heated build plate: 400-800°C (critical for crack prevention)
- Pre-alloyed RHEA powder from PREP or plasma atomization
  - Custom atomization: ~$80K-150K for small batch
- Laser Directed Energy Deposition (L-DED) may be more practical than LPBF:
  - Larger build volume
  - Lower residual stress
  - Coarser microstructure (acceptable for structural parts)
  - Machines: TRUMPF TruLaser Cell, Optomec LENS

**Verdict:** Promising for near-term R&D (2-3 years). L-DED route is more practical than LPBF for these alloys.

---

### Alloy 4: GRCop-42 (Cu-4Cr-2Nb) — YES, PRODUCTION READY

**Current status: This is the success story of aerospace 3D printing.**
- NASA has printed GRCop-42 combustion chambers for the RS-25 (SLS) and RDRE (Rotating Detonation Rocket Engine) programs
- Elementum 3D and Carpenter Additive sell GRCop-42 powder commercially
- Print parameters are published and well-characterized
- NASA TRL 7+ (flight-qualified hardware)

**What is needed:**
- Standard LPBF system with 400W+ laser (EOS M290, M400-4)
- GRCop-42 powder (commercially available)
  - Supplier: Elementum 3D (USA) — ~$150-300/kg
  - Particle size: 15-53 μm, spherical, gas atomized
- Green laser (515 nm) preferred over IR (1,070 nm) for Cu alloys
  - Cu is highly reflective at IR wavelengths (>95% reflectivity)
  - Green laser reflectivity on Cu: ~60% — much better absorption
  - Machines with green lasers: TRUMPF TruPrint 1000 Green, SLM Solutions (green option)
  - Alternative: Standard IR laser at higher power (400W+) works but less efficient

**Process parameters (IR laser, proven):**
- Laser power: 370 W
- Scan speed: 800 mm/s
- Layer thickness: 30 μm
- Hatch spacing: 0.09 mm
- Build atmosphere: Ar (O₂ < 100 ppm)
- Baseplate preheat: 200°C
- As-built density: >99.5%
- Post-build HIP: 900°C / 100 MPa / 4 hr (closes remaining porosity)

**Integral cooling channel design rules for AM:**
```
SELF-SUPPORTING CHANNEL CROSS-SECTIONS (no support needed):

    Teardrop (preferred):        Diamond:            Inverted arch:
         /\                        /\                  ┌──────┐
        /  \                      /  \                 │      │
       /    \                    /    \                │      │
      │      │                  │      │               \    /
      │      │                  │      │                \  /
       \    /                    \    /                  \/
        ────                      \/

    Max span: 3-4 mm           Max span: 3 mm        Max span: 3 mm
    Overhang angle: >45°       Overhang angle: 45°   Good for bottom wall cooling
```

**Key advantage for HPM-120:** GRCop-42 AM enables printing the RDE cooling jacket as a single piece with integral cooling channels. No brazing or diffusion bonding joints — the #1 failure mode in conventionally-made regeneratively-cooled chambers.

**Verdict:** Ready for production NOW. This is the single highest-impact AM application for the HPM-120.

---

### Alloy 5: W-La₂O₃/Cu Graded Electrodes — NOT FEASIBLE VIA AM

**Why not:**
- Requires a smooth composition gradient from W to Cu
- W and Cu have incompatible melting points (3,695 K vs 1,358 K)
- Multi-material AM is not mature enough for W↔Cu gradients
- The press-sinter-infiltrate route produces superior electrode quality

**Possible future approach:**
- Directed Energy Deposition (DED) with dual powder feeders (W and Cu)
- Gradually change the W:Cu ratio layer by layer
- This has been demonstrated for Ti↔V and SS↔Inconel gradients
- W↔Cu remains unproven due to the extreme melting point mismatch

**Verdict:** Stick with conventional press-sinter-infiltrate process. SPS grading also works well.

---

### Alloy 6: Co-17Re-23Cr Superalloy — FEASIBLE

**Current status:**
- Co-Cr alloys are routinely 3D printed (dental, medical, aerospace)
- Co-Cr-Re has not been specifically printed, but the metallurgy is compatible with AM
- The high Re content (17 wt%) may cause hot cracking during solidification

**What would be needed:**
- Standard LPBF system (EOS M290/M400-4)
- Pre-alloyed Co-Re-Cr powder (custom atomization: ~$20K-40K)
- Parameter development to avoid hot cracking (Re segregation to grain boundaries)
- Post-build HIP + solution treatment

**Verdict:** Feasible with moderate development effort. Worthwhile if complex-geometry parts are needed (manifolds, transition sections). For simple shells, investment casting is more cost-effective.

---

### Alloy 7: Gd₂Zr₂O₇ / YSZ TBC — NOT AN AM PROCESS

TBC coatings are applied by thermal spray (APS) or vapor deposition (EB-PVD), not by 3D printing. These are coating processes applied onto already-fabricated structural parts. No change needed — the existing APS/EB-PVD process chain is the correct approach.

---

### AM Feasibility Summary for Advanced Alloys

| Alloy | AM Feasible? | Best AM Method | Readiness | Recommendation |
|-------|:----------:|---------------|:---------:|----------------|
| 1. W-Re-HfC | No (2025) | LPBF (future) | TRL 2-3 | Use SPS + HIP |
| 2. Nb-Si composite | Partial | LPBF / DED | TRL 3-4 | Use VAR + extrusion for production |
| 3. NbMoTaW-Re RHEA | Partial | L-DED | TRL 3-4 | DED prototypes feasible |
| 4. GRCop-42 | **YES** | LPBF | **TRL 7+** | **Print immediately — proven** |
| 5. W-La₂O₃/Cu graded | No | N/A | TRL 1-2 | Use press-sinter-infiltrate |
| 6. Co-Re-Cr | Yes (dev) | LPBF | TRL 4-5 | Feasible with parameter development |
| 7. GZO/YSZ TBC | N/A | APS / EB-PVD | TRL 8 | Not an AM process (coating) |

---

## Part 4: Complete Manufacturing Flow — What Gets Printed vs. What Doesn't

### Phase 1: RDE Demonstrator (1-5 kN) — Budget ~$65K

**All structural parts are 3D printed:**

```
PHASE 1 MANUFACTURING FLOW
═══════════════════════════

3D PRINT (Service Bureau)                 CONVENTIONAL (Vendors)
┌─────────────────────────┐               ┌───────────────────────┐
│                         │               │                       │
│  EOS M290 Build 1:      │               │  Procure:             │
│  • RDE annulus (IN718)  │               │  • 5 kW magnetron     │
│  • Injector plate (IN625│)              │  • Pressure sensors   │
│  • Simple nozzle (IN718)│               │  • Thermocouples      │
│  • Brackets (IN718)     │               │  • Fuel pump          │
│                         │               │  • Plumbing & fittings│
│  EOS M290 Build 2:      │               │  • DAQ system         │
│  • Intake (Ti-6Al-4V)   │               │  • Spark igniter      │
│  • Manifolds (316L)     │               │                       │
│                         │               │  Fabricate:           │
└──────────┬──────────────┘               │  • Test stand (steel) │
           │                              │  • Fuel tank          │
           ▼                              │  • Safety shields     │
┌─────────────────────────┐               └───────────┬───────────┘
│  Post-Processing:       │                           │
│  • HIP (outsource)      │                           │
│  • Heat treat (outsource│)                          │
│  • CNC finish (outsource│)                          │
│  • FPI + CT scan        │                           │
└──────────┬──────────────┘                           │
           │                                          │
           └──────────────┬───────────────────────────┘
                          │
                          ▼
               ┌─────────────────────┐
               │     ASSEMBLY        │
               │  Bolt-up + plumb    │
               │  Leak test          │
               │  Instrument         │
               │  Cold-flow test     │
               │  HOT FIRE TEST      │
               └─────────────────────┘

Phase 1 does NOT need:
  ✗ C/SiC liners (short-duration test, uncooled or film-cooled)
  ✗ MHD sections (no MHD in Phase 1)
  ✗ Superconducting magnets
  ✗ Cryogenics
  ✗ TBC coatings (optional, can test without for short runs)
  ✗ Advanced alloys (standard IN718/625 sufficient for demonstrator)
```

**Phase 1 Equipment You Actually Need:**

| Equipment | Own or Outsource | Cost |
|-----------|:----------------:|-----:|
| Metal AM printing (all parts) | Outsource | $15,000 |
| HIP + heat treatment | Outsource | $5,000 |
| CNC finishing | Outsource | $8,000 |
| Thrust stand + load cells | Own | $8,000 |
| DAQ system (>1 MHz) | Own | $5,000 |
| Pressure transducers (8) | Own | $6,000 |
| Magnetron igniter (5 kW) | Own | $4,000 |
| Fuel system | Own | $3,000 |
| Instrumentation (TC, flow) | Own | $5,000 |
| Test stand structure | Own | $3,000 |
| Safety equipment | Own | $3,000 |
| **Phase 1 Total** | | **~$65,000** |

---

### Phase 2: RDE + MHD Demonstrator (10-20 kN)

```
PHASE 2 MANUFACTURING FLOW
═══════════════════════════

3D PRINT                        CONVENTIONAL MANUFACTURE            PROCURE
┌──────────────────┐           ┌──────────────────────┐           ┌──────────────────┐
│ LPBF (Inconel):  │           │ C/SiC Liners:        │           │ Magnets:          │
│ • Larger RDE shell│          │ • RDE inner liner     │           │ • Cu coils (1-2T) │
│ • Injector plate  │          │ • MHD gen walls       │           │   (NOT supercon-  │
│ • MHD outer casing│          │ • MHD accel walls     │           │   ducting yet)     │
│ • Nozzle shell    │          │ Outsource: CoorsTek   │           │ • Power supply    │
│ • Manifolds       │          │                       │           │                    │
│                   │          │ W-Cu Electrodes:      │           │ Instrumentation:  │
│ LPBF (GRCop-42): │          │ • 112 pieces          │           │ • Sensors         │
│ • RDE cooling     │          │ • Press-sinter-infil  │           │ • DAQ upgrade     │
│   jacket          │          │                       │           │ • ECU             │
│                   │          │ BN Insulators:        │           │                    │
│ EBM (Ti-6Al-4V): │          │ • 56 pieces           │           │ Cooling System:   │
│ • Intake (larger) │          │ • CNC from billet     │           │ • Pumps           │
│                   │          │                       │           │ • Heat exchanger  │
│                   │          │ TBC Coatings:         │           │ • Plumbing        │
│                   │          │ • APS on all hot parts│           │                    │
└────────┬─────────┘          └──────────┬───────────┘           └────────┬───────────┘
         │                               │                                │
         └───────────────────┬───────────┘────────────────────────────────┘
                             │
                             ▼
                  ┌─────────────────────────┐
                  │   ASSEMBLY & TEST       │
                  │   • Sub-module assembly  │
                  │   • MHD stack build      │
                  │   • System integration   │
                  │   • Cold flow test       │
                  │   • MHD power test       │
                  │   • Hot fire test        │
                  └─────────────────────────┘
```

---

### Phase 3: Full-Scale HPM-120 (120 kN)

This phase introduces the advanced metallurgy alloys and superconducting magnets:

```
PHASE 3 MANUFACTURING FLOW
═══════════════════════════

3D PRINT                     POWDER METALLURGY              CVI / COATING         PROCURE
┌────────────────────┐      ┌──────────────────────┐      ┌──────────────────┐   ┌──────────────┐
│ LPBF (IN718/625):  │      │ SPS + HIP:           │      │ C/SiC Liners:    │   │ SC Magnets:  │
│ • RDE outer shell  │      │ • W-Re-HfC liner     │      │ • MHD walls      │   │ • NbTi 2-4T  │
│ • Nozzle shell     │      │   inserts             │      │ • Nozzle inner   │   │ • Cryostats  │
│ • Brackets         │      │ • NbMoTaW-Re RHEA    │      │                  │   │ • LN₂ system │
│ • Manifolds        │      │   channel inserts     │      │ TBC (APS+EB-PVD):│   │              │
│                    │      │                      │      │ • GZO/YSZ bilayer│   │ Power:       │
│ LPBF (GRCop-42):  │      │ VAR + Extrusion:     │      │ • Ir coatings    │   │ • MHD power  │
│ • RDE cooling      │      │ • Nb-Si structural   │      │ • Bond coats     │   │   conditioning│
│   jacket (full)    │      │   shells             │      │                  │   │ • APU (50kW) │
│ • Nozzle cooling   │      │                      │      │ Pack Cementation:│   │              │
│   jacket           │      │ Press-Sinter-Infil:  │      │ • Silicide coat  │   │ Sensors:     │
│                    │      │ • W-La₂O₃/Cu graded  │      │   on Nb-Si parts │   │ • Full suite │
│ LPBF (Co-Re-Cr):  │      │   electrodes (112)   │      │                  │   │              │
│ • Transition       │      │                      │      │                  │   │              │
│   section          │      │ CNC:                 │      │                  │   │              │
│                    │      │ • BN insulators (56) │      │                  │   │              │
└────────┬───────────┘      └──────────┬───────────┘      └────────┬─────────┘   └──────┬───────┘
         │                             │                           │                     │
         └─────────────────┬───────────┘───────────────────────────┘─────────────────────┘
                           │
                           ▼
              ┌────────────────────────────┐
              │   FULL SYSTEM INTEGRATION  │
              │   • "Super Wall" assembly  │
              │   • MHD stack assembly     │
              │   • Magnet integration     │
              │   • Cryo system plumb-in   │
              │   • Full instrumentation   │
              │   • System-level tests     │
              │   • Progressive hot fire   │
              │   • Performance mapping    │
              └────────────────────────────┘
```

---

## Part 5: Equipment Investment Strategy

### Option A: Maximum Outsourcing (Recommended for Phase 1-2)

Buy only test/instrumentation equipment. Outsource all manufacturing.

| Category | Own | Outsource |
|----------|----:|----------:|
| Metal AM printing | $0 | $15K-250K (per phase) |
| HIP + heat treatment | $0 | $5K-30K |
| CNC finishing | $0 | $8K-50K |
| C/SiC liners | $0 | $250K-600K |
| Coatings (TBC, bond coat) | $0 | $30K-100K |
| Electrodes + insulators | $0 | $20K-50K |
| Test & instrumentation | $50K-80K | $0 |
| **Total Phase 1** | **~$65K** | **included** |
| **Total Phase 2** | **~$100K (add'l)** | **~$300K-600K** |
| **Total Phase 3** | **~$150K (add'l)** | **~$1.5M-3M** |

### Option B: Partial In-House (Phase 2+)

Buy a mid-range AM machine + post-processing basics. Outsource specialty processes.

| Equipment | Cost |
|-----------|-----:|
| EOS M290 (LPBF, handles IN718/625/GRCop/316L) | $500K-800K |
| Vacuum furnace (stress relief, aging) | $150K-300K |
| Wire EDM | $100K-200K |
| Small CNC mill (3-axis) | $80K-150K |
| Hardness tester, basic metrology | $20K-40K |
| Ar glove box (powder handling) | $15K-30K |
| **Subtotal** | **$865K-1.5M** |
| Still outsource: HIP, CT scan, C/SiC, magnets, coatings | Variable |

### Option C: Full In-House Capability (Phase 3 / Production)

| Equipment | Cost |
|-----------|-----:|
| EOS M400-4 (large LPBF) | $1.5-2.0M |
| EOS M290 or TRUMPF TruPrint (small/GRCop) | $500K-800K |
| HIP unit | $500K-2M |
| Vacuum furnace | $200K-400K |
| SPS system (advanced alloys) | $200K-500K |
| VAR (button/lab scale) | $50K-150K |
| Wire EDM + Sinker EDM | $200K-400K |
| 5-axis CNC | $300K-600K |
| APS plasma spray | $100K-200K |
| CMM | $100K-250K |
| CT scanner | $300K-800K |
| Ball mill + glove box + misc | $50K-100K |
| Facility (clean room, gas lines, safety) | $200K-500K |
| **Total** | **$4.2M-8.7M** |

---

## Part 6: Can You 3D Print the ENTIRE Engine?

**Short answer: No. About 45% by part count, but ~70% by structural mass can be 3D printed.**

### What MUST be conventionally made (no foreseeable AM path):

1. **C/SiC ceramic composite liners** — CVI is fundamentally a chemical deposition process, not additive manufacturing. Ceramic AM (binder jetting SiC, then CVI) is being researched but is 5-10 years from engine-grade maturity.

2. **Superconducting magnet coils** — NbTi wire must be drawn, twisted, and wound. This is a specialized wire/cable manufacturing process.

3. **BN insulators** — Hot-pressed BN billets are made by sintering BN powder at high pressure. CNC machining from billets is simpler and cheaper than any AM alternative.

4. **W-Cu electrodes** — The infiltration process (liquid Cu wicking into sintered W skeleton) produces a microstructure that AM cannot replicate. The Cu-filled pore network provides thermal conductivity paths that are optimized by the capillary infiltration physics.

5. **TBC and EBC coatings** — Thermal spray and EB-PVD are coating processes applied onto substrates. They are inherently not "printing" processes.

### What CAN be 3D printed today (production-ready):

| Part | Material | Why AM is Better |
|------|----------|------------------|
| RDE injector face plate | IN625 | **Impossible conventionally** — 24 integrated injectors + internal manifold in monolithic disc |
| RDE cooling jacket | GRCop-42 | Integral cooling channels, no braze joints, 25× thermal conductivity vs IN718 |
| RDE outer shell | IN718 | Conformal cooling channels integrated into wall |
| Nozzle outer shell | IN718 | Single-piece complex contour |
| Intake components | Ti-6Al-4V | Weight-optimized, topology-optimized brackets |
| Cooling manifolds | 316L | Complex plumbing paths in compact volume |

### Future possibility (3-5 years): Multi-material AM

Emerging multi-material AM systems could eventually print:
- W→Cu graded electrodes (DED with dual powder feed)
- IN718 shell with GRCop-42 cooling layer (dissimilar metal LPBF)
- Functionally graded TBC (ceramic AM + metal AM hybrid)

These are active research areas at NASA Glenn, ORNL, and several European institutions, but not production-ready.

---

## Part 7: Recommended Equipment Purchase Order

| Priority | Equipment | When | Cost | Justification |
|:--------:|-----------|------|-----:|---------------|
| 1 | Test stand + instrumentation | Phase 1 start | $50K | Cannot test without it |
| 2 | Service bureau contracts (AM, HIP, CNC) | Phase 1 start | $30K | Outsource all manufacturing |
| 3 | Basic metrology (hardness, calipers, gauges) | Phase 1 | $5K | In-house QC |
| 4 | EOS M290 (LPBF printer) | Phase 2 start | $500-800K | Iterate designs rapidly in-house |
| 5 | Wire EDM | Phase 2 | $100-200K | Cut parts from build plates, precision |
| 6 | Vacuum furnace | Phase 2 | $150-300K | In-house heat treatment |
| 7 | Ar glove box | Phase 2 | $15-30K | Handle GRCop-42, Ti powders safely |
| 8 | SPS system | Phase 3 prep | $200-500K | Advanced alloy development |
| 9 | Large-format LPBF (M400-4) | Phase 3 | $1.5-2M | Full-size parts |
| 10 | APS spray system | Phase 3 | $100-200K | In-house TBC coating |
