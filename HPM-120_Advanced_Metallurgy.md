# HPM-120 Advanced Metallurgy: Metal Combinations for Extreme Performance

## Context & Operating Environment

The HPM-120 operates under conditions that push materials to their absolute limits:

| Zone | Gas Temperature | Wall Target | Pressure | Cycling |
|------|----------------|-------------|----------|---------|
| RDE Annulus | 3,500-4,000 K | <1,400 K | 15-25 bar | 1,500-2,000 Hz thermal pulses |
| MHD Generator | 3,500-4,000 K | <1,800 K | 10-15 bar | Continuous |
| MHD Accelerator | 3,000-3,500 K | <1,800 K | 5-10 bar | Continuous |
| Nozzle Throat | 2,400-3,000 K | <1,800 K | 3-8 bar | Continuous |

**Key constraints:** oxidation resistance, thermal shock resistance (microsecond detonation pulses), electrical conductivity (MHD electrodes), and structural integrity at extreme temperatures.

---

## Part 1: Periodic Table Survey of Candidate Metals

### Refractory Metals (Primary Candidates)

| Metal | Symbol | Z | Melting Point (K) | Density (kg/m³) | Key Property | Engine Relevance |
|-------|--------|---|-------------------|-----------------|--------------|------------------|
| **Tungsten** | W | 74 | 3,695 | 19,300 | Highest melting point of all metals | Electrodes, UHTC reinforcement |
| **Rhenium** | Re | 75 | 3,459 | 21,020 | Best creep resistance, ductile at high T | Alloying with W, Ni superalloys |
| **Tantalum** | Ta | 73 | 3,290 | 16,650 | Excellent corrosion resistance | Carbides for UHTC, alloying |
| **Osmium** | Os | 76 | 3,306 | 22,590 | Highest density, toxic OsO₄ | Not practical (toxic oxide) |
| **Molybdenum** | Mo | 42 | 2,896 | 10,220 | High stiffness, lower density than W | Silicides, HEA component |
| **Niobium** | Nb | 41 | 2,750 | 8,570 | Low density refractory, superconductive | Silicide composites, alloying |
| **Iridium** | Ir | 77 | 2,719 | 22,560 | Most corrosion-resistant metal known | Oxidation-resistant coatings |
| **Hafnium** | Hf | 72 | 2,506 | 13,310 | Forms highest-melting carbide (HfC: 4,232 K) | UHTC components |
| **Chromium** | Cr | 24 | 2,180 | 7,190 | Forms protective Cr₂O₃ oxide scale | Oxidation resistance in alloys |
| **Vanadium** | V | 23 | 2,183 | 6,110 | Lightweight refractory | HEA component |
| **Zirconium** | Zr | 40 | 2,128 | 6,506 | Forms ZrB₂ (UHTC), ZrO₂ (TBC) | Already used in TBC (YSZ) |

### Transition Metals (Superalloy Bases)

| Metal | Symbol | Z | Melting Point (K) | Density (kg/m³) | Key Property | Engine Relevance |
|-------|--------|---|-------------------|-----------------|--------------|------------------|
| **Nickel** | Ni | 28 | 1,728 | 8,908 | Stable FCC at all temps, γ/γ' strengthening | Superalloy base (current) |
| **Cobalt** | Co | 27 | 1,768 | 8,900 | Higher melting than Ni, γ/γ' possible | Next-gen superalloy base |
| **Iron** | Fe | 26 | 1,811 | 7,874 | Cheapest structural metal | Limited (too low T for hot section) |
| **Platinum** | Pt | 78 | 2,041 | 21,450 | Extreme oxidation resistance | Bond coat modifier |
| **Rhodium** | Rh | 45 | 2,237 | 12,410 | Catalytic, oxidation-resistant | Electrode surface coating |
| **Ruthenium** | Ru | 44 | 2,607 | 12,370 | Improves superalloy stability | 4th-gen superalloy additions |

### Light Metals (Structural/Alloying)

| Metal | Symbol | Z | Melting Point (K) | Density (kg/m³) | Key Property | Engine Relevance |
|-------|--------|---|-------------------|-----------------|--------------|------------------|
| **Titanium** | Ti | 22 | 1,941 | 4,507 | Best strength-to-weight | Intake (already used), aluminides |
| **Aluminum** | Al | 13 | 933 | 2,700 | Forms protective Al₂O₃ scale | Oxidation resistance in coatings |
| **Beryllium** | Be | 4 | 1,560 | 1,850 | Highest specific stiffness of any metal | Toxic; limited to specific uses |
| **Yttrium** | Y | 39 | 1,799 | 4,472 | Stabilizes oxide scales | TBC (YSZ), bond coat additive |

### Rare Earth & Actinide Elements (Specialist Roles)

| Metal | Symbol | Z | Melting Point (K) | Key Property | Engine Relevance |
|-------|--------|---|-------------------|--------------|------------------|
| **Lanthanum** | La | 57 | 1,193 | Oxide dispersion strengthening | W-La₂O₃ electrodes |
| **Cerium** | Ce | 58 | 1,068 | Oxygen getter, reduces oxide scale spalling | Bond coat additive |
| **Gadolinium** | Gd | 64 | 1,585 | Forms pyrochlore Gd₂Zr₂O₇ | Advanced TBC material |
| **Thorium** | Th | 90 | 2,023 | Excellent electron emitter | W-ThO₂ electrodes (radioactive, avoid) |

---

## Part 2: Recommended Alloy Combinations by Engine Section

---

### ALLOY 1: W-Re-HfC (RDE Liner & Hottest Sections)

**Composition:** W-3Re-0.5HfC (wt%)

