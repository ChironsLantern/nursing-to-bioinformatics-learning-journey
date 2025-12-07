
# 🧬 Amino Acids & Proteins 

---
## 1️⃣ Amino Acids

### What they are (EL5 + med)

Amino acids are **20 little LEGO people with different hats**.  
You snap them together into long chains; the hats decide how they behave:

- shy vs loud (hydrophobic vs hydrophilic)
    
- sticky vs slippery (charged vs neutral)
    
- bendy vs stiff (glycine vs proline)
    
- good at passing protons, making bonds, or getting tagged
    

Each amino acid has the same body plan:

- **α-carbon** (central carbon)
    
- **Amino group** (–NH₃⁺ at physiological pH)
    
- **Carboxyl group** (–COO⁻ at physiological pH)
    
- **Hydrogen**
    
- **R-group / side chain** → this is the “hat” that changes everything
    

The **R-group** determines:

- hydrophobic vs hydrophilic behavior
    
- charge at biological pH (positive, negative, neutral)
    
- ability to form hydrogen bonds
    
- whether it can form special bonds (e.g., disulfide)
    
- whether it is a good site for post-translational mods (phosphorylation, glycosylation, methylation, etc.)
    

### High-yield categories

**Hydrophobic (tend to bury inside proteins):**  
Val, Leu, Ile, Met, Phe, Trp, Pro, Ala

**Polar uncharged (like water, often on surfaces or in active sites):**  
Ser, Thr, Asn, Gln, Tyr, Cys

**Basic (+ charge at physiological pH):**  
Lys, Arg, His

**Acidic (– charge):**  
Asp, Glu

### Special players (EL5 notes baked in)

- **Glycine** – smallest; like a tiny hinge → adds flexibility
    
- **Proline** – rigid ring; breaks α-helices, creates kinks/turns → “kink brick”
    
- **Cysteine** – can form **disulfide bonds (S–S)** → molecular safety pins that lock structure
    
- **Histidine** – pKa near physiological pH → perfect for **acid/base catalysis** in active sites (proton relay friend)
    
- **Ser/Thr/Tyr** – favorite targets for **phosphorylation** → on/off switches in signaling
    

**EL5 translation:**  
Some LEGO people are tiny acrobats (Gly), some are stiff elbows (Pro), some can form handcuffs with each other (Cys), some are proton tossers in enzyme reactions (His), and some are “switch bricks” that the cell can tag with phosphate flags (Ser/Thr/Tyr).

### Bioinformatics (BIS lens)

- Amino acid properties (size, charge, polarity) form the basis of **substitution matrices** (PAM, BLOSUM).
    
- Conservation patterns in multiple sequence alignments point to:
    
    - conserved **catalytic residues** (often D, E, H, K, S, C)
        
    - conserved **binding motifs** (e.g., HxH, HxGH in metal-binding sites)
        
- Hydrophobic stretches of amino acids help predict:
    
    - **transmembrane helices** (hydropathy plots)
        
    - **signal peptides** (N-terminal hydrophobic patches)
        
- Post-translational modification sites are often predictable by motifs:
    
    - e.g. **Ser/Thr** in consensus sequences for kinases, **N-X-S/T** for N-glycosylation
        
- Features like disorder vs order, low complexity regions, and repeat motifs are all encoded at the amino acid level and matter for:
    
    - phase separation
        
    - signaling hubs
        
    - intrinsically disordered regions (IDRs)
        

---

## 2️⃣ Proteins: The Workers

### What proteins are (EL5)

Proteins are the **workers of the cell city**.

- DNA = recipe book
    
- mRNA = copied recipe
    
- Ribosome = kitchen
    
- Amino acids = ingredients
    
- Protein = finished worker (folded tool/robot)
    

The chain of amino acids folds into a shape that decides **what job** the protein does.

### Structure levels (med + BIS)

1. **Primary:** linear sequence of amino acids
    
2. **Secondary:** local patterns like **α-helices** and **β-sheets**
    
3. **Tertiary:** full 3D folding of a single chain
    
4. **Quaternary:** multiple chains assembling (dimers, tetramers, etc.)
    

