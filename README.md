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
- **AUC** (Area Under the Receiver Operating Curve)
- **OPT_ER**: Optimum Point on the ROC.
- **EER** (Equal Error Rate): Operating point on ROC for equal True Positive Rate and False Positive Rate.
- **Accuracy**: Correct classification, when the probability threshold is set to 0.5 for classification between binary classes
- **TP** (True Positive): Number of observations in positive class (i.e. class of interest) correctly as positive class.
- **FP** (False Positive): Number of observations in negative class wrongly predicted as positive.
- **TN** (True Negative): Number of observations in negative class correctly predicted as negative.
- **FN** (False Negative): Number of observations in negative class wrongly predicted as negative.
- **FPR** (False Positive Rate): 
- **TPR** (True Positive Rate)
- **Recall**: 
- **Precision**: 
- **F1_score**: 
- **TPR_when_FPR0p10**
- **TPR_when_FPR0p05**
- **TPR_when_FPR0**
- **FPR_when_TPR0p90**
- **FPR_when_TPR0p95**
- **FPR_when_TPR1p00**
- **HL_test** (Hosmer-Lemeshow Test) : evaluates goodness-of-fit of model, i.e. if the model predicts 10% probability of a positive class for an observation, is the model correctly predicting the positive class 10% of the time? 


Worked on MATLAB 2017a.


## References

[1] Peng, Chao-Ying Joanne, Kuk Lida Lee, and Gary M. Ingersoll. "An introduction to logistic regression analysis and reporting." The journal of educational research 96.1 (2002): 3-14.
[2] http://www.nyu.edu/projects/farbood/projects/stats.html
[3] https://www.mathworks.com/matlabcentral/fileexchange/22441-curve-intersections?focused=5165138&tab=function