**Why these metals together:**
- **W** (74): Provides the highest melting point of any metal (3,695 K) — the structural backbone
- **Re** (75): At 3-5 wt%, dramatically improves ductility and creep resistance of W. Re atoms distort the W lattice, inhibiting dislocation climb at high temperatures. Also eliminates the ductile-to-brittle transition temperature (DBTT), dropping it from ~400°C (pure W) to below room temperature
- **Hf** (72) as HfC: Hafnium carbide particles (melting point 4,232 K) pin grain boundaries via Zener pinning, preventing grain growth and creep. HfC is the highest-melting binary compound known

**Target properties:**
- Service temperature: up to 2,200 K (with cooling: survive 3,500 K gas)
- Tensile strength at 1,500 K: >200 MPa
- DBTT: below 200°C (vs 400°C for pure W)
- Density: ~19,400 kg/m³

**Manufacturing process:**

```
Step 1: Powder Preparation
├── Source W powder (99.97% purity, 1-5 μm particle size, FSSS)
├── Source Re powder (99.99% purity, <10 μm)
├── Source HfC powder (99.5% purity, <1 μm)
└── Weigh to composition: W-3Re-0.5HfC (wt%)

Step 2: Mechanical Alloying (Critical Step)
├── Load powders into WC-lined ball mill jars
├── Ball-to-powder ratio: 10:1
├── Milling atmosphere: Ultra-high purity Argon (O₂ < 1 ppm)
├── Milling speed: 250 RPM
├── Milling time: 40-60 hours
├── Result: Nanostructured composite powder with HfC uniformly distributed
└── Verify via SEM/EDS that HfC particles are <100 nm and uniformly dispersed

Step 3: Consolidation — Spark Plasma Sintering (SPS)
├── Load milled powder into graphite die (lined with BN spray)
├── Apply uniaxial pressure: 50-80 MPa
├── Heating rate: 100°C/min
├── Sintering temperature: 1,800-2,000°C
├── Hold time: 5-10 minutes
├── Atmosphere: Vacuum (<10 Pa) or flowing Argon
├── Cool under pressure to 800°C, then free cool
└── Result: >99% theoretical density billet

Step 4: Hot Isostatic Pressing (HIP) — Densification
├── Encapsulate SPS billet in Mo or Ta can
├── HIP temperature: 1,600-1,800°C
├── HIP pressure: 150-200 MPa (Argon gas)
├── Hold time: 2-4 hours
└── Result: 100% theoretical density, closed porosity eliminated

Step 5: Machining
├── Wire EDM (Electrical Discharge Machining) for rough shaping
├── Diamond grinding for final dimensions
├── Surface finish: Ra < 0.8 μm
└── Tolerance: ±0.05 mm

Step 6: Quality Control
├── Archimedes density measurement (target: >19,300 kg/m³)
├── Vickers hardness mapping (target: HV 450-550)
├── 3-point bend test at RT and 1,500°C
├── Microstructure: SEM + EBSD for grain size (target: 1-5 μm)
└── Non-destructive: Ultrasonic C-scan for internal defects
```

**Application on HPM-120:**
- RDE annulus inner liner (replacing C/SiC where thermal protection is insufficient)
- Nozzle throat insert
- RDE injector face plate upgrade

**Cost estimate:** ~$800-1,200/kg for finished parts

---

### ALLOY 2: Nb-Si-Ti-Hf-Cr (Next-Gen Structural Hot Section)

**Composition:** Nb-22Ti-16Si-5Cr-2Hf-2Al (at%)

This is an **in-situ composite** — not a conventional alloy. It forms two co-existing phases:
- **Nbₛₛ** (Niobium solid solution): Provides toughness and ductility
- **Nb₅Si₃** (Niobium silicide): Provides extreme creep resistance up to 1,500°C

**Why these metals together:**
- **Nb** (41): The matrix metal. Melting point 2,750 K, density only 8,570 kg/m³ (half of Ni-superalloys by volume). Forms the ductile Nbₛₛ phase and the creep-resistant Nb₅Si₃ intermetallic
- **Ti** (22): Partitions into both Nbₛₛ and Nb₅Si₃, lowering DBTT of the silicide phase and improving oxidation resistance. Reduces density further
- **Si** (14): Forms the Nb₅Si₃ strengthening phase. The silicide has a melting point of ~2,520 K and creep strength far exceeding any Ni-superalloy above 1,200°C
- **Cr** (24): Dramatically improves oxidation resistance by promoting a Cr₂O₃-based protective scale. Also forms Laves phase (Cr₂Nb) which adds strength
- **Hf** (72): Refines the Nbₛₛ/Nb₅Si₃ microstructure. HfO₂ pegs in the oxide scale prevent spallation. Improves creep life by 5-10× at 0.5-2 at%
- **Al** (13): Forms Al₂O₃ sub-scale beneath the outer oxide, providing a secondary oxidation barrier

**Target properties:**
- Service temperature: 1,450-1,550 K (vs 1,100 K for Inconel 718) — **a 350-450 K improvement**
- Density: ~6,800-7,200 kg/m³ (vs 8,190 kg/m³ for Inconel 718) — **12-17% lighter**
- Creep rupture life at 1,200°C/137 MPa: >1,000 hours
- Fracture toughness: 15-25 MPa√m

**Manufacturing process:**