Folding is driven by:

- hydrophobic collapse
    
- hydrogen bonds
    
- electrostatic interactions
    
- van der Waals forces
    
- disulfide bonds (Cys–Cys)
    

Bioinformatics connection:

- Tools like AlphaFold2 predict **3D structure** from the **primary sequence**, exploiting evolutionary covariation.
    
- Conservation + structure highlights:
    
    - active sites
        
    - binding pockets
        
    - interface surfaces
        
- Misfolding → disease (e.g., amyloids, CFTR ΔF508, etc.)
    

**EL5 translation:**  
You start with a string of beads, then it crumples into a very specific origami creature that can only do its job if the folds are just right.

---

## 3️⃣ Job 1 — Catalysts (Enzymes)

### EL5 anchor

Enzymes are **cooks** that make chemical reactions go fast.  
They have tiny pockets (**active sites**) that hug ingredients (**substrates**), lower the “effort hill” (activation energy), and let reactions happen quickly—without getting used up.

### Active site (med + BIS)

- 3D pocket with **specific shape** and **chemical environment**.
    
- Often lined with amino acids that:
    
    - donate/accept protons (His, Asp, Glu, Lys)
        
    - act as nucleophiles (Ser, Cys)
        
    - stabilize charged intermediates (Arg, Lys)
        
- Frequently designed to bind and stabilize the **transition state** more than the substrate itself.
    

Mutations in active site residues often cause:

- loss of function
    
- metabolic disease (e.g., enzyme deficiencies like PKU)
    

Bioinformatics notes:

- Active sites often show:
    
    - **strong conservation** across homologs
        
    - clustered catalytic residues in 3D space
        
- Can be detected/annotated using:
    
    - structural alignment to known enzymes
        
    - motif searches (e.g., HExGH, HxH, HxD patterns)
        
    - databases like CSA / MACiE (for catalytic site annotation)
        

**EL5 translation:**  
The active site is the exact-shaped mouth the cook uses to bite, hold, and transform the food.

---

## Allosteric Site & Regulation (extra pocket, extra magic)

### EL5 anchor

An allosteric site is a **second pocket** on the enzyme—far from the main working pocket—where a molecule can sit and **change the enzyme’s mood**.

- Happy sticker in that pocket → enzyme works **faster** (activation)
    
- Grumpy sticker → enzyme works **slower** (inhibition)
    

Allosteric = “other shape/place.”  
Something binds somewhere else → the whole protein **changes shape** → activity shifts.

### Structural & mechanistic reality (BIS + med)

- Allosteric sites are:
    
    - **topographically distinct** cavities
        
    - often at **domain** or **subunit interfaces**
        
    - connected to the active site via **long-range conformational networks**
        

Binding at an allosteric site causes:

- residue interaction network re-weighting
    
- changes in hydrogen bond networks
    
- disulfide switching (in some proteins)
    
- helix re-packing or β-sheet shearing
    
- shift between **T-state** (tense / inactive) and **R-state** (relaxed / active)
    

Types of allosteric regulation:

1. **Homotropic** — substrate itself is the effector (e.g., O₂ in hemoglobin)
    
2. **Heterotropic** — different molecule is the effector (e.g., ATP inhibiting PFK-1)
    
3. **Positive / Negative** — stabilizes active vs inactive conformations
    
4. **Conformational selection vs induced fit** — pre-existing ensemble vs ligand-driven change
    

Enzymes with allostery often show:

- **sigmoidal (S-shaped) kinetics** instead of hyperbolic
    
- **cooperativity** between subunits (when one subunit binds/activates, neighbors are more likely to activate)
    

**EL5 slide metaphor:**  
One kid goes down the slide → next kid thinks “that looks fun!” → more kids join → the curve of “kids using slide vs time” looks S-shaped, not a straight line.

### Metabolic and clinical importance

Allosteric enzymes are often **control points** in pathways:

- **PFK-1** in glycolysis:
    
    - ATP = grumpy sticker (inhibits)
        
    - AMP, F2,6BP = happy stickers (activate)
        
- **Pyruvate kinase**:
    
    - ATP inhibits
        
    - F1,6BP activates
        

