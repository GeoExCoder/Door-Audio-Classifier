# Door-Audio-Classifier
This repository contains an audio classification pipeline designed to identify door material types (wood, metal, and glass) from knock recordings. The project explores how machine learning and signal processing can support urban mining and building material reuse by enabling fast, low-cost identification of door types using only a smartphone microphone.

Dataset: 
~400 labeled audio clips of knocks collected via iPhone microphone.

Preprocessing: 
Audio segmentation, normalization, and feature extraction using Librosa

Features: 
Mel-Frequency Cepstral Coefficients (MFCCs), Delta-MFCCs, Spectral statistics (contrast, centroid, bandwidth, roll-off)

Modeling: 
Implemented with scikit-learn

Tested classifiers: 
Random Forest (final model), SVM, baseline logistic regression

Evaluation: 
GroupKFold cross-validation (ensuring clips from the same door don’t leak across train/test sets), Confusion matrix, PCA and t-SNE for feature selection 

Deployment-ready:
Model serialized with joblib for reproducibility and future integration.

Results:

Baseline (random guess): 
- 33.3% accuracy
  
Final SVM (most accurate) model: 
- 63.4% accuracy (update with your result)
  
Findings:
- Wood doors classified most accurately.
- Glass often misclassified as wood/metal due to framing materials producing hybrid acoustic signatures.
  
Results highlight both the promise and challenges of unimodal, audio-only material classification.

Applications:

- Sustainable deconstruction: Identify door materials quickly during building tear-downs.
- Urban mining: Support material reuse and recycling workflows.
- Low-cost sensing: Demonstrates how commodity devices (iPhone mic) can perform material classification.

Author:
Andrew Rothschild Averbach
Statistics Major, Washington University in St. Louis
Interests: Data Science, Business Analytics, Spatial Analysis, Sustainability
