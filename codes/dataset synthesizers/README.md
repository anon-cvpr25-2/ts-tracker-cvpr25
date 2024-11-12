# Dataset synthesizers

The dataset synthesizers presented (file names like ..._DataGen.ipynb) in this folder are originally meant to be ran in the google colab environment
If running in google colab, be careful to allow the download of multiple files from browser, otherwise (likely) only the smaller test set will be automatically downloaded

The codes can be easily executed locally too via removing the rows starting with '!'and executing the bash commands manually, and via removing the colab-specific download block starting with 'from google.colab import files'

# LabelTransformation

This code performs a simple label format transformation from ID-masks to serial object polygons format so that the prediction are ground truth formats match
Perform this label transformation for all test set ground truth labels intended for comparation against predictions