They act as **traffic lights**:

- Green = pathway flows
    
- Red = pathway slows or stops
    

Dysregulation → metabolic disease, cancer, inborn errors.

### Bioinformatics & AI angle

Allosteric sites tend to:

- be **less conserved** than active sites (good drug targets)
    
- show **co-evolving residues** (correlated mutations)
    
- have high **network centrality** in residue interaction graphs
    
- appear as **cryptic pockets** in MD simulations (not obvious in static structures)
    

Tools / approaches:

- Pocket detection: fpocket, SiteMap, DoGSite
    
- Dynamics: MD + ENM/ANM, normal mode analysis, Markov state models
    
- Coevolution: EVcouplings, GREMLIN
    
- Conformational impact: DynaMut, ENCoM
    
- ML: models to predict allosteric sites and ligands for drug discovery
    

**EL5 translation:**  
You can find the secret mood pocket by looking at which parts of the protein wiggle together or change together in evolution.

---

## 4️⃣ Job 2 — Signaling

### EL5 anchor

Signaling proteins are **doorbells, radios, and walkie-talkies**.

One protein shouts “HEY!”  
Another hears it and changes what the cell does.  
Sometimes the message spreads into a whole **cascade** and ends up changing gene expression.

---

### GPCRs (G-Protein Coupled Receptors)

#### EL5 house metaphor

- Cell = house
    
- GPCR = **doorbell snake** in the wall (7 times in/out → 7 helices)
    
- Ligand (hormone, neurotransmitter) = someone pressing the doorbell
    
- Inside: **G-protein robot** with:
    
    - alpha arm
        
    - beta leg
        
    - gamma leg
        

Doorbell press → snake wiggles → robot wakes → splits and pushes buttons inside (make cAMP, open Ca²⁺ doors, etc.).  
If it’s pressed too often, the house gets annoyed, slaps “shame stickers” (phosphates) on the doorbell, and the babysitter (β-arrestin) drags it inside = **desensitization**.

#### Molecular / BIS version

- **Structure:**
    
    - 7-transmembrane α-helices
        
    - EC N-terminus (often for ligand binding)
        
    - IC C-terminus (interacts with G-proteins, GRKs, β-arrestins)
        
    - Conserved motifs: **DRY** on helix 3, **NPxxY** on helix 7
        
- **Activation sequence:**
    
    - Ligand binding → conformational change
        
    - Gα releases GDP → binds GTP
        
    - Gα–GTP dissociates from Gβγ
        
    - Both Gα–GTP and Gβγ regulate effectors (enzymes, ion channels)
        
    - GTP hydrolysis returns Gα to GDP-bound inactive state → reassociation
        
- **Gα families:**
    
    - **Gs** → activates adenylyl cyclase → ↑cAMP → PKA
        
    - **Gi/o** → inhibits adenylyl cyclase → ↓cAMP
        
    - **Gq/11** → activates PLC-β → PIP₂ → IP₃ + DAG → Ca²⁺ + PKC
        
    - **G12/13** → Rho GTPase signaling (cytoskeleton, migration)
        
- **Desensitization:**
    
    - GRKs phosphorylate active GPCR
        
    - β-arrestin binds phosphorylated tail
        
    - Receptor internalized via clathrin-coated pits
        
    - Recycled or degraded
        
    - Explains drug tolerance (e.g., opioids, β-agonists)
        

**Bioinformatics notes:**

- GPCRs are easily detected from sequence via:
    
    - 7-TM domain architecture
        
    - Class-specific motifs
        
- Families classified into Class A/B/C etc.
    
- ML + AlphaFold + MD used to:
    
    - predict active vs inactive conformations
        
    - identify ligand binding pockets and allosteric sites
        
- Bias signaling (G-protein vs β-arrestin pathways) is linked to specific conformational ensembles.
    

---

### Receptor Tyrosine Kinases (RTKs)

#### EL5 anchor

RTKs are **“grow and survive” doorbells**.  
Two receptors hug each other when the ligand binds, then start adding phosphate “power stickers” to their own tails and recruit signaling teams.

#### Med + BIS

