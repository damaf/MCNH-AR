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
python3 -O mcnh-ar-C1_training.py train_data_dir nb_time_series model_output_dir ar_order nb_states
```

## MCNH-AR model: context variables $\mathcal{C}_2$ 

### Launch model learning on anesthesia dataset
```{python}
python3 -O mcnh-ar-C2_training.py train_data_dir nb_time_series model_output_dir ar_order nb_states features_file
```
