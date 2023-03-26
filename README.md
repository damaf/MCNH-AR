# MCNH-AR

## Markov Chain Non-Homogeneous Auto-Regressive (MCNH-AR)
This package contains the software programs designed for MCNH-AR model. It includes a learning algorithm, a prediction function and a state inference algorithm.

## Requirements
 * Numpy
 * Scipy
 * Pickle
 * Futures
 * Sklearn
 * Tick

## MCNH-AR model: context variables $\mathcal{C}_1$ 

### Launch model learning on anesthesia dataset
```{python}
python3 -O mcnh-ar-C1_training.py TRAIN_DATA_DIR NB_TIME_SERIES MODEL_OUTPUT_DIR Ar_order Nb_states  Nb_covariates
```

## MCNH-AR model: context variables $\mathcal{C}_2$ 

### Launch model learning on anesthesia dataset
```{python}
python3 -O mcnh-ar-C2_training.py TRAIN_DATA_DIR NB_TIME_SERIES MODEL_OUTPUT_DIR Ar_order Nb_states  Nb_covariates Features_file Minus_baseline
```