- **Structure:**
    
    - Extracellular ligand-binding domain
        
    - Single transmembrane helix
        
    - Intracellular tyrosine kinase domain (with activation loop and conserved motifs: DFG, HRD, APE, VAIK)
        
- **Activation:**
    
    1. Ligand binding → receptors dimerize
        
    2. **Trans-autophosphorylation** of tyrosine residues
        
    3. Phosphotyrosines become **docking sites** for SH2/PTB-domain proteins
        
    4. Canonical cascade:  
        RTK → GRB2 → SOS → RAS–GTP → RAF → MEK → ERK → transcription factors (ELK1, c-Fos)
        
- **Examples:**
    
    - Insulin receptor (pre-formed dimer; uses IRS proteins → PI3K → AKT → mTOR)
        
    - EGFR (mutations in cancer; targeted by TKIs)
        
    - VEGFR (angiogenesis)
        

**Bioinformatics view:**

- RTKs are identified by **Pfam tyrosine kinase domains (PF07714)**
    
- Somatic mutations in RTKs are common in cancer; bioinformatics pipelines:
    
    - identify driver mutations (e.g., EGFR L858R)
        
    - map them to kinase domain structures
        
    - predict drug resistance (e.g., T790M)
        

---

### Ligand-Gated Ion Channels (LGICs)

#### EL5 anchor

These are **fast doors**.  
A neurotransmitter is the key; it binds, door opens, ions rush in or out → the electrical mood of the cell changes instantly.

#### Med + BIS

- Structure:
    
    - Often pentameric (nicotinic ACh, GABA-A) or tetrameric (NMDA)
        
    - Pore-forming transmembrane helices
        
    - Ligand-binding EC domain
        
- Mechanism:
    
    - Ligand binds
        
    - Conformational change → gate opens
        
    - Ion flux changes membrane potential
        
- Examples:
    
    - GABA-A: Cl⁻ influx → hyperpolarization (inhibition)
        
    - NMDA: Na⁺/Ca²⁺ influx; requires depolarization + co-agonist; blocked by Mg²⁺ at rest
        
    - Nicotinic ACh: Na⁺ influx → depolarization
        

**Bioinformatics:**

- Key motifs:
    
    - K⁺ channels: **GYG** in selectivity filter
        
    - Ionotropic glutamate receptors: **SYTANLAAF**
        
- MD simulations + homology models used to study:
    
    - gating motions
        
    - ion selectivity
        
    - drug binding (e.g., anesthetics, benzodiazepines)
        

---

### Second Messengers & Signal Amplification

#### Second messengers (quick list)

- **cAMP** – from ATP via adenylyl cyclase; activates PKA; changes gene expression via CREB.
    
- **cGMP** – via guanylyl cyclase; activates PKG; smooth muscle relaxation; regulated by PDEs.
    
- **IP₃** – soluble; releases Ca²⁺ from ER via IP₃ receptors.
    
- **DAG** – membrane-bound; activates PKC.
    
- **Ca²⁺** – universal; controls contraction, secretion, transcription, etc.
    
- **NO** – gaseous; diffuses; activates soluble guanylyl cyclase → cGMP.
    

#### Amplification (EL5 + BIS)

One ligand → one receptor → many G-proteins → many enzymes → hundreds or thousands of second messengers → many kinases → many phosphorylated targets.

Tiny whisper at the membrane → huge chorus inside the cell.

In modeling:

- represented via **cascades**,
    
- ODE systems,
    
- stoichiometric coefficients,
    
- network graphs.
    

#### Gene regulation cross-talk

Signals end up in the nucleus by:

- activating transcription factors (CREB, NF-κB, STATs, AP-1)
    
- modifying chromatin (acetylation, methylation)
    
- altering mRNA stability (AREs, miRNAs)
    
- affecting splicing regulators
    

Bioinformatics tools:

- motif scanning for TF binding sites
    
- ChIP-seq for occupancy
    
- RNA-seq for transcriptomic responses
    
- network inference for pathway reconstruction
    

**EL5 translation:**  
Protein doorbells talk to sparkles (second messengers), sparkles talk to light switches on DNA (transcription factors), and then the cell changes what it builds.

