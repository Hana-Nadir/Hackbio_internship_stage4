# **Virtual screening of Histone deacetylases subtypes : a Molecular Docking Study** 

---
## Authors
        Hanna (@slack)
        BigWils (@slack)
        DerleenM (@slack)
## [Python Script](https://github.com/Hana-Nadir/Hackbio_internship_stage4/blob/main/Phase%20Two%20Script/Generating_Means_STDs_And_Heatmaps_for_the_docking_results_2.ipynb)
## **Introduction and Background :**

Histone deacetylases (HDACs), are critical enzymes in the regulation of gene expression through the removal of acetyl groups from histones. This condenses chromatin with a resulting reduction in its transcription. Overexpression or misregulation of HDACs has been implicated in the growth and progression of tumors due to the silencing of tumor suppressor genes, promoting uncontrolled cell growth.

HDAC inhibitors have emerged as promising anti-cancer agents. Current interest is being developed for selective inhibitors targeting specific HDAC subtypes because each subtype has distinct biological functions. Selective inhibitors may increase therapeutic efficacy while minimizing off-target effects. 

## **Methodology :**

### **Protein Structure Preparation**

The 3D structures of the first 10 HDAC subtypes were retrieved from the Protein Data Bank (PDB), while HDAC11 was modeled using AlphaFold . Proteins were prepared using both PyMOL and Discovery Studio, where water molecules, bound ligands, and heteroatoms were removed, hydrogens were added. The prepared protein structures were saved in PDB format for docking simulations.

### **Ligand Library Curation**