```
Step 1: Vacuum Arc Melting (VAR)
├── Prepare consumable electrode:
│   ├── Stack alternating layers of Nb sheet, Ti sponge, Si chips, Cr pieces, Hf turnings
│   ├── Compact into electrode shape via cold isostatic press (CIP) at 200 MPa
│   └── Weld electrode tip to copper stinger
├── VAR parameters:
│   ├── Crucible: Water-cooled copper
│   ├── Atmosphere: Vacuum (<0.1 Pa)
│   ├── Arc current: 3,000-8,000 A (DC)
│   ├── Voltage: 25-35 V
│   ├── Melt rate: 5-10 kg/hr
│   └── Magnetic stirring: 5-15 Hz (homogenize)
├── Triple melt: VAR → flip ingot → VAR → flip → VAR
│   (3 melts minimum to ensure chemical homogeneity)
└── Result: ~100-200 mm diameter ingot, 300-500 mm long

Step 2: Homogenization Heat Treatment
├── Temperature: 1,500°C
├── Atmosphere: Argon (flowing, O₂ < 10 ppm)
├── Duration: 50-100 hours
├── Purpose: Dissolve casting segregation, equilibrate Nbₛₛ/Nb₅Si₃ phases
└── Cool: Furnace cool to RT (slow, ~2°C/min)

Step 3: Hot Extrusion (Critical for Microstructure Refinement)
├── Preheat billet to 1,400°C in Ar atmosphere
├── Extrusion ratio: 4:1 to 8:1
├── Ram speed: 25-50 mm/s
├── Lubricant: Glass-based (borosilicate type)
├── Jacket: Mo or steel canning to prevent oxidation
├── Die material: TZM (Mo-0.5Ti-0.1Zr)
├── Result: Refined Nbₛₛ/Nb₅Si₃ lamellar/eutectic microstructure
└── Phase size: Nbₛₛ lamellae 5-20 μm, Nb₅Si₃ 2-10 μm

Step 4: Directional Solidification (Alternative to Steps 1-3)
├── For turbine-blade-like components, DS or single crystal growth
├── Bridgman furnace with W-mesh heating elements
├── Temperature gradient: >30°C/cm
├── Withdrawal rate: 5-20 mm/hr
├── Result: Aligned Nbₛₛ/Nb₅Si₃ eutectic with superior creep resistance
└── Best for annular or cylindrical components

Step 5: Aging Heat Treatment
├── Temperature: 1,100°C
├── Atmosphere: Argon
├── Duration: 24-48 hours
├── Purpose: Precipitate fine secondary Nb₅Si₃ in the Nbₛₛ matrix for additional strengthening
└── Cool: Air cool (in Ar)

Step 6: Oxidation Protection Coating (MANDATORY — Nb oxidizes catastrophically above 500°C)
├── Apply Si-pack cementation coating:
│   ├── Pack composition: Si powder + NaF activator + Al₂O₃ filler
│   ├── Temperature: 1,050-1,150°C
│   ├── Time: 10-20 hours
│   ├── Atmosphere: Argon
│   └── Result: 20-50 μm NbSi₂/Nb₅Si₃ graded coating
├── Optional outer layer: Plasma-sprayed HfSiO₄ (hafnon) EBC
│   ├── Thickness: 50-100 μm
│   └── Purpose: Barrier against water vapor attack on SiO₂ scale
└── Coating service life: >500 hours at 1,300°C

Step 7: Machining
├── Rough machining BEFORE final heat treatment (material is more machinable)
├── Carbide tooling (TiAlN-coated)
├── Finish machining: CBN (cubic boron nitride) inserts
├── EDM for complex features
└── Coat AFTER final machining
```

**Application on HPM-120:**
- RDE outer shell (replacing Inconel 718, gaining 350-450 K temperature capability)
- MHD channel structural walls
- Nozzle structural shell
- Mounting brackets for hot section

**Cost estimate:** ~$400-700/kg for finished parts (less than Ni single-crystal superalloys)

---

### ALLOY 3: Refractory High-Entropy Alloy — NbMoTaW-Re (MHD Channel Extreme Environment)

**Composition:** Nb₂₅Mo₂₅Ta₂₅W₂₀Re₅ (at%)

High-entropy alloys (HEAs) are a revolutionary class of materials containing 4-5+ principal elements in near-equal proportions. The high configurational entropy stabilizes a single-phase solid solution (BCC in this case) rather than forming brittle intermetallics.

**Why these metals together:**
- **Nb** (41): Lowers density (8,570 kg/m³) vs W/Ta, stabilizes BCC structure, provides solid solution strengthening
- **Mo** (42): Excellent high-temperature strength contributor, moderate density (10,220 kg/m³), good oxidation resistance via MoO₃ volatilization (self-cleaning)
- **Ta** (73): Extreme melting point (3,290 K), outstanding corrosion resistance in hot combustion gases, strong solid-solution hardener
- **W** (74): Highest melting point anchor (3,695 K), dominant contributor to high-temperature strength, radiation resistance
- **Re** (75): The "ductilizer" — Re breaks up the directional bonding in BCC refractories, dramatically improving room-temperature ductility and fracture toughness. Also the strongest solid-solution strengthener per atom

**The high-entropy effect:**
The configurational entropy (ΔS_mix = R·ln(5) = 13.4 J/mol·K) stabilizes a random BCC solid solution, preventing the formation of brittle ordered phases (σ, μ, χ) that would form in binary or ternary combinations of these metals. This is the fundamental advantage: **you get the combined properties of all five refractory metals without the embrittlement that normally results from mixing them.**

**Target properties:**
- Melting range: ~2,900-3,100 K
- Yield strength at 1,600°C: >400 MPa (vs ~50 MPa for Inconel 718 at same temperature)
- Yield strength at RT: ~1,200 MPa
- Hardness: HV 500-600
- Density: ~13,500 kg/m³
- Crystal structure: Single-phase BCC

**Manufacturing process:**

