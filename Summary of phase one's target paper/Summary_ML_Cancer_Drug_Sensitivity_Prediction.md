# **Summary of Predicting Cancer Drug Response with Machine Learning ,(Menden et al., 2013).**
## Authors : 
         Hanna (@slack)
         BigWils (@slack)
         DerleenM(@slack)
## Background         
This work demonstrates the use of machine learning in the prediction of
cancer cell line sensitivity to drugs based on genomic features and
chemical properties of drugs (Menden et al., 2013). The developed neural
network and random forest models integrate two key data streams:

1\) Genomic features of cancer cell lines, including mutations and copy
number variations

2\) Chemical descriptors of drugs

Using data from more than 600 cell lines and 111 drugs, their models
achieved a good prediction performance of drug sensitivity represented
by IC50 values both in cross-validation (R2 = 0.72) and blind tests (R2
= 0.64) (Menden et al., 2013). Importantly, the models were also capable
of predicting sensitivity for completely new cell lines not used in
training.

These models can be applied to the following uses, as suggested by the
authors (Menden et al., 2013):

1\) Optimization of experimental design by estimating missing drug
response data

2\) Make in silico predictions of novel drug efficacy using their
chemical characteristics

3\) Recognize candidates for drug repurposing

4\) Guide personalized cancer treatment by linking patient genomic
profiles to predicted drug responses

This work demonstrates how machine learning can integrate diverse data
types to accelerate the process of cancer drug discovery and development
(Menden et al., 2013).

## **Reference**

Menden, M.P., Iorio, F., Garnett, M., McDermott, U., Benes, C.H.,
Ballester, P.J. and Saez-Rodriguez, J., 2013. Machine learning
prediction of cancer cell sensitivity to drugs based on genomic and
chemical properties. PloS one, 8(4), p.e61318.