The ligand library consisted of 61 compounds, including 11 known inhibitors (one for each HDAC subtype) and 50 phytochemicals. The chemical structures of the ligands were obtained in SDF format and prepared for docking using Open Babel (O'Boyle et al., 2011).

### **Molecular Docking Procedure**

The molecular docking study was conducted using PyRx. All 61 ligands were docked into the active site of each HDAC subtype. Active sites were identified using PrankWeb . To ensure reliability, triplicate docking simulations were performed for each protein-ligand pair, and docking scores (binding affinities) were calculated in kcal/mol. Mean and standard deviation values were computed to determine the ligands with the highest and most consistent binding affinities toward each HDAC subtype.

## **Results and Interpretation :**

### **Docking Score Analysis**

The docking analysis revealed TMP269 and TMP195 as top ligands, with high affinity for multiple subtypes. TMP269 exhibited the strongest binding to HDAC8 (−11.5 kcal/mol) and showed consistent interactions across HDAC1, HDAC3, HDAC7, HDAC10, and HDAC11. TMP195 demonstrated high affinity for HDAC2, HDAC5, HDAC6, and HDAC9. Standard deviations were generally low, indicating stable binding in triplicate dockings. These results highlight TMP269 and TMP195 as potent candidates for further HDAC-targeted drug discovery efforts.

| HDAC Subtype | Literature Inhibitor | PDB ID | Ligand with Highest Affinity (CID) | Mean of the Binding Affinity (kcal/mol) | Standard deviation |
| :---- | :---- | :---- | :---- | :---- | :---- |
| HDAC1 | Entinostat (MS-275) | 4bkx | 53344908 ([TMP269](https://pubchem.ncbi.nlm.nih.gov/compound/53344908)) | −8.5 | 0 |
| HDAC2 | Valproic acid | 4lxz | 67324851 ([TMP195](https://pubchem.ncbi.nlm.nih.gov/compound/67324851)) | \-5.9 | 1.09 |
| HDAC3 | RGFP966 | 4a69 | 53344908 ([TMP269](https://pubchem.ncbi.nlm.nih.gov/compound/53344908)) | \-8.9 | 0 |
| HDAC4 | TMP269 | 5zop | 6654 ([ALPHA-PINENE](https://pubchem.ncbi.nlm.nih.gov/compound/6654)) | \-5 | 0 |
| HDAC5 | LMK-235 | 5uwi | 67324851 ([TMP195](https://pubchem.ncbi.nlm.nih.gov/compound/67324851)) | \-9.5 | 0 |
| HDAC6 | Tubastatin A | 3phd | 67324851 ([TMP195](https://pubchem.ncbi.nlm.nih.gov/compound/67324851)) | \-9.1 | 0 |
| HDAC7 | BRD73954 | 3znr | 53344908 ([TMP269](https://pubchem.ncbi.nlm.nih.gov/compound/53344908)) | \-8.3 | 0 |
| HDAC8 | PCI-34051 | 2v5x | 53344908 ([TMP269](https://pubchem.ncbi.nlm.nih.gov/compound/53344908)) | \-11.5 | 0 |
| HDAC9 | TMP195 | [8Q9R](https://www.rcsb.org/structure/8Q9R)  | 67324851 ([TMP195](https://pubchem.ncbi.nlm.nih.gov/compound/67324851)) | \-7.8 | 0 |
| HDAC10 | LSL | [7SGG](https://www.rcsb.org/structure/7SGG)  | 53344908 [TMP269](https://pubchem.ncbi.nlm.nih.gov/compound/53344908) | \-10.1 | 0 |
| HDAC11 | FT895 |  | 53344908 ([TMP269](https://pubchem.ncbi.nlm.nih.gov/compound/53344908)) | \-8.53 | 0 |

Table 1: Molecular Docking Analysis of HDAC Subtypes.

### **Comparative Binding Affinities of Compounds Across HDAC Subtypes**


![image](https://github.com/user-attachments/assets/2d187f25-a07c-4da0-be8f-82ab69992ce4)


_Figure 1: HDAC Binding Affinity Heatmap. This heatmap visualizes the binding affinities of various compounds (represented by PubChem CIDs on the y-axis) across 11 HDAC subtypes (x-axis)._ 



### **Comparison with The Target Paper**

1. **HDAC11 Selectivity**: Baselious et al., 2024 highlighted FT895 as a selective HDAC11 inhibitor with a docking affinity of −8.53 kcal/mol  Our results confirmed TMP269 as the ligand with the highest affinity for HDAC11, with a similar binding score of −8.53 kcal/mol.  
2. **Cross-subtype Affinity**: While Baselious et al., 2024 focused primarily on HDAC11, our analysis includes all 11 HDAC subtypes. TMP269 and TMP195 demonstrated high affinities across multiple HDACs in our results, suggesting broader inhibitory potential compared to FT895.Our findings support TMP269 as a broad HDAC inhibitor with strong affinity for HDAC11.

### **Docking Poses Visualization**

(a)= describe the 3D structure of the ligand within the binding site.  
(b)= describe the 2D structure of the ligand and its interaction in the binding site**.**

**1- HDAC 1 :**


![image](https://github.com/user-attachments/assets/a238b0b8-002a-4072-944a-57db974cf130)

_Figure 2: TMP269 (CID-53344908)  in HDAC1 binding site ._



**2- HDAC2 :**



![image](https://github.com/user-attachments/assets/ef2f1c85-c6f6-4dba-bc7f-06ee50e30bc1)


_Figure 3: TMP195 (CID-67324851)  in HDAC2 binding site ._



**3- HDAC 3 :**



![image](https://github.com/user-attachments/assets/73337dee-3b60-41c3-912f-78ab7973bdf3)


_Figure 4: TMP269 in HDAC3 binding site ._




**4- HDAC 4 :**



![image](https://github.com/user-attachments/assets/4ad474f5-e478-4624-8bb1-b4f9aeca8219)


_Figure 5: Alpha-pinene (CID-6654) in HDAC4 binding site ._ 




**5- HDAC 5:** 



![image](https://github.com/user-attachments/assets/d3eb8692-6e24-4f7b-918d-95ca18e9cebb)


_Figure 6 : TMP269 in HDAC5 binding site ._




**6- HDAC 6 :**



![image](https://github.com/user-attachments/assets/90b3d448-0fd9-467c-9d65-c18d2a0bd776)


_Figure 7: TMP169 in HDAC6 binding site ._





**7- HDAC 7 :**



![image](https://github.com/user-attachments/assets/f8819174-8018-4a34-95bf-86cc28aaa5e5)


_Figure 8: TMP269 in HDAC7 binding site ._




**8- HDAC 8 :**



![image](https://github.com/user-attachments/assets/3c952b36-5454-4c7c-ad4b-5cc5b9d53587)


_Figure 9: TMP195 in HDAC8 binding site ._





**9- HDAC 9 :**



![image](https://github.com/user-attachments/assets/0d85064d-033a-4908-80e2-774aa045cb77)


_Figure 10: TMP195 in HDAC9 binding site ._






**10- HDAC 10 :**



![image](https://github.com/user-attachments/assets/87273f37-038f-4791-9265-60641e36f106)


_Figure 11: TMP269 in HDAC10 binding site ._






**11- HDAC 11 :**



![image](https://github.com/user-attachments/assets/228056b3-fd4e-433d-8856-82276c83c083)


_Figure 12: TMP269 in HDAC11 binding site ._





## **Conclusion :**

When comparing to the target paper, TMP269's binding affinity for HDAC11 mirrors that of FT895, However, TMP269's broader affinity profile, especially its strong interactions with other HDACs, positions it as a versatile inhibitor for cancer therapy, addressing a broader range of HDAC-driven oncogenic pathways. The low standard deviation in triplicate dockings indicates robust binding, further supporting these ligands as valuable leads for future therapeutic development.

---

## **References**

1. Balasubramanian, S., Ramos, J., Luo, W., Sirisawad, M., Verner, E., Buggy, J. J., & Dai, Y. (2008). A novel histone deacetylase 8 (HDAC8)-specific inhibitor PCI-34051 induces apoptosis in T-cell lymphomas. *Leukemia*, 22(5), 1026-1034.

2. Baselious, F., et al., 2024\. Structure‐based design of selective HDAC11 inhibitors using an optimized AlphaFold model. Chemical Biology & Drug Design, pp.1-13.

3. Butler, K. V., Kalin, J., Brochier, C., Vistoli, G., Langley, B., & Kozikowski, A. P. (2010). Rational design and simple chemistry yield a superior, neuroprotective HDAC6 inhibitor, Tubastatin A. *Journal of the American Chemical Society*, 132(31), 10842-10846.

4. Chinellato, M., Perin, S., Carli, A., Lastella, L., Biondi, B., Borsato, G., Di Giorgio, E., Brancolini, C., Cendron, L., & Angelini, A. (2024). Folding of class IIa HDAC derived peptides into α-helices upon binding to myocyte enhancer factor-2 in complex with DNA. \*Journal of Molecular Biology\*, \*436\*(9), 168541\. [https://doi.org/10.1016/j.jmb.2024.168541](https://doi.org/10.1016/j.jmb.2024.168541)

5. Fung, H. Y. J., Fu, S.-C., & Chook, Y. M. (2017). Nuclear export receptor CRM1 recognizes diverse conformations in nuclear export signals. \*eLife\*, \*6\*, e23961. [https://doi.org/10.7554/eLife.23961](https://doi.org/10.7554/eLife.23961)

6. Hai, Y., Jarrard, R. E., Zhao, L., Lee, D., & Tu, X. (2017). Selective Histone Deacetylase 10 (HDAC10) Inhibitors Developed Using a Scaffold-Based Approach Exhibit HDAC10 Isoform Potency and Selectivity. *ACS Medicinal Chemistry Letters*, 8(10), 970-973.

7. Krivák, R., & Hoksza, D. (2018). P2Rank: Machine learning-based tool for rapid and accurate prediction of ligand binding sites from protein structure. *Journal of Cheminformatics*, 10(1), 39\.  
8. Lauffer, B. E. L., Mintzer, R., Fong, R., Kaminker, J. S., & Heise, C. E. (2013). Histone deacetylase (HDAC) inhibitor kinetic rate constants correlate with cellular histone acetylation but not transcription and cell viability. \*Journal of Biological Chemistry\*, \*288\*(37), 26750-26759. [https://doi.org/10.1074/jbc.M113.493032](https://doi.org/10.1074/jbc.M113.493032)  
9. Lobera, M., Madauss, K., Pohlhaus, D., et al. (2013). Selective class IIa histone deacetylase inhibition via a nonchelating zinc-binding group. \*Nature Chemical Biology\*, \*9\*(5), 319–325. [https://doi.org/10.1038/nchembio.1223](https://doi.org/10.1038/nchembio.1223)

10. McQuown, S. C., Barrett, R. M., Matheos, D. P., Post, R. J., Rogge, G. A., Alenghat, T., ... & Wood, M. A. (2011). HDAC3 is a critical negative regulator of long-term memory formation. *Journal of Neuroscience*, 31(2), 764-774.

11. Millard CJ, Watson PJ, Celardo I, Gordiyenko Y, Cowley SM, Robinson CV, Fairall L, Schwabe JW. Class I HDACs share a common mechanism of regulation by inositol phosphates. Mol Cell. 2013 Jul 11;51(1):57-67. doi: 10.1016/j.molcel.2013.05.020. Epub 2013 Jun 20\. PMID: 23791785; PMCID: PMC3710971.  
12. O'Boyle, N. M., Banck, M., James, C. A., Morley, C., Vandermeersch, T., & Hutchison, G. R. (2011). Open Babel: An open chemical toolbox. *Journal of Cheminformatics*, 3(1), 33\.

13. Oehme, I., Deubzer, H. E., Wegener, D., Pickert, D., Linke, J. P., Hero, B., & Witt, O. (2009). Histone deacetylase 8 in neuroblastoma tumorigenesis. *Clinical Cancer Research*, 15(1), 91-99.

14. Olson, D. E., Wagner, F. F., Kaya, T., Gale, J. P., Aidoud, R., Rodriguez, R., & Holson, E. B. (2013). Discovery of the first histone deacetylase 6/8 dual inhibitor, TMP269, with activity in neurodegenerative disease models. *Journal of Medicinal Chemistry*, 56(24), 7316-7329.

15. Ouyang, H., Ali, Y. O., Ravichandran, M., Dhe-Paganon, S., Arrowsmith, C. H., & Zhai, R. G. (2012). Protein aggregates are recruited to aggresome by histone deacetylase 6 via unanchored ubiquitin C termini. \*Journal of Biological Chemistry\*, \*287\*(4), 2317-2327. [https://doi.org/10.1074/jbc.M111.316893](https://doi.org/10.1074/jbc.M111.316893)

16. Phiel, C. J., Zhang, F., Huang, E. Y., Guenther, M. G., Lazar, M. A., & Klein, P. S. (2001). Histone deacetylase is a direct target of valproic acid, a potent anticonvulsant, mood stabilizer, and teratogen. *Journal of Biological Chemistry*, 276(39), 36734-36741.

17. Qian, Y., Hu, X., Li, Z., & Zhang, X. (2019). FT895, a novel inhibitor of HDAC11, induces apoptosis and inhibits cell proliferation in diffuse large B-cell lymphoma. *Oncotarget*, 10(23), 2198-2211.

18. Saito, A., Yamashita, T., & Mariko, Y. (1999). A synthetic inhibitor of histone deacetylase, MS-275, induces differentiation of human myeloid leukemia cells. *Proceedings of the National Academy of Sciences*, 96(8), 4592-4597.

19. Santo, L., Hideshima, T., Kung, A. L., Tseng, J. C., Tamang, D., Yang, M., & Anderson, K. C. (2012). Preclinical activity, pharmacodynamic, and pharmacokinetic properties of a selective HDAC6 inhibitor, ACY-1215, in combination with bortezomib in multiple myeloma. *Blood*, 119(11), 2579-2589.

20. Schrödinger, LLC. (2015). The PyMOL molecular graphics system, version 1.8.  
21. Steimbach, R. R., Herbst-Gervasoni, C. J., Lechner, S., Stewart, T. M., Klinke, G., Ridinger, J., Géraldy, M. N. E., Tihanyi, G., Foley, J. R., Uhrig, U., Kuster, B., Poschet, G., Casero, R. A. Jr., Médard, G., Oehme, I., Christianson, D. W., Gunkel, N., & Miller, A. K. (2022). Aza-SAHA derivatives are selective histone deacetylase 10 chemical probes that inhibit polyamine deacetylation and phenocopy HDAC10 knockout. \*Journal of the American Chemical Society\*, \*144\*(41), 18861-18875. [https://doi.org/10.1021/jacs.2c05030](https://doi.org/10.1021/jacs.2c05030)  
22. Suk-Youl Park, Gwang Sik Kim, Hyo-Jeong Hwang, Taek-Hyun Nam, Hee-Sae Park, Jaeyoung Song, Tae-Ho Jang, Young Chul Lee, Jeong-Sun Kim, Structural basis of the specific interaction of SMRT corepressor with histone deacetylase 4, *Nucleic Acids Research*, Volume 46, Issue 22, 14 December 2018, Pages 11776–11788, [https://doi.org/10.1093/nar/gky926](https://doi.org/10.1093/nar/gky926)

23. Thomas, R. C., Kim, S. Y., Raffoul, J. J., & Drake, K. (2019). HDAC9 inhibition protects against oxidative stress-induced retinal degeneration in retinal pigment epithelial cells. *Biochemical and Biophysical Research Communications*, 511(1), 120-126.
24. Trott, O., & Olson, A. J. (2010). AutoDock Vina: Improving the speed and accuracy of docking with a new scoring function, efficient optimization, and multithreading. *Journal of Computational Chemistry*, 31(2), 455-461.  
25. Vannini, A., Volpari, C., Gallinari, P., Jones, P., Mattu, M., Carfí, A., De Francesco, R., Steinkühler, C., & Di Marco, S. (2007). Substrate binding to histone deacetylases as shown by the crystal structure of the HDAC8–substrate complex. \*EMBO Reports\*, \*8\*(9), 879-884. [https://doi.org/10.1038/sj.embor.7401047](https://doi.org/10.1038/sj.embor.7401047)  
26. Watson, P., Fairall, L., Santos, G., et al. (2012). Structure of HDAC3 bound to co-repressor and inositol tetraphosphate. \*Nature\*, \*481\*, 335–340. [https://doi.org/10.1038/nature10728](https://doi.org/10.1038/nature10728)  
          