---

## 5️⃣ Job 3 — Structure

### EL5 anchor

Structural proteins are the **beams, ropes, and scaffolding** of the cell.  
Without them, the cell would sag into soup.

### Med + BIS

Key examples:

- **Collagen** – triple helix (Gly–X–Y repeats); provides tensile strength in skin, bone, tendons. Needs vitamin C for proline/lysine hydroxylation.
    
- **Elastin** – stretchy, crosslinked; in lungs, vessels, skin.
    
- **Actin** – microfilaments; cell shape, movement, muscle contraction (with myosin).
    
- **Tubulin** – microtubules; mitotic spindle, vesicle transport (dynein/kinesin), cilia/flagella.
    
- **Keratins** – intermediate filaments in epithelial cells; structural integrity of skin, hair, nails.
    

Disorders:

- Ehlers–Danlos (collagen defects)
    
- Osteogenesis imperfecta (Type I collagen)
    
- Epidermolysis bullosa (keratin/anchoring defects)
    

Bioinformatics:

- Repeats and motifs (Gly–X–Y in collagen, coiled-coil heptad repeats, etc.)
    
- Domain families for cytoskeletal proteins (actin-like, tubulin-like, IF domains)
    
- Structural prediction and MD used to study mechanical properties.
    

---

## 6️⃣ Job 4 — Energy / Gradient Generation

### EL5 anchor

Cells make **tiny batteries** by putting a lot of charged ions on one side of a membrane.  
Then they let the ions rush back through protein turbines to make **ATP**, the energy candy.

### Med + BIS

Key components:

- **Na⁺/K⁺-ATPase** – uses ATP to pump 3 Na⁺ out, 2 K⁺ in → maintains membrane potential.
    
- **Other pumps** – H⁺ pumps in lysosomes, Ca²⁺ pumps in ER and plasma membrane.
    

**Electron Transport Chain (ETC):**

- Inner mitochondrial membrane complexes I–IV:
    
    - Accept electrons from NADH/FADH₂
        
    - Pump protons into intermembrane space
        
    - Create **proton motive force (PMF)**
        

**ATP synthase (Complex V):**

- Protons flow back down gradient through ATP synthase
    
- Rotor turns → conformational changes in catalytic sites
    
- ADP + Pi → ATP
    

**Secondary active transport:**

- Uses existing gradients (e.g., Na⁺) to power transport of other solutes (e.g., Na⁺/glucose symporters in gut and kidney).
    

Disorders:

- Mitochondrial diseases → impaired oxidative phosphorylation → lactic acidosis, myopathies, neuropathies.
    
- Ion gradient disruption → arrhythmias, seizures, muscle weakness.
    

Bioinformatics:

- ETC and ATP synthase components are highly conserved; phylogenetics used to study mitochondrial evolution.
    
- Pathogenic mutations identified by:
    
    - variant calling in mtDNA / nuclear ETC genes
        
    - structural mapping to predict impact on proton channels, binding sites.
        

**EL5 translation:**  
The cell builds a wall, piles ions on one side, then uses the rushing “waterfall” of ions to spin a molecular waterwheel that makes ATP coins.

---

## 🔥 Final Hybrid Summary

- **Amino acids** = tiny LEGO pieces with different hats.
    
- **Proteins** = folded LEGO workers.
    

They do at least four core jobs:

1. **Catalysts (Enzymes)** – lower activation energy, speed up reactions; active sites and allosteric sites tune their behavior.
    
2. **Signaling** – GPCRs, RTKs, ion channels, second messengers; from membrane whispers to nuclear decisions.
    
3. **Structure** – collagen, elastin, actin, tubulin, keratin; beams, ropes, and scaffolds.
    
4. **Energy/Gradients** – pumps, ETC, ATP synthase; electric batteries and proton waterfalls.
    

**EL5:**  
Cells are cities, proteins are the workers, amino acids are the bricks, and gradients are their batteries.

**BIS:**  
Everything—from sequence alignments to structural modeling, pathway simulation, and drug design—rests on understanding how these amino-acid-based machines fold, signal, catalyze, scaffold, and harness energy.

---

