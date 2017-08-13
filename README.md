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

This file performs the following calculations for a binary prediction problem:
- AUC (Area Under the Receiver Operating Curve)
- OPT_ER
- EER
- Accuracy
- TP
- FP
- TN
- FN
- FPR
- TPR
- Recall
- Precision
- F1_score
- TPR_when_FPR0p10
- TPR_when_FPR0p05
- TPR_when_FPR0
- FPR_when_TPR0p90
- FPR_when_TPR0p95
- FPR_when_TPR1p00
- HL_test (Hosmer-Lemeshow Test) : evaluates how well calibrated the model is.

Worked on MATLAB 2017a.
