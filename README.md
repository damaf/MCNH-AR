# NHMC-AR model 

## Non-Homogeneous Markov Chain  Auto-Regressive (NHMC-AR) model

This package contains the software programs designed for the NHMC-AR model. It includes a learning algorithm, a prediction function and a state inference algorithm.

This package has been implemented by Fatoumata Dama, PhD student (2019-2022), Nantes University, France.

Fatoumata Dama was supported by a PhD scholarship granted by the French Ministery for Higher Education, Research and Innovation. She worked under the supervision of Christine Sinoquet, Associate Professor, PhD supervisor, LS2N / UMR CNRS 6004 (Digital Science Institute of Nantes), Nantes University, France.

## Requirements
 * Python 3.6
 * Numpy
 * Scipy
 * Scikit-learn
 * Pickle5
 * Futures
 * Numba 0.45
 * Tick

## Anesthesia data
FC : heart frequency (HF)

PAS : systolic blood pressure (SBP)

PAM : average blood pressure (ABP)

PAD : diastolic  blood pressure (DBP)

## NHMC-AR model: contextual variables extracted using the Hawkes point process framework - Application to anesthesia data

### Launch model learning on anesthesia dataset
```{python}
python3 -O mcnh-ar_training.py train_data_dir nb_time_series model_output_dir ar_order nb_states features_file
```

## Definition of parameters

  * train_data_dir: "anesthesia_data" directory
  * nb_time_series: the number of training instances (between 1 and 500)
  * model_output_dir: the name of the directory in which model output is saved within a serialized file
  * ar_order: the order of the auto-regressive process (>= 0)
  * nb_states: the number of states to be considered (>= 2)
  * features_file: the file that contains the contextual variables extracted based on Hawkes process (to load from directory "Point-process-models/tick-Hawkes-process/model_outputs/expKernel/5-event-types")
