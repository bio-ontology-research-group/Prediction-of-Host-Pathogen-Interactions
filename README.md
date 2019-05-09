# Prediction of Host Pathogen Interactions
The scripts to reproduce the analysis of the HPI prediction paper

## Notebooks
All notebooks should be run with Python3. 

### 1. Preprocessing
* preprocessing_pathogen.ipynb: From PathoPhenoDB, generates the input file for OPA2Vec.
* preprocessing_protein.ipynb: From HPO, MGI and GO, generates the input file for OPA2Vec (example is given for the intersection set of HP, MP and GO).
* preprocessing_HPIDB.ipynb: From HPIDB, generates hpidb2.score.txt by converting entrez IDs to UniProt IDs
hyperopt.

### 2. Hyperparameter optimization using hyperas 
* hyperopt.ipynb: Runs the hyperas library to tune hyperparameters.

### 3. Training, evaluation and prediction
* train.ipynb: Trains the prediction model by leave-one-taxon-out cross-validation and computing the performance. The input files need to be changed for each set of features.
* train&predict.ipynb: Trains and saves the model predictions to predictions.tsv.

### 4. Plotting the figures in the paper
* plots.ipynb: generates the TPR plots and the AUC-Epoch figures.

## Prediction results
* predictions_bacteria_intersection.tsv: predicted protein partners for 29 bacteria taxa based on the intersection feature for proteins and the taxonomic propogation

* predictions_virus_intersection.tsv: predicted protein partners for 96 virus taxa based on the intersection feature for proteins and the taxonomic propogation
