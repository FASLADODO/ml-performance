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

- AUC (Area Under the Receiver Operating Curve)
- Accuracy
- 


Worked on MATLAB 2017a.
