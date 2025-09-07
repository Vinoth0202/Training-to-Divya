## Title: Detection of Potential Phytochemicals for the development of Multi-Target Polyherbal formulation in Type 2 Diabetes management


1. Identification of anti-diabetic herbal plants (10 plants & availability)
2. Find the phytochemicals present in the herbal plants
3. Identify the targets to be inhibited that are causing the disorder
4. Collect the datasets for the 3 target molecules 
5. Find IC 50, Ki values from the SMILES/CSV bioactivity data
6. Train the datasets using the ML algorithm
7. Find the best predicted score
8. Identify 2-3 antidiabetic herbs
9. Do cross validation using wet-lab experiments
10. Find IC50 values by doing inhibition assays (repetitive)
11. Get the liquid extract of the final compound 
12. Get the powdered form of herbal formulation
13. Development of Prototype
14. Lab to Market


# Methodology

- **Disease**: Type 2 Diabetes Mellitus.
- **Approach**: Multi-target phytochemical/polyherbal strategy.
**End-product**: A **standardized herbal capsule or sachet** with reproducible potency (multi-target enzyme inhibition).

# Step 1. Collection of Phytochemical Compounds 

**Literature mining**
PubMed, Scopus, IMPPAT, PhytoHub, PubChem for anti-diabetic phytochemicals.
- Extract compound name, PubChem CID/SMILES, plant source, reported IC₅₀ against α-glucosidase, α-amylase, DPP-4, or PTP1B.
**Build your database**
- Spreadsheet: Plant → Compound → CID → SMILES → Reported Target(s) → IC₅₀ → Reference.

**Outcome → **Curated phytochemical library**.

# Step 2. In-silico Screening (Machine Learning + Docking)

**Descriptor calculation**
- Convert SMILES → 2D/3D structures (ChemAxon Marvin, RDKit).
- Compute molecular descriptors (PaDEL) → MW, XLogP, TPSA, H-bond donors/acceptors, ring counts, fingerprints.
**Machine Learning**
- Train QSAR models (Random Forest, Gradient Boosting) using literature IC₅₀ data.
- Predict activity of untested phytochemicals against each target.
- Rank top 20–30 candidates per target.
**Docking support**
- Dock top-ranked compounds to α-glucosidase, DPP-4, PTP1B PDB structures.
- Validate binding interactions with catalytic residues.

**Outcome→ **Ranked list of phytochemicals with predicted potency and docking scores**.

# Step 3. Select Plants & Extracts

- Choose **3–5 plants** rich in the prioritized phytochemicals (anchors = morin, catechin, rosmarinic acid, caffeic acid).
- Source authenticated raw material (farm/herbal suppliers).
- Prepare **hydro-ethanolic extracts** (50–70%).
- Standardize each extract with **HPLC/UPLC marker quantification**.

**Outcome → **Standardized plant extracts with defined marker content**.

# Step 4. In-vitro Validation (Wet Lab)

**Primary assays (multi-target)**
- α-Glucosidase (pNPG, A405 nm).
- α-Amylase (starch/DNS).
- DPP-4 (AMC fluorogenic substrate).
- PTP1B (pNPP colorimetric).
**Controls**: acarbose (α-glucosidase/α-amylase), sitagliptin (DPP-4), sodium orthovanadate (PTP1B).
**IC₅₀ determination**: dose-response curves, triplicates.
**Classify potency**: High (<50 µM), Moderate (50–100 µM), Low (>100 µM).

**Outcome → **Experimental IC₅₀ table for candidate compounds/extracts**.

# Step 5. Combine Literature + Experimental Data

- Add your new IC₅₀ results to the **literature dataset**.
- Retrain ML models → improve accuracy.
- Predict again → refine candidate list.
- This is the **active learning loop** (each experiment improves the model).

**Outcome → **Updated model + improved predictions**.

# Step 6. Synergy Testing for Polyherbal blend

1. Select **2–3 top compounds/extracts** per target.
2. Perform **checkerboard assays** (pairwise + 3-component).
3. Calculate **Combination Index (CI)** or Fractional Inhibitory Concentration (FIC).
- CI < 1 = synergy.
- CI ≈ 1 = additive.
- CI > 1 = antagonism.
4. Identify best synergistic mixtures across multiple targets.

**Outcome → **Synergistic multi-target blend 

# Step 7. Safety & ADMET Filtering

**In-silico ADMET**: SwissADME, pkCSM.
- Screen for oral absorption, hepatotoxicity, CYP inhibition, hERG risk.
**In-vitro safety**: MTT cytotoxicity in HepG2/3T3-L1.
- SI = CC₅₀ / IC₅₀ ≥ 10 is acceptable.

**Outcome → **Shortlisted phytochemicals extracts**.

# Step 8. Prototype Formulation

1. **Formulation type**: capsule/powder blend of standardized extracts.
2. **Composition**: optimized % ratios based on synergy + potency.
3. **Excipients**: microcrystalline cellulose, magnesium stearate, silica.
4. **Quality testing**:
- Marker assay (HPLC).
- Microbial load.
- Heavy metals/pesticides.
- Functional potency test (fixed-dose α-glucosidase inhibition).

**Outcome → **Pilot capsule**.

# Step 9. Stability & Scale-up

**Stability testing** (ICH Q1A):
- Accelerated (40 °C/75% RH, 3–6 months).
- Long-term (25 °C/60% RH, 12 months).
- Monitor marker content + potency.
**Scale-up extraction & blending** under GMP/AYUSH norms.

**Outcome → **Stable, standardized pilot-scale product**.
# Step 10. Tech Transfer → Market

- Prepare **tech dossier**: SOPs, batch records, assays, stability, safety.
- Regulatory: AYUSH nutraceutical filing (India) or dietary supplement path (US/EU).
- Branding, packaging, commercialization.

**Expected outcome**: A reproducible, standardized, multi-target **polyherbal anti-diabetic capsule**, validated by AI screening and wet lab validation.


# Plant List **## 

| S.No | Plant(Botanical) name     | Common name    | Phytochemical compound | Plant part | Identifier  | Reference (ISBN No:) |
| ---- | ------------------------- | -------------- | ---------------------- | ---------- | ----------- | -------------------- |
| 1    | Momordica charantia       | Bitter melom   | Charantin              | Fruit      | IMPHY002334 | 9770972795006        |
| 2    | Coccinia grandis          | Ivy gourd      | Beta-sitosterol        | Aeria part | IMPHY014836 | 9788171360536        |
| 3    | Curcuma longa             | Turmeric       | Curcumin               | Rhizome    | IMPHY007574 | 9780387706375        |
| 4    | Moringa oleifera          | Drumstick tree | Quercitin              | Flower     | IMPHY004619 | 9788172363130        |
| 5    | Trigonella foenum-graecum | Fenugreek      | Trigonelline           | Seed       | IMPHY005839 | 9788172361266        |
| 6    | Syzygium cumini           | Jamun          | Ellagic acid           | Bark       | IMPHY005537 | 9788171360536        |

# Multi-Targets that will get inhibited by the selected plant compounds

1. α-Glucosidase
2. Dipeptidyl Peptidase-4 (DPP-4)
3. Protein Tyrosine Phosphatase 1B (PTP1B)