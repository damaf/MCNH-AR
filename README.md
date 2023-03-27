# MCNH-AR

## Markov Chain Non-Homogeneous Auto-Regressive (MCNH-AR)
This package contains the software programs designed for MCNH-AR model. It includes a learning algorithm, a prediction function and a state inference algorithm.

## Requirements
 * Python 3.6
 * Numpy
 * Scipy
 * Scikit-learn
 * Pickle5
 * Futures
 * Numba 0.45
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

## Definition of parameters

  * train_data_dir: "anesthesia_data" directory
  * nb_time_series: the number of training instances (between 1 and 100)
  * model_output_dir: the name of the directory in which model output is saved within a serialized file
  * ar_order: the order of the auto-regressive process (>= 0)
  * nb_states: the number of states to be considered (>= 2)
  * features_file: the file that contains the context variable $\mathcal{C}_2$ extracted based on Hawkes process (to load from directory "Point-process-models/tick-Hawkes-process/model_outputs/expKernel/5-event-types")