```
Step 1: Vacuum Arc Melting (VAR)
├── Prepare consumable electrode:
│   ├── Use high-purity elemental pieces (>99.9%):
│   │   ├── Nb rod/sheet
│   │   ├── Mo rod
│   │   ├── Ta sheet
│   │   ├── W rod (may need to be pre-crushed or use W powder compact)
│   │   └── Re pellets
│   ├── Stack in calculated mass ratios for Nb₂₅Mo₂₅Ta₂₅W₂₀Re₅ (at%)
│   │   Mass ratio example (per 100g):
│   │   ├── Nb: 14.75g
│   │   ├── Mo: 15.23g
│   │   ├── Ta: 28.73g
│   │   ├── W: 23.35g
│   │   └── Re: 5.91g (actually Re: 17.94g for 5at%, need to recalculate)
│   └── Press into electrode via CIP or clamp mechanically
├── VAR parameters:
│   ├── Crucible: Water-cooled copper
│   ├── Vacuum: <0.01 Pa
│   ├── Arc current: 300-500 A (for button melts) or 3,000+ A (ingot)
│   ├── Electromagnetic stirring: essential due to high density differences
│   └── Remelt minimum: 5 times (flip and remelt) — MORE than conventional alloys
│       because of extreme melting point differences (W: 3,695 K vs Nb: 2,750 K)
└── Result: Homogeneous single-phase BCC ingot

ALTERNATIVE Step 1: Powder Metallurgy Route (Preferred for W-rich HEAs)
├── Source elemental powders:
│   ├── All 99.9%+ purity
│   ├── Particle size: 5-45 μm
│   └── Weigh to atomic composition
├── Mechanical alloying:
│   ├── WC-lined ball mill, WC balls
│   ├── BPR: 10:1
│   ├── Atmosphere: Ultra-high purity Ar
│   ├── Speed: 300 RPM
│   ├── Time: 30-50 hours
│   └── Monitor via XRD: single BCC peak = alloyed
├── Consolidation: Spark Plasma Sintering (SPS)
│   ├── Temperature: 1,700-1,900°C
│   ├── Pressure: 50-70 MPa
│   ├── Hold: 10-15 minutes
│   ├── Atmosphere: Vacuum
│   └── Density target: >98% TD
└── HIP: 1,500°C / 200 MPa / 3 hours → >99.5% TD

Step 2: Homogenization
├── Temperature: 1,800°C
├── Atmosphere: Vacuum or Ar
├── Duration: 24-48 hours
├── Purpose: Ensure single-phase BCC with no dendritic segregation
└── Verify: XRD (single BCC), SEM-EDS (composition variation <1 at%)

Step 3: Thermomechanical Processing
├── Hot forging or hot rolling:
│   ├── Temperature: 1,400-1,600°C
│   ├── Reduction: 50-80%
│   ├── Strain rate: 0.01-1 /s
│   └── Atmosphere: Ar-filled encapsulated can (Mo or steel)
├── This step is CRITICAL: breaks up cast dendrites, refines grain size
├── Without TMT, the as-cast HEA is coarse-grained and brittle at RT
└── Target grain size: 10-50 μm

Step 4: Annealing
├── Temperature: 1,200-1,400°C
├── Duration: 2-4 hours
├── Atmosphere: Ar or vacuum
├── Purpose: Relieve residual stress, achieve equiaxed grain structure
└── Cool: Furnace cool

Step 5: Machining
├── EDM only (too hard for conventional machining)
├── Wire EDM for profiles
├── Sinker EDM for cavities
├── Diamond grinding for surfaces
└── Electrochemical machining (ECM) for complex geometries

Step 6: Oxidation Coating (MANDATORY above 800°C in air)
├── Option A: Si-Cr-Fe pack cementation
│   ├── Creates MoSi₂-type protective coating
│   └── Service temp: up to 1,700°C in air
├── Option B: Ir electroplating
│   ├── Iridium is oxidation-resistant to >2,000°C
│   ├── Electrodeposit from IrCl₃ solution
│   ├── Thickness: 5-20 μm
│   └── Expensive but unmatched performance
└── Option C: ZrO₂-based TBC (same as current engine spec)
```

**Application on HPM-120:**
- MHD channel liner segments (replacing C/SiC in highest-stress areas)
- RDE annulus reinforcement rings
- Nozzle throat insert (where creep at >1,500°C is the failure mode)

**Cost estimate:** ~$1,500-3,000/kg (Re is the cost driver at ~$3,000/kg)

---

### ALLOY 4: GRCop-42 + Ir Coating (Regeneratively Cooled Sections)

**Composition:** Cu-4Cr-2Nb (at%) — NASA GRCop-42

**Why these metals together:**
- **Cu** (29): Highest thermal conductivity of any structural metal (400 W/m·K). Essential for regenerative cooling channel walls where heat must be conducted rapidly from gas-side wall to coolant
- **Cr** (24): Forms nanoscale Cr₂Nb Laves phase precipitates that pin dislocations. Unlike typical Cu alloys that soften above 300°C, GRCop retains 80% of its RT strength at 700°C
- **Nb** (41): Partners with Cr to form the Cr₂Nb intermetallic strengthening phase. The Cr₂Nb particles are thermodynamically stable up to ~1,000°C (unlike CuCrZr which over-ages above 500°C)

**Why not stay with Inconel for cooled walls?** Inconel 718 has thermal conductivity of only 11.4 W/m·K. GRCop-42's conductivity is **280 W/m·K** — 25× higher. This means:
- The temperature drop across the wall is 25× smaller
- Cooling is far more effective
- Thermal stresses are drastically reduced
- Thermal fatigue life increases by orders of magnitude

**Target properties:**
- Thermal conductivity: 280 W/m·K at RT, 250 W/m·K at 500°C
- Yield strength at RT: 255 MPa
- Yield strength at 500°C: 205 MPa
- UTS at RT: 420 MPa
- Low-cycle fatigue at 600°C: >10,000 cycles at 0.5% strain range
- Density: 9,130 kg/m³
- Max service temperature (with Ir coating): 800°C (cooled side), gas-side protected by Ir/ZrO₂

**Manufacturing process:**

