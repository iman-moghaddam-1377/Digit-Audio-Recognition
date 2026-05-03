# 🎙️ Digit Audio Recognition (Attention-Based)

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-EE4C2C.svg)

## 📋 Project Overview
The objective is to classify spoken digits from a provided dataset. The architecture is inspired by the **Whisper** model, utilizing transformer-like components while strictly avoiding Recurrent Neural Networks (RNNs).

### Key Constraints:
*   **Architecture:** Must include **Attention** blocks and **Positional Encoding**.
*   **Exclusions:** No RNN, LSTM, or GRU blocks allowed.
*   **Inspiration:** Designs based on the [Whisper paper](https://arxiv.org/abs/2212.04356) or associated [GitHub repositories](https://github.com/openai/whisper).

---

## 🏗️ Model Architecture
The proposed model follows an encoder-only (or encoder-decoder) transformer structure adapted for audio spectrograms.

### Components:
1.  **Feature Extraction:** Conversion of raw audio to Mel-spectrograms.
2.  **Positional Encoding:** Added to retain temporal information of the audio sequence.
3.  **Multi-Head Attention:** To capture long-range dependencies within the audio signals.
4.  **Feed-Forward Layers:** For non-linear transformations.

---

## 🚀 Implementation & Tasks

### A) Model Design
Detailed block diagram and description of each component's functionality within the digit recognition pipeline.

### B) Evaluation
After training, the model's performance is analyzed using a **Confusion Matrix** to identify which digits are most frequently misclassified.

### C) Robustness Testing (Noise Analysis)
We evaluate the model's resilience by adding **White Noise** to the test set. 
*   **Metric:** Accuracy vs. SNR (Signal-to-Noise Ratio).
*   **Result:** A plot showing the degradation of accuracy as the noise level increases.

### D) Bonus: Noise Robustness Strategy
Implementation of a technique to improve performance in noisy environments (e.g., Data Augmentation, Spectral Subtraction, or specialized Denoising layers). 

---

### Accuracy vs. SNR Curve
![Accuracy vs SNR Plot](https://via.placeholder.com/600x300?text=Accuracy+vs+SNR+Plot+Placeholder)

---

