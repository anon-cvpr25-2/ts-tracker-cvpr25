# MOTS codes

These codes present the full data preparation, training and prediction pipeline for MOTSynthCVPR22 and MOTS datasets
The codes follow a similar style and order as the ones presented in /training and prediction/, however they are more challenging
Thus we strongly recommend getting familiar with those codes first

# Data preparation
MOTS format is not compatible with our environment and the recordings are too high resolution for reasonable training, thus a reformatting and rescaling must be done
The codes must be ran in order (first two can be executed in parallel):
- MOTSynthCVPR22_AnnotPrep_SmallRes_Comittable.ipynb
- MOTSynthCVPR22_VideoPrep_SmallRes_Comittable.ipynb
- MOTSynthCVPR22_AnnotPrep_TrackingFramewise_SmallRes_Comittable.ipynb

# Training
Then trainings can be performed using:
- MOTSynthCVPR22_InstSegTrain_Comittable.ipynb
- MOTSynthCVPR22_InstSegTrain_Comittable.ipynb
In our (reasonable but not too strong) environment these codes ran for multiple weeks, so expect lengthy trainings ...

# Predictions
- MOTSynthCVPR22_RefactoredPredictorTest.ipynb: Performs prediction for a single evaluation sample from the MOTSynthCVPR22 dataset properely transformed (only serves testing purposes)
- MOTS_Predictor.ipynb: Performs prediction for the MOTS dataset full HD train samples