```
Step 1: Gas Atomization
├── Melt Cu-4Cr-2Nb in vacuum induction furnace
├── Superheat to 1,350°C
├── Atomize with high-pressure Ar gas (4-6 MPa)
├── Collect powder: 15-53 μm fraction
├── Oxygen content: <200 ppm (critical for Cu)
└── Result: Pre-alloyed spherical powder with Cr₂Nb precipitates already formed

Step 2A: Selective Laser Melting / LPBF (Preferred for Complex Cooling Channels)
├── Machine: EOS M290 or similar
├── Laser power: 370 W
├── Scan speed: 800 mm/s
├── Layer thickness: 30 μm
├── Hatch spacing: 0.09 mm
├── Build atmosphere: Ar (O₂ < 100 ppm)
├── Baseplate: Cu or steel, preheated to 200°C
├── CRITICAL advantage: Can print integral cooling channels directly
│   ├── Channel cross-section: 2×3 mm (same as current HPM-120 spec)
│   ├── Self-supporting channel geometry (teardrop cross-section)
│   └── No brazing or diffusion bonding joints (which are failure initiation sites)
└── As-built density: >99.5%

Step 2B: Hot Isostatic Pressing (Alternative for Simple Shapes)
├── Fill can with atomized powder
├── Evacuate and seal
├── HIP: 900°C / 100 MPa / 4 hours
└── Result: fully dense billet

Step 3: Heat Treatment
├── Solution anneal: 950°C / 0.5 hr / Ar atmosphere
├── Rapid cool (water quench or fast gas cool)
├── Age: 500°C / 2 hours / Ar atmosphere
├── Purpose: Optimize Cr₂Nb precipitate size (50-200 nm) and distribution
└── Verify: TEM imaging of precipitate morphology

Step 4: Iridium Protective Coating (Gas-Side Surface)
├── Substrate prep: Grit blast to Ra 3-5 μm, ultrasonic clean
├── Deposition method: Electron Beam Physical Vapor Deposition (EB-PVD)
│   ├── Source: Ir ingot (99.9%)
│   ├── Beam voltage: 10 kV
│   ├── Deposition rate: 2-5 μm/hr
│   ├── Substrate temperature: 800-1,000°C
│   ├── Thickness: 10-30 μm
│   └── Atmosphere: Vacuum (<0.01 Pa)
├── Purpose: Ir does not oxidize below 2,000°C, protecting the Cu alloy
├── Alternative: Magnetron sputtering (lower cost, thinner 2-5 μm films)
└── Adhesion test: Scratch test, critical load >30 N

Step 5: (Optional) TBC Over Iridium
├── Apply 8YSZ via APS over the Ir layer
├── Thickness: 0.3-0.5 mm
├── Purpose: Further reduce heat flux into the Cu wall
└── This creates a Ir/YSZ duplex coating that is state-of-the-art for rocket thrust chambers

Step 6: Quality Control
├── Thermal conductivity measurement (laser flash method)
├── Tensile test at RT and 600°C
├── Coating adhesion (4-point bend + acoustic emission)
├── CT scan for internal channel integrity (AM parts)
└── Proof pressure test at 1.5× operating pressure
```

**Application on HPM-120:**
- RDE annulus cooling channel walls (replace Inconel 718 shell in cooled zone)
- RDE injector face plate (replace Inconel 625)
- Nozzle throat regenerative cooling jacket
- Any wall segment where heat must be moved from gas-side to coolant as efficiently as possible

**Cost estimate:** ~$200-400/kg (powder), ~$600-1,000/kg (AM-printed finished parts)

---

### ALLOY 5: W-La₂O₃-Cu Functionally Graded Electrode (MHD Electrodes)

**Composition:** Graded from W-1La₂O₃ (plasma side) → W-Cu 80/20 → Cu (coolant side)

**Why this combination improves on current W-Cu 80/20:**
- **W** (74): High melting point, resists arc erosion from MHD current flow
- **La** (57) as La₂O₃: Lanthanum oxide particles (1 wt%) dramatically reduce the **work function** of W from 4.55 eV to ~2.7 eV. This means electrons are emitted more easily from the electrode surface, reducing the voltage drop at the electrode-plasma interface and improving MHD efficiency by 5-15%. La₂O₃ also stabilizes grain boundaries, preventing recrystallization embrittlement
- **Cu** (29): Provides thermal conductivity for heat removal on the cooled back side

The **functional grading** means the composition transitions smoothly from pure refractory (plasma-facing) to high-conductivity (coolant-facing), eliminating the sharp interface in current W-Cu composites that causes thermal stress cracking.

**Manufacturing process:**

```
Step 1: Powder Preparation
├── Layer A (plasma face): W-1La₂O₃ powder
│   ├── W powder: 99.97%, 1-3 μm (Fisher sub-sieve)
│   └── La₂O₃ powder: 99.9%, <1 μm, 1 wt%
├── Layer B: W-20Cu powder
│   ├── W powder: 99.97%, 1-3 μm
│   └── Cu powder: 99.9%, <10 μm, electrolytic
├── Layer C: W-50Cu powder
├── Layer D: W-80Cu powder
├── Layer E (coolant face): Pure Cu powder
└── Each layer: ~1.5 mm thick → total ~8 mm electrode

Step 2: Layer-by-Layer Spark Plasma Sintering
├── Load powders into graphite die in sequence (Layer A first, Layer E last)
├── Separate layers with thin marker powder (0.1 mm) for later inspection
├── SPS parameters:
│   ├── Temperature: 1,100°C (compromise — Cu melts at 1,085°C,
│   │   so use 1,050°C with longer hold, OR use two-stage SPS)
│   ├── Alternative two-stage approach:
│   │   ├── Stage 1: SPS W-La₂O₃ layers alone at 1,800°C / 60 MPa / 5 min
│   │   └── Stage 2: Stack pre-sintered W part with Cu-rich layers, SPS at 1,000°C / 40 MPa / 10 min
│   ├── Atmosphere: Vacuum
│   └── Pressure: 40-60 MPa
└── Result: Graded electrode with continuous composition transition

ALTERNATIVE Step 2: Cu Infiltration of Graded W Skeleton
├── Create W-La₂O₃ skeleton with graded porosity:
│   ├── Dense (5% porosity) on plasma face
│   ├── Medium (20% porosity) in middle
│   └── High (50% porosity) on coolant face
├── Achieved by mixing W powder with different sizes of pore-former
│   (e.g., NH₄HCO₃ that decomposes during sintering)
├── Sinter skeleton: 2,000°C / H₂ atmosphere / 2 hours
├── Place Cu billet on porous face
├── Infiltrate: 1,150°C / H₂ atmosphere / 30 minutes
│   Cu wicks into the W skeleton by capillary action
└── Result: Graded W-Cu with natural gradient matching porosity gradient

Step 3: EDM Cutting
├── Wire EDM to cut individual electrodes from the billet
├── Cut to: 25 mm wide × channel-width long × 8 mm thick
└── 112 electrodes needed (48 + 64 for generator + accelerator)

Step 4: Surface Finishing
├── Plasma-facing surface: Polished to Ra < 0.4 μm
│   (reduces arc initiation sites)
├── Coolant-facing surface: Roughened to Ra 3-5 μm
│   (improves heat transfer to coolant)
└── Side surfaces: Ground flat, ±0.02 mm for fit with BN insulators

Step 5: Quality Control
├── Electrical conductivity profile (4-point probe across thickness)
│   Target: 5% IACS (plasma face) → 90% IACS (coolant face)
├── Thermal conductivity (laser flash, through-thickness)
│   Target: 100 W/m·K (plasma face) → 350 W/m·K (coolant face)
├── Microhardness profile (Vickers, 100g load, every 0.5 mm)
├── SEM cross-section imaging (verify gradient smoothness)
└── Thermionic emission test: Measure electron emission at 1,200°C
    Target: >5 A/cm² at 1,500 K (vs ~1 A/cm² for un-doped W-Cu)
```

**Application on HPM-120:**
- All 112 MHD electrode pairs (generator + accelerator)
- Improves MHD interaction efficiency by reducing electrode voltage drop
- Extends electrode life via La₂O₃ grain boundary stabilization

**Cost estimate:** ~$150-250 per electrode → ~$17,000-28,000 for full set of 112

---

### ALLOY 6: Co-Re-Cr-Ni (Emerging Superalloy for Intermediate Sections)

**Composition:** Co-17Re-23Cr-2.6C (wt%) — based on the Co-Re alloy system

**Why these metals together:**
- **Co** (27): Melting point 1,768 K (40 K higher than Ni). FCC/HCP transformation provides additional strengthening mechanisms not available in Ni-base alloys. Co-base alloys inherently resist sulfidation (hot corrosion from jet fuel sulfur)
- **Re** (75): In Co-Re alloys, Re raises the solidus temperature by ~200 K compared to conventional Co superalloys. Re is the heaviest common alloying element but provides unmatched solid-solution strengthening. Co-Re forms a stable HCP structure at high temperatures, unlike the FCC Ni-base alloys
- **Cr** (24): Essential for oxidation resistance. Forms protective Cr₂O₃ scale. In Co-Re, Cr also stabilizes the desired crystal structure
- **C** (6): Forms M₂₃C₆ and MC carbides that strengthen grain boundaries

**Why Co-Re instead of Ni-base?**
Ni-base superalloys (Inconel 718, CMSX-4) are limited to ~1,100-1,150°C. Above this, the γ' strengthening phase dissolves. Co-Re alloys maintain their strength to 1,200-1,300°C because their strengthening mechanism (solid solution + HCP structure) does not depend on precipitate phases that dissolve.

**Target properties:**
- Service temperature: up to 1,300°C (1,573 K) — 200°C above best Ni superalloys
- Yield strength at 1,100°C: >300 MPa
- Oxidation resistance: comparable to Ni superalloys with Cr₂O₃ scale
- Density: ~11,000 kg/m³ (heavier than Ni-base due to Re)

**Manufacturing process:**

```
Step 1: Vacuum Induction Melting (VIM)
├── Charge sequence (to manage Re melting):
│   ├── First: Melt Co in Al₂O₃ crucible under vacuum (<1 Pa)
│   ├── Add Cr (dissolves easily in molten Co)
│   ├── Add Re pellets gradually (Re melts at 3,459 K)
│   │   ├── Use superheating: hold Co-Cr melt at 1,650-1,700°C
│   │   ├── Re dissolves into the melt over 30-60 minutes
│   │   └── Stir electromagnetically to ensure dissolution
│   └── Add C last (as graphite rod, dipped into melt)
├── Pour into ceramic shell mold or permanent graphite mold
└── Result: As-cast ingot

Step 2: Investment Casting (for Complex Shapes)
├── Create wax pattern of engine component
├── Ceramic shell: Al₂O₃ + ZrSiO₄ (zircon) backup
├── VIM melt as above
├── Pour at 1,600°C into preheated shell (1,100°C)
├── For DS (directional solidification):
│   ├── Bridgman furnace
│   ├── Withdrawal rate: 3-5 mm/min
│   └── Thermal gradient: >40°C/cm
├── For equiaxed: air cool
└── Knockout, blast, and inspect

Step 3: HIP (Close Casting Porosity)
├── Temperature: 1,200°C
├── Pressure: 150 MPa Ar
├── Duration: 4 hours
└── Closes all internal microporosity

Step 4: Solution Heat Treatment
├── Temperature: 1,250°C
├── Duration: 4-8 hours
├── Atmosphere: Ar
├── Cool: Gas fan cool (fast, ~50°C/min)
└── Purpose: Homogenize, dissolve coarse carbides

Step 5: Aging
├── Temperature: 900-1,000°C
├── Duration: 16-24 hours
├── Atmosphere: Ar
├── Cool: Air cool
└── Purpose: Precipitate fine M₂₃C₆ carbides on grain boundaries

Step 6: Machining
├── Carbide tools with TiAlN coating
├── Cutting speed: 15-30 m/min (slow, hard material)
├── Copious coolant (water-soluble)
└── Grinding for final surfaces
```

**Application on HPM-120:**
- RDE-to-MHD transition section (highest thermal gradient zone)
- MHD channel outer casing (replacing Inconel 718 for higher temperature capability)
- Nozzle structural components

