
1.Objectives

Objective of this task is to derive a cutoff of one of the features and to find a combination of potentially diagnostic variables for the identification of benign vs. malignant 
tumors.

2.Dataset

The dataset consists of 569 examples of breast cancer biopsies. Each example has 32 variables. Out of the 32 variables, 30 are continuous features(biomarkers), one is an 
identification number, and the other is diagnosis. The diagnosis outcome is coded as “M” to indicate the tumor is malignant and as “B” to indicate the tumor is benign.
3.Exploratory Data Analysis(EDA)
Exploratory analysis was performed to describe the centrality, variability, and distributional behavior of the biomarkers. The mean was used as a measurement of central 
tendency, the standard deviation, range, and the coefficient of variation(CV) were used as measurements of variation, and skewness and kurtosis were used as measurements of
distribution shape. Also, as part of data exploration histogram of each biomarker by diagnosis (M vs. B) was visualized.
3.1.1.Summary Statistics

Descreptive statistics

![Descriptive](table_1.PNG)

Histogram of Biomarkers

![Histogram](figure_1.PNG)

According to the CV values, area_se (standard error of area), concavity_se(standard error of concavity), and concavity_mean(mean concavity) have the highest relative dispersion compared to other biomarkers.
 For a variable that has a perfect normal distribution, the skewness is 0 and the kurtosis is 3. From the values of skewness and kurtosis presented in Table 1, all biomarkers have distributions that are deviated from a normal distribution. However, their level of the deviations are different. For example, area_se (standard error of area) has a distribution that least resembles a normal distribution (skewness = 5.433 and kurtosis = 51.767). The biomarker that has the most close to normal distribution is smoothness_worst(skewness =0.414 and Kurtosis = 3.503). The histograms in Figure 1 also showed the deviations of the distributions of biomarkers from a normal distribution for malignant and benign tumors separately.
 
 4.Correlation Between Biomarkers
 
 One important step in predicting a certain outcome is analyzing the relationship between between features. This helps to see if candidate predictors are correlated or if they contain redundant information. To assess the relationship between biomarkers the Spearman’s rank correlation coefficients were calculated.
 
 ![Heatmap](figure_2.PNG)
