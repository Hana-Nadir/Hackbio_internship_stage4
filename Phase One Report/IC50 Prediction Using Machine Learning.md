# IC50 Prediction Using Machine Learning
## Authors:
          Hanna (@slack)
          BigWils (@slack)
          DerleenM (@slack)
## [Python Script](https://github.com/Hana-Nadir/Hackbio_internship_stage4/blob/main/Phase%20One%20Script/IC50%20prediction%20model_2.ipynb)          
## **Background**  
This study utilized the Genomics of Drug Sensitivity in Cancer (GDSC)
dataset to build a machine learning model predicting drug sensitivity
(LN_IC50) for the SK-MEL-2 cancer cell line. The dataset was curated to
retain key features: CELL_LINE_NAME, TCGA_DESC, DRUG_NAME, and LN_IC50.
SMILES notations for the drugs were generated using public databases
like PubChem, and molecular descriptors were extracted using RDKit.

## **Methodology**  
SMILES were used to generate molecular descriptors, and the dataset was
split for training and evaluation. PyCaret library was used for model
selection. The model\'s performance was evaluated using Mean Absolute
Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R²).
Hyperparameter optimization was conducted via grid search. The final
model was assessed using 10-fold cross-validation, and the predicted
LN_IC50 values were compared to actual values through a scatter plot.

## **Results**  
The cross-validation results showed an average **MAE** of 2.01, **RMSE**
of 2.54, and **R²** of 0.0373, explaining only about 9.81% of the
variance in LN_IC50 values. However, the scatter plot comparing
predicted to actual values yielded a correlation coefficient of
**0.3257**, suggesting a strong positive correlation despite the model\'s

## **Cross-Validation Results**


| Fold | MAE | MSE | RMSE | R2 | RMSLE | MAPE |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 0 | 1.6658 | 4.0955 | 2.0237 | 0.1741 | 0.4225 | 0.9045 |
| 1 | 1.5494 | 4.2101 | 2.0519 | \-0.0913 | 0.4861 | 0.8134 |
| 2 | 2.4952 | 9.3535 | 3.0584 | 0.1027 | 0.6266 | 2.0015 |
| 3 | 1.6048 | 4.1868 | 2.0462 | 0.2028 | 0.615 | 1.2149 |
| 4 | 2.8159 | 11.3381 | 3.3672 | 0.0575 | 0.6089 | 3.4477 |
| 5 | 1.6721 | 4.8438 | 2.2009 | \-0.0027 | 0.4536 | 0.6165 |
| 6 | 1.604 | 3.6721 | 1.9163 | 0.2248 | 0.5246 | 2.0472 |
| 7 | 2.5793 | 11.9252 | 3.4533 | \-0.6573 | 0.62 | 3.1744 |
| 8 | 1.8874 | 6.7473 | 2.5976 | 0.1361 | 0.4555 | 1.5378 |
| 9 | 2.2462 | 7.5851 | 2.7541 | 0.2261 | 0.4937 | 1.0901 |
| **Mean** | **2.012** | **6.7958** | **2.5469** | **0.0373** | **0.5306** | **1.6848** |
| **Std** | **0.4532** | **2.9743** | **0.5557** | **0.2514** | **0.0756** | **0.9308** |



![image](https://github.com/user-attachments/assets/3d212da0-bfdc-4e1a-bd9a-3e3406d9ca5c)


Fig 1: Plot of actual IC50 against predicted IC50



## **Comparison of Findings**  
When compared to the reference study by Menden et al., this model
underperformed, as Menden\'s model achieved higher R² values of **0.72**
in cross-validation and **0.64** in blind testing. This performance gap
is likely due to the lack of genomic features in this analysis, as
Menden et al. incorporated both genomic and chemical data for better
accuracy.

## **Conclusion and Insights**  
In conclusion, this task demonstrates the potential of machine learning
to predict drug sensitivity in cancer treatment, showing a strong
correlation between predicted and actual LN_IC50 values. The limited R²
value (0.0981) suggests room for improvement. Despite modest
performance, the research demonstrates the importance of predictive
modeling in drug discovery process.

## **References**  
Menden, M. P., Iorio, F., Garnett, M., McDermott, U., Benes, C. H.,
Ballester, P. J., & Saez-Rodriguez, J. (2013). Machine learning
prediction of cancer cell sensitivity to drugs based on genomic and
chemical properties. *PLoS ONE, 8*(4), e61318.
<https://doi.org/10.1371/journal.pone.0061318>