**Cost estimate:** ~$500-900/kg (Re content drives cost)

---

### ALLOY 7: Advanced TBC System — Gd₂Zr₂O₇ / YSZ Bilayer

**Composition:** Gadolinium zirconate (GZO) top layer + 8YSZ underlayer

This replaces the current single-layer 8YSZ TBC with a dual-layer system offering 30-40% lower thermal conductivity.

**Why these elements together:**
- **Gd** (64): Gadolinium in Gd₂Zr₂O₇ creates a **pyrochlore crystal structure** that has intrinsically lower thermal conductivity (1.5-2.0 W/m·K) than YSZ (2.2-2.5 W/m·K). The large Gd³⁺ ions create massive phonon scattering, disrupting heat conduction
- **Zr** (40): Forms the ZrO₂ backbone. In the pyrochlore structure, Zr and Gd occupy ordered sublattices, creating a superlattice that further scatters phonons
- **Y** (39): In the YSZ underlayer, yttrium stabilizes the tetragonal ZrO₂ phase. The YSZ layer is needed because GZO is chemically incompatible with the NiCrAlY bond coat (forms GdAlO₃ perovskite which causes delamination)

**Why the bilayer?**
- GZO has 30-40% lower thermal conductivity than YSZ → thinner coating for same protection, or lower wall temperature for same thickness
- GZO has superior sintering resistance → maintains porosity and low conductivity longer in service
- GZO is incompatible with alumina-forming bond coats → YSZ interlayer acts as a chemical barrier
- Combined effect: **100-200 K reduction in wall temperature** compared to current single YSZ

**Manufacturing process:**

```
Step 1: Bond Coat Application
├── Material: NiCrAlY (same as current spec)
├── Method: Low-Pressure Plasma Spray (LPPS) or HVOF
├── Thickness: 100-150 μm
├── Roughness: Ra 5-8 μm (for TBC adhesion)
└── Pre-oxidize: 1,080°C / 4 hr / low pO₂ → forms thin α-Al₂O₃ TGO

Step 2: YSZ Interlayer
├── Material: 8 wt% Y₂O₃-ZrO₂ (8YSZ)
├── Method: EB-PVD (for columnar structure, better strain tolerance)
│   ├── Source: 8YSZ ingot
│   ├── Beam power: 40-50 kW
│   ├── Substrate temperature: 1,000°C
│   ├── Rotation: 5-20 RPM
│   ├── Deposition rate: 3-5 μm/min
│   └── Thickness: 100-150 μm
├── Purpose: Chemical barrier between GZO and bond coat
└── Columnar microstructure provides strain tolerance for thermal cycling

Step 3: GZO Top Layer
├── Material: Gd₂Zr₂O₇ powder (spray-dried & sintered, 20-80 μm)
├── Method: Air Plasma Spray (APS)
│   ├── Plasma gun: Metco 9MB or similar
│   ├── Primary gas: Ar, 40 SLPM
│   ├── Secondary gas: H₂, 8 SLPM
│   ├── Power: 35-45 kW
│   ├── Spray distance: 100-120 mm
│   ├── Feed rate: 30-50 g/min
│   └── Substrate temperature: maintain 200-300°C during spray
├── Thickness: 300-400 μm
├── Porosity target: 12-18% (for low thermal conductivity)
└── Alternative: EB-PVD for GZO too (better cyclic life, higher cost)

Step 4: Surface Sealing (Optional)
├── Laser glazing of GZO surface
│   ├── CO₂ laser, 500-1,000 W
│   ├── Scan speed: 50-100 mm/s
│   ├── Creates 20-50 μm dense surface layer
│   └── Purpose: Prevents infiltration by molten alkali seed (K₂CO₃/CsOH)
│       which would chemically attack the GZO
└── This is CRITICAL for HPM-120 given the alkali seed injection

Step 5: Quality Control
├── Adhesion: ASTM C633 tensile adhesion test (target: >20 MPa)
├── Thermal conductivity: Laser flash method on free-standing coating
│   Target: <1.5 W/m·K (GZO layer), <2.0 W/m·K (YSZ layer)
│   Effective through-thickness: <1.2 W/m·K (combined)
├── Thermal cycling test:
│   ├── 1,200°C / 5 min → forced air cool to RT / 5 min
│   ├── Target: >500 cycles without spallation
│   └── (Current YSZ achieves ~200-300 cycles — GZO/YSZ should exceed 500)
├── Phase analysis: XRD to confirm pyrochlore structure in GZO
└── Thickness: Metallographic cross-section measurement
```

**Application on HPM-120:**
- All hot-section surfaces currently using single YSZ TBC
- Particularly beneficial for RDE annulus where detonation thermal pulses are most severe
- The laser-glazed surface is essential to resist chemical attack from K₂CO₃/CsOH alkali seed

**Cost estimate:** ~$300-500/m² (vs ~$150-250/m² for single YSZ)

---

## Part 3: Material Selection Matrix

| Engine Section | Current Material | Proposed Upgrade | Temp Gain | Weight Impact | Key Benefit |
|---------------|-----------------|------------------|-----------|---------------|-------------|
| RDE Inner Liner | C/SiC | **W-3Re-0.5HfC** (Alloy 1) | +400 K service temp | +40% heavier | Survives detonation pulses |
| RDE Outer Shell | Inconel 718 | **Nb-Si-Ti-Hf-Cr** (Alloy 2) | +350-450 K | -15% lighter | Higher temp, lower density |
| RDE Cooling Walls | Inconel 718 | **GRCop-42 + Ir** (Alloy 4) | Same temp limit | +11% heavier | 25× thermal conductivity |
| RDE Injector Face | Inconel 625 | **GRCop-42 + Ir** (Alloy 4) | -300 K (but cooled) | +8% | Eliminates hot spots |
| MHD Channel Liner | C/SiC | **NbMoTaW-Re HEA** (Alloy 3) | +300-500 K | +4× heavier | Metallic toughness at 1,600°C |
| MHD Channel Casing | Inconel 718 | **Co-17Re-23Cr** (Alloy 6) | +200 K | +34% heavier | Higher temp structural |
| MHD Electrodes | W-Cu 80/20 | **W-La₂O₃/Cu graded** (Alloy 5) | Same | Same | 5-15% better MHD efficiency |
| All Hot TBCs | 8YSZ | **GZO/YSZ bilayer** (Alloy 7) | -100-200 K wall temp | Negligible | Alkali seed resistant |
| Nozzle Throat | C/SiC | **W-3Re-0.5HfC** (Alloy 1) | +400 K | +40% heavier | Eliminates UHTC need |

