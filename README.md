# AIMI_ProjectGroup16_PANDA
## Testing Foundation Models for Digital Pathology on a Public Prostate Cancer Detection Challenge

This is the project on Prostate cANcer graDe Assessment (PANDA) Challenge done by group 16 for AIMI course.


This project consists of three main Jupyter notebooks:
1) phikon-Extract-Embd-Files.ipynb
2) training-file-phikon_.ipynb
3) offline-inference-trident-pipeline.ipynb

Follow these steps to use the notebooks:

###Installation:
Main libraries needed to run the files are Trident and Titan from the mahmoodlab. To run the inference file offline on kaggle, please download these libraries first and import them as datasets for the inference file.

------------------------------------------------------------
1) Extract Embeddings (phikon-Extract-Embd-Files.ipynb)

- Goal: Extract feature embeddings from your input data.
- Steps:
  - Open the notebook.
  - Run each cell in sequence to process your input data.
  - This will generate .pt files (feature files) and save them in the output directory.

- Note: If you’re doing it on Kaggle, the output is typically saved in:
  kaggle/working

------------------------------------------------------------
2) Download the Saved Feature Files

- After running the extraction notebook, download the generated .pt files from kaggle/working as a dataset, and use this dataset as the input for training file.

------------------------------------------------------------
3) Train the Model (training-file-phikon_.ipynb)

- Goal: Train the model on the extracted embeddings.
- Steps:
  - Open the notebook.
  - Set the path to the downloaded .pt feature files as input.
  - Run all cells to train the model.
- Output: The trained model weights (.ckpt or .pt file) will be saved in kaggle/working (if on Kaggle).

------------------------------------------------------------
4) Use the Trained Model for Inference (offline-inference-trident-pipeline.ipynb)

- Goal: Run inference on new data using the trained model weights.
- Steps:
  - Open the notebook.
  - Set the path to the trained model weights you downloaded from training.
  - Load the model and run inference on new data.

------------------------------------------------------------
Summary of Workflow

1) Extract embeddings using phikon-Extract-Embd-Files.ipynb
2) Download the generated feature files (.pt) from kaggle/working
3) Train the model in training-file-phikon_.ipynb
4) Download the trained model weights from kaggle/working
5) Run inference using offline-inference-trident-pipeline.ipynb with the downloaded weights

------------------------------------------------------------
Notes:

- If running on Kaggle, the notebooks save intermediate files and final outputs in:
  kaggle/working
- You can download your output files from kaggle/working after execution.
