### Project 1: Ames Housing Data and Kaggle Challenge


### Problem Statement

This project attempts to build a linear regression model which reliably predicts real estate prices in Ames, a college town with population of approx. 70,000, located in central Iowa.

### Summary

The modeling effort consisted of a number of iterations, each of which leveraged of a subset of provided data  describing 2,000+ properties through 81 characteristics including size, location, setup, access to amenities, age of the building, recency of renovations, and many others, as well as several variables engineered mostly as either binary representations of non-numeric data or combinations of variables.  
As a metric of model reliability, we used the mean R2 score that the model achieved when cross-validated between train and test data folds. The best performing model scored 0.8969, meaning it explained nearly 90% of the variation in Ames house pricing.

### Data Dictionary

The data dictionary for the original dataset can be found here: http://jse.amstat.org/v19n3/decock/DataDocumentation.txt. All variable transformations, including definitions of newly engineered features, are described in Part 3 of the attached notebook.

### Key Observations

1. The R2 score of the best model the team tested is 0.8969.
2. After careful selection of independent variables to "feed" the model, we've observed that further improvement of the score and the model's ability to more accurately predict the prices of unseen properties was hindered by the asymmetric distribution of the target variable.
3. Of all tactics applied in the iterations, the "brilliant basics" of removing outlier observations caused a surprisingly meaningful improvement in the model score, whereas more advanced methods such as variable scaling or coefficient regularization had little effect on the R2.

### Conclusions and Recommendations

As obvious as the lesson may seem, it is still hugely valuable: it doesn't pay to iterate on a complex model (or even a simple one) before investing time in understanding the data and separating signal from noise  by removing outliers.

---
### Next Steps

We noted when inspecting the results of subsequent iterations of the model that despite gradual improvement in the overall R2 score, the estimator continued to perform very poorly on those observations whose true prices exceeded $340,000.
While the team understood that this was due to the asymmetric distribution of the target variable, we chose to prioritize interpretability of the model and refrained from transforming the data so as to bring that distribution closer to normal. Given additional time, we would have iterated on the model further to improve predictions for expensive properties while still generating clearly interpretable insights.

---
