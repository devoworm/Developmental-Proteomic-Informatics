## Welcome to the Developmental Proteomics Informatics for _C. elegans_ project.

### This bioinformatics pipeline was constructed by Suroush Bastani over Summer 2024.

__Instructions:__
1. Each .zip file includes two .json files that must be used in conjunction with the Biopython-pipeline.ipynb file.

2. Biopython pipeline communicates with the [NCBI Protein Database](https://www.ncbi.nlm.nih.gov/protein). 

3. For additional methods, please see the methods from the following paper: Alicea, B., Bastani, S., Gordon, N.K., Crawford-Young, S., and Gordon, R.G. (2024). The Molecular Basis of Differentiation Wave Activity in Embryogenesis. _BioSystems_, 105272 (see [arXiv version](https://www.biorxiv.org/content/10.1101/2024.06.04.597397v1) for open access
# C. elegans Protein Extraction Pipeline 🪱

**A DevoWorm / OpenWorm Studentship Project**

## 📖 About This Project

This repository provides an automated, open-source pipeline to extract and analyze protein sequence data specific to the nematode *Caenorhabditis elegans*.

Computational models of *C. elegans* embryogenesis, such as those exploring invariant cell lineages and differentiation waves (e.g., Alicea et al., 2024), must be grounded in underlying molecular biology. This tool uses Biopython and the NCBI API to automate BLAST searches against the non-redundant database, strictly filtering for the *C. elegans* proteome.

It allows researchers to rapidly pull homolog data, sequence alignments, and e-values for key developmental drivers without manual web scraping. Target proteins include:

- **Wnt Signaling Pathway:** APC, AXIN, and β-catenin, which help dictate cell fate and polarity.
- **Cell Cycle Regulators:** CDK-1 and Cyclin D, which drive the timing of lineage divisions.
- **Kinase Cascades:** MAPK and JNK, which transduce developmental signals.

## 🗂️ Repository Contents

- `DevoWorm_Protein_Pipeline.ipynb`: The main Jupyter Notebook containing the automated extraction pipeline.
- `requirements.txt`: The Python dependencies required to run the code.
- `Alicea et al.pdf`: Reference literature detailing the differentiation wave models this pipeline supports.

## ⚙️ How to Use This Pipeline

### 1. Clone the Repository

Clone this repository to your local machine using your terminal:

```bash
git clone https://github.com/bastanisl/owproject.git
cd owproject
```

### 2. Install Dependencies

Ensure you have Jupyter installed, then install the required Python libraries:

```bash
pip install -r requirements.txt
```

### 3. Run the Notebook

Launch Jupyter:

```bash
jupyter lab
```

Open `DevoWorm_Protein_Pipeline.ipynb` and run the cells sequentially. The notebook includes Markdown explanations describing how to modify the protein targets and parse the resulting JSON data.

## 📊 What the Data Shows

The pipeline outputs structured JSON files containing `BlastOutput2` objects. These files contain:

- Confirmed *C. elegans* homolog accession IDs.
- E-values indicating the statistical significance of each match.
- Sequence identity and alignment lengths.

This data can be directly integrated into downstream systems biology models to bridge theoretical lineage waves with actual genomic sequence data.

## 👨‍🔬 Author

**Soroush Bastani**  
Developed as part of the OpenWorm Foundation Studentship.