---

## Part 4: Combined "Super Wall" Stack for RDE Annulus

Integrating the best alloys into a single wall system for the most extreme zone (RDE):

```
HOT GAS SIDE — Rotating detonation wave (3,500-4,000 K)
    ↓
┌─────────────────────────────────────────────┐
│  Gd₂Zr₂O₇ TBC (Alloy 7)         0.4 mm    │  Thermal + alkali barrier
│  8YSZ interlayer                   0.15 mm   │  Chemical barrier
│  NiCrAlY bond coat                0.1 mm    │  Oxidation barrier
├─────────────────────────────────────────────┤
│  W-3Re-0.5HfC liner (Alloy 1)    3.0 mm    │  Extreme-temp structural wall
│  Ir diffusion barrier             0.02 mm   │  Prevents W-Cu interdiffusion
├─────────────────────────────────────────────┤
│  GRCop-42 cooling jacket (Alloy 4) 4.0 mm  │  25× better heat removal
│  [Internal cooling channels: 2×3 mm]        │  Jet fuel coolant @ 3.0 kg/s
├─────────────────────────────────────────────┤
│  Nb-Si-Ti-Hf-Cr shell (Alloy 2)  4.0 mm    │  Pressure vessel + structure
└─────────────────────────────────────────────┘
    ↓
COLD SIDE (~400-500 K)

Total wall thickness: ~12 mm
Estimated gas-side surface temp: ~1,800 K (with active cooling)
Estimated cold-side temp: ~500 K
Temperature drop through wall: ~1,300 K managed across 12 mm
```

**Improvement over current design:**
- Current wall thickness: 16-24 mm → New: 12 mm (33-50% thinner)
- Current thermal conductivity bottleneck: Inconel at 11.4 W/m·K → New: GRCop at 280 W/m·K
- Current TBC surface limit: 1,500 K → New GZO: 1,600 K
- Current structural temp limit: 1,100 K (Inconel 718) → New: 1,500 K (Nb-Si composite)

---

## Part 5: Supplier & Equipment Requirements

### Critical Equipment Needed

| Equipment | Purpose | Estimated Cost | Lead Time |
|-----------|---------|---------------|-----------|
| Spark Plasma Sintering (SPS) | W-Re-HfC, HEA consolidation | $200K-500K | 3-6 months |
| Vacuum Arc Melter (VAR) | Nb-Si composite, HEA, Co-Re melting | $150K-400K | 3-6 months |
| Hot Isostatic Press (HIP) | Densification of all PM alloys | $500K-2M (outsource) | N/A |
| Selective Laser Melting (SLM) | GRCop-42 printing with channels | $500K-1M | 3-6 months |
| Wire/Sinker EDM | Machining all refractory alloys | $100K-300K | 1-3 months |
| Air Plasma Spray (APS) | GZO/YSZ TBC coating | $80K-200K (outsource) | N/A |
| EB-PVD | Ir coating, columnar YSZ | $1M+ (outsource) | N/A |

### Key Material Suppliers

| Material | Supplier Examples |
|----------|-------------------|
| W, Mo, Re powders | Plansee (Austria), H.C. Starck (Germany), AMETEK (USA) |
| Nb, Ta, Hf metals | CBMM (Brazil, Nb), ATI (USA, Ta/Hf), Treibacher (Austria) |
| GRCop-42 powder | Elementum 3D (USA), NASA Glenn (license), Carpenter Additive |
| Gd₂Zr₂O₇ powder | Oerlikon Metco, Praxair Surface Technologies |
| C/SiC preforms | Safran Ceramics (France), CoorsTek (USA), SGL Carbon (Germany) |
| Ir metal | Heraeus (Germany), Johnson Matthey (UK) |

---

## Part 6: Development Priority Roadmap

### Priority 1 — Highest Impact, Lowest Risk
1. **GZO/YSZ bilayer TBC** (Alloy 7) — Drop-in replacement for current YSZ. No structural changes needed. Immediate 100-200 K wall temperature reduction.
2. **W-La₂O₃/Cu graded electrodes** (Alloy 5) — Direct replacement for current W-Cu 80/20. Improves MHD efficiency without any geometry changes.

### Priority 2 — High Impact, Moderate Risk
3. **GRCop-42 cooling jacket** (Alloy 4) — Requires redesign of cooling channel geometry but offers transformative improvement in heat removal. NASA TRL 7+ (flown on Artemis SLS RS-25 engine).
4. **Nb-Si composite structural shell** (Alloy 2) — Replaces Inconel 718 with 350-450 K higher temperature capability at lower weight. Requires oxidation coating development.

### Priority 3 — Highest Impact, Highest Risk
5. **W-Re-HfC liner** (Alloy 1) — Replaces C/SiC in hottest zones. Extremely high temperature capability but heavy and expensive. Justified only where C/SiC + TBC proves insufficient.
6. **NbMoTaW-Re RHEA** (Alloy 3) — Cutting-edge material, limited production experience. Pursue for Phase 3+ full-scale prototype.
7. **Co-Re superalloy** (Alloy 6) — Emerging class, limited supplier base. Consider for Phase 3.
