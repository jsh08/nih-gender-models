# nih-gender-models
Trains on female and male chest x ray images to find possible bias

NOTES======

dependencies: (install via pip)
  - numpy
  - matplotlib
  - pillow
  - pandas
  - scikit-image
  - scikit-learn
  - seaborn
  - jupyterlab
  - ipykernel

CSV files: there are 7 csv files, and each name should tell you which group is trained on and which is tested on -- nih_labels.csv corresponds to all diseases without gender separation

cxr_dataset.py (line 21) and model.py (line 218): change "nih_labels.csv" to name of file with subgroup you're analyzing (e.g., "nih_labels_master_mtrain_ftest")

retrain.py 
  - (line 11): change PATH_TO_IMAGES to the path of all uncompressed images
  - I personally used a google bucket to store all the images and then downloaded them to the directory folder raw_data, but if you're not using a bucket, then just change the         path to wherever you're storing them (if you're using a bucket like me, you need to generate key.json from the google service account)
  
run_training.ipynb:
  - ignore the first cell (this changes the directory to a folder that doesn't exist in this repository)
  - try to keep the number of cells reduced since more output slows down the notebook
  
  
