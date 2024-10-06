# IC50 Prediction Using Machine Learning

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
The cross-validation results showed an average **MAE** of 1.93, **RMSE**
of 2.48, and **R²** of 0.0981, explaining only about 9.81% of the
variance in LN_IC50 values. However, the scatter plot comparing
predicted to actual values yielded a correlation coefficient of
**0.81**, suggesting a strong positive correlation despite the model\'s
limited predictive power.

## **Cross-Validation Results**

| Fold | MAE        | MSE        | RMSE       | R²         | RMSLE      | MAPE       |
|------|------------|------------|------------|------------|------------|------------|
| 0    | 1.7943     | 4.8351     | 2.1989     | 0.0231     | 0.5793     | 1.6774     |
| 1    | 1.9792     | 7.1528     | 2.6745     | 0.2157     | 0.4838     | 1.1161     |
| 2    | 2.1220     | 6.8376     | 2.6149     | 0.3229     | 0.6880     | 1.3890     |
| 3    | 1.3267     | 2.8975     | 1.7022     | -0.1064    | 0.3661     | 0.4370     |
| 4    | 2.2110     | 9.0728     | 3.0121     | -0.1172    | 0.5543     | 0.7513     |
| 5    | 2.2051     | 6.9745     | 2.6409     | 0.2265     | 0.5580     | 0.7744     |
| 6    | 1.7715     | 4.4171     | 2.1017     | 0.0836     | 0.5206     | 1.6763     |
| 7    | 1.4848     | 5.2243     | 2.2857     | 0.1568     | 0.4129     | 1.3485     |
| 8    | 2.0118     | 6.6540     | 2.5795     | 0.0267     | 0.4846     | 0.9236     |
| 9    | 2.4033     | 9.0802     | 3.0133     | 0.1488     | 0.6500     | 2.2468     |
| Mean | **1.9310** | **6.3146** | **2.4824** | **0.0981** | **0.5298** | **1.2340** |
| Std  | **0.3210** | **1.8825** | **0.3904** | **0.1364** | **0.0938** | **0.5143** |

![](media/image1.png){width="4.90434820647419in"
height="3.407673884514436in"}

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
