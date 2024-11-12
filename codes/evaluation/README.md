# Evaluation

This folder contains the evaluation pipeline for the results presented in the paper

Before running these codes, predictions must be done and saliency map statistics must be calculated using codes:
/training and prediction/BatchPredictor.ipynb
/training and prediction/SaliencyMaps.ipynb
Both of which requires trained models using:
/training and prediction/InstSegTrain.ipynb
/training and prediction/LocalTrackingTrain.ipynb

And the whole MOTS pipeline must be executed for those results (with trivial code modifications, these can be excluded) as described in:
/mots training and prediction/README.md

Then the three codes should be executed in order:
- MetricsDataprep (combines all imported ground truth values and prediction results into a singular table)
- Metrics (calculated the metrics for the values present in the combined table)
- Analytics (generates figures and other statistics based on the calculated metrics, and imported saliency map results)

These codes use our old naming convention for the synthetic datasets, for successful execution be careful to rename the files and folders appropriately:

OLD, NEW
ArrowSynth1, SyntheticArrows
ArrowSynthShapes, SyntheticAmoeboids
ArrowSynthTurns, SyntheticArrowsTR1
ArrowSynthTurnsOften, SyntheticArrowsTR2
ArrowSynthShapesTP20, SyntheticAmoeboidsRP20 (or in the paper RP-1/20)
ArrowSynthShapesTP5, SyntheticAmoeboidsRP5 (or in the paper RP-1/5)

The codes presented in this folder are originally meant to be ran in the google colab environment, for local runs, make sure to execute the bash commands starting with '!' manually