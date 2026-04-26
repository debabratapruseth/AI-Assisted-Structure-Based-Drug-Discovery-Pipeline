# AI-Assisted-Structure-Based-Drug-Discovery-Pipeline

![AlphaFold Protein](https://raw.githubusercontent.com/debabratapruseth/AI-Assisted-Structure-Based-Drug-Discovery-Pipeline/main/AlphaFold%20Protein%20Synthesis.png)

*Figure: AI-predicted protein structure using AlphaFold*

This project demonstrates an end-to-end AI-assisted structural biology workflow starting from a protein sequence and progressing to drug-binding hypothesis generation.

Using AlphaFold (via ColabFold) and molecular docking (AutoDock Vina), the pipeline:

- Predicts protein 3D structure from sequence  
- Evaluates structural confidence  
- Identifies potential binding regions  
- Simulates ligand docking  
- Extracts interacting residues  
- Generates a structured scientific interpretation using an LLM  

---

## Research Objective

> Can we use AI-predicted protein structures to generate plausible, explainable hypotheses for small-molecule binding?

---

## Target Protein

- Name: Dihydrofolate Reductase (DHFR)  
- Gene: folA  
- Organism: Escherichia coli  
- UniProt ID: P0ABQ4  

DHFR is a well-known enzyme involved in DNA synthesis, making it a classic target in drug discovery.

---

## Pipeline Architecture

- Sequence (FASTA)
- AlphaFold / ColabFold
- 3D Protein Structure (PDB)
- Confidence Analysis (pLDDT)
- Protein Preparation (PDBQT)
- Ligand Preparation
- Docking (AutoDock Vina)
- Binding Pose + Score
- Residue Interaction Mapping
- AI-Assisted Scientific Interpretation

---

## Key Results

### Structural Model Quality
- Mean pLDDT: 95  
- No low-confidence regions (<70)  
- Globally reliable structure  

### Docking Result
- Best binding affinity: ** -5.7 kcal/mol**  
- Indicates moderate, computationally plausible binding

### Interaction Analysis
- Residues within 4.5 Å identified  
- Suggests a potential binding region  

---

## AI-Assisted Interpretation

An LLM (OpenAI API) was used to:

- Translate raw computational outputs into scientific language
- Generate structured interpretation:
  - Objective  
  - Model quality  
  - Docking insights  
  - Limitations  
  - Next steps  

---

## Scientific Limitations

This project is exploratory and computational only.

- AlphaFold predicts structure, not dynamics  
- Docking scores are approximate  
- No experimental validation  
- Protein flexibility not modeled  

👉 Results represent hypothesis generation, not confirmed biology  

---

## Future Improvements

- Use known DHFR inhibitor (e.g., Methotrexate)  
- Perform docking against specific active site  
- Add molecular dynamics simulation  
- Compare multiple ligands  
- Integrate binding site prediction tools  

---

## Key Takeaway

> This project demonstrates how AI + structural biology + simulation tools can be combined to create interpretable, reproducible drug discovery workflows.

---

## Tech Stack

- AlphaFold / ColabFold  
- AutoDock Vina  
- Open Babel  
- Python (NumPy, Pandas, Matplotlib)  
- py3Dmol (3D visualization)  
- OpenAI API  

---

