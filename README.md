# HDAC Inhibitor Docking and Machine Learning Project

## Project Overview

This repository contains all the materials for a research project focused on Histone Deacetylase (HDAC) inhibition, docking studies, and machine learning (ML) predictions related to cancer drug sensitivity. The project is divided into two main phases:

- **Phase One**: Utilizes machine learning to predict IC50 values for various cancer drugs using a curated dataset of inhibitors and relevant target proteins.
- **Phase Two**: Involves molecular docking analysis of HDAC subtypes with multiple inhibitors, including both validated compounds and phytochemicals, using PyRx and other docking tools.

---

## Repository Structure

- **Binding sites**: Contains the binding site information for each HDAC subtype used in the docking studies.
- **Curated Inhibitors**: Contains a list of the inhibitors (phytochemicals and validated inhibitors) used for docking.
- **Final docking result**: Contains CSV files and visualizations of the final docking results, including binding affinities and other relevant metrics.
- **Phase One Script**: Python scripts used for the IC50 prediction using machine learning models.
- **Phase Two Script**: Python scripts used for molecular docking and analysis of the docking results.
- **Prepared proteins**: Contains the prepared protein structures for all HDAC subtypes, which were used in the docking process.
- **Phase One Report**: Detailed report for the machine learning phase, including methodology, results, and analysis of the IC50 prediction.
- **Phase Two Report**: Detailed report for the docking analysis phase, including the methodology for protein and ligand preparation, docking pipeline, and result analysis.
- **Summary of Phase One's Target Paper**: A summary of the target paper related to ML-based cancer drug sensitivity prediction.
- **Summary of Phase Two's Target Paper**: A summary of the target paper that inspired the docking analysis of HDAC inhibitors.

---

## Key Features

1. **Machine Learning (Phase One)**: 
   - A machine learning pipeline to predict IC50 values for cancer drug sensitivity using a dataset of inhibitors.
   - Utilizes regression models and validation techniques for robust predictions.

2. **Molecular Docking (Phase Two)**:
   - Docking of 11 HDAC subtypes with 61 inhibitors (including phytochemicals).
   - Triplicate docking studies for each ligand-target pair to ensure reliable affinity scores.
   - Post-docking analysis includes heatmap generation and docking pose visualizations.

---

## How to Use This Repository

1. **Machine Learning (Phase One)**:
   - Navigate to the `Phase One Script` folder to find scripts for IC50 prediction.
   - The dataset and instructions for running the models are included in the report file within the `Phase One Report` folder.

2. **Molecular Docking (Phase Two)**:
   - The `Phase Two Script` folder contains Python code for running docking analyses.
   - You can explore the docking results in the `Final docking result` folder, where binding affinities are summarized.

3. **Prepared Data**:
   - The `Binding sites` and `Prepared proteins` folders contain necessary files for protein preparation and binding site analysis.

---

## Results Overview

- **Phase One (Machine Learning)**: The IC50 prediction models show strong predictive performance with key cancer inhibitors, validated against experimental data.
- **Phase Two (Molecular Docking)**: TMP269 and TMP195 ligands showed the highest affinities for HDAC subtypes, with HDAC8 exhibiting the best binding affinity for TMP269.

---

## Citations

This project is inspired by two key papers:
- **Phase One Paper**: Menden, M.P., Iorio, F., Garnett, M., McDermott, U., Benes, C.H., Ballester, P.J. and Saez-Rodriguez, J., 2013. Machine learning prediction of cancer cell sensitivity to drugs based on genomic and chemical properties. PloS one, 8(4), p.e61318.
- **Phase Two Paper**: Baselious, F., et al. (2024). Utilization of an optimized AlphaFold protein model for structure-based design of a selective HDAC11 inhibitor with anti-neuroblastoma activity. Archiv der Pharmazie.

---

## Acknowledgments
We thank [HackBio](https://course.thehackbio.com/) for providing this learning opportunity, which has allowed us to grow and apply our skills in drug discovery and computational biology.

