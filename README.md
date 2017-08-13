# ml-performance
This repo contains MATLAB code to measure performance of machine learning classifiers.

**calibrate.m** - this is the main file to run.

```
  perf = calibrate(actual,predicted,trueClass,Nbins) 
 
  Returns performance metrics of your model.
 
    actual    : Ground Truth (binary class labels, 1 or 0)
    predicted : Model predictions
    trueClass : Label for Class of Interest (1 or 0)
    Nbins     : Number of bins to use for HL-test
```

**calibrate.m** calls **HosmerLemeshowTest.m** [1,2] and **InterX.m** [3].

## Classification Metrics

This file performs the following calculations for a binary prediction problem:
- **AUC** (Area Under the Receiver Operating Curve).
- **OPT_ER**: Optimum Point on the ROC.
- **EER** (Equal Error Rate): Operating point on ROC for equal True Positive Rate and False Positive Rate.
- **Accuracy**: Correct classification, when the probability threshold is set to 0.5 for classification between binary classes
- **TP** (True Positive): Number of observations in positive class (i.e. class of interest) correctly as positive class.
- **FP** (False Positive): Number of observations in negative class wrongly predicted as positive.
- **TN** (True Negative): Number of observations in negative class correctly predicted as negative.
- **FN** (False Negative): Number of observations in negative class wrongly predicted as negative.
- **FPR** (False Positive Rate): Out of all the negative observations, the percentage of which were wrongly predicted positive.
- **TPR** (True Positive Rate) : Out of all the positive observations, the percentage of which were correctly predicted positive.
- **Recall**   : (Same as True Positive Rate).
- **Precision**: Out of all positive predictions, the the percentage of which were correctly predicted positive.
- **F1_score** : The harmonic mean of Precision and Recall.
- **TPR_when_FPR0p10** : True Positive Rate at 10% False Positive Rate.
- **TPR_when_FPR0p05** : True Positive Rate at 5% False Positive Rate.
- **TPR_when_FPR0** : True Positive Rate at 0% False Positive Rate.
- **FPR_when_TPR0p90** : False Positive Rate at 90% True Positive Rate.
- **FPR_when_TPR0p95** : False Positive Rate at 95% True Positive Rate.
- **FPR_when_TPR1p00** : False Positive Rate at 100% True Positive Rate.
- **HL_test** (Hosmer-Lemeshow Test) : evaluates goodness-of-fit of model, i.e. if the model predicts 10% probability of a positive class for an observation, is the model correctly predicting the positive class 10% of the time? 


Worked on MATLAB 2017a.


## References

[1] Peng, Chao-Ying Joanne, Kuk Lida Lee, and Gary M. Ingersoll. "An introduction to logistic regression analysis and reporting." The journal of educational research 96.1 (2002): 3-14.

[2] http://www.nyu.edu/projects/farbood/projects/stats.html

[3] https://www.mathworks.com/matlabcentral/fileexchange/22441-curve-intersections?focused=5165138&tab=function

