# Collaborative Imputation for Multivariate Time Series with Convergence Guarantee


## File Structure

* Code: source code of our implementation
* Data: source files of datasets used in experiments
* appendix.pdf: the complete proofs for all the theoretical results in the manuscript, including Propositions 1,2,3,4,6 and 7, Lemma 5.

## Demo Script Running
```
python main.py --dataset AirQualityUCI ---iter 0 --missing_percent 0.1  --impute_model HUGE --missing_column 0 1 2 3 4 5 6 7 8 9 10 11 12 --used_regression_index 0 1 2 3 4 5 6 7 8 9 10 11 12 --impute_learning_rate 1e-2 --impute_reg_learning_rate 1e-2 --impute_skip_training 1e-4 --impute_learning_epoch 30 --init ARIMA
```

```
python main.py --dataset energy ---iter 0 --missing_percent 0.1  --impute_model HUGE --missing_column 0 1 2 3 4 5 6 7 8 --used_regression_index 0 1 2 3 4 5 6 7 8 --impute_learning_rate 1e-2 --impute_reg_learning_rate 5e-4 --impute_skip_training 1e-7 --impute_learning_epoch 50 --init EWMA
```

## Running a Dataset for All Cases:
```
# change the parameters in config.py
# change the python path and file path in exp_script.py
# runnning the script
python exp_script.py
```

## Dataset Source
* AirQuality: https://archive.ics.uci.edu/ml/datasets/Air+Quality
* Energy: https://archive.ics.uci.edu/ml/datasets/Appliances%20energy%20prediction
* Ethanol: http://www.timeseriesclassification.com/description.php?Dataset=EthanolConcentration
* Location: GPS time series dataset collected by us 
