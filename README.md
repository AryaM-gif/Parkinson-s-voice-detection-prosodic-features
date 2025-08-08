# Parkinson-s-voice-detection-prosodic-features
ML-based detection of Parkinson's Disease using prosodic features from voice recordings (pitch, energy, jitter, shimmer, etc.)
# Parkinson's Voice Detection using Prosodic Features

This project aims to detect Parkinson's Disease (PwPD) using voice recordings, primarily focusing on prosodic features like pitch, energy, jitter, shimmer, etc.

## 🚀 Project Workflow

1. **Data Loading & Validation**
2. **Audio Preprocessing** (resampling, pre-emphasis, silence removal)
3. **Feature Extraction**
   - Global: pitch range, energy mean/std, jitter, shimmer
   - Frame-wise pitch using librosa
4. **Exploratory Data Analysis (EDA)**
   - Histograms, box plots, KDEs, statistical testing
5. **Modeling Approaches**
   - HMM + MLP
   - GMM + MLP
   - RNN (LSTM-based)
6. **Evaluation**
   - Accuracy, F1-score, Confusion matrix, ROC-AUC
7. **Prediction on New Audio**

## 📂 Folder Structure

