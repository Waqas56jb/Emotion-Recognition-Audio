# 🎭 **Emotion Recognition from Speech**

Welcome to **Homework 3: Emotion Recognition**, where we explore the fascinating intersection of audio processing and machine learning to detect emotions from speech signals. This project focuses on extracting meaningful audio-based features, training a classification model, and performing error analysis to understand and improve the results.

---

## 🚀 **Project Overview**

Speech Emotion Recognition (SER) is the process of identifying emotions from speech using computational models. Emotional states like *anger, sadness, joy,* and *anxiety* influence acoustic features of speech, such as pitch and intensity. This project breaks down the workflow into three key phases:

1. **Feature Extraction**: Extract audio-based features like pitch and intensity using the `parselmouth` library (Praat interface).
2. **Model Training**: Train a **Support Vector Machine (SVM)** for emotion classification using extracted features.
3. **Error Analysis**: Analyze model performance using confusion matrices, precision-recall metrics, and class-specific errors.

---

## 🎯 **Objectives**

- Extract meaningful acoustic features (pitch, intensity) from audio files.
- Train a machine learning model to classify emotions accurately.
- Evaluate and analyze errors to suggest improvements for future work.

---

## 🛠 **Technologies Used**

| **Tool/Library**     | **Purpose**                                  |
|-----------------------|---------------------------------------------|
| Python               | Primary programming language                |
| Parselmouth (Praat)  | Audio feature extraction (pitch, intensity) |
| Scikit-learn         | Machine learning and evaluation metrics     |
| Matplotlib/Seaborn   | Visualization of results and error analysis |
| Pandas/Numpy         | Data processing and transformation          |

---

## 🧩 **Project Workflow**

1. **Feature Extraction**:
   - Extract *minimum, maximum, and mean* values for pitch and intensity.
   - Normalize features using Z-score normalization for better comparability.

2. **Classification**:
   - Train an **SVM classifier** with Leave-One-Speaker-Out (LOSO) cross-validation.
   - Evaluate model performance using metrics like accuracy, precision, recall, and F1-score.

3. **Error Analysis**:
   - Generate a **confusion matrix** to visualize misclassifications.
   - Identify class-specific issues (e.g., class imbalance, overlapping features).

---

## 📊 **Highlights**

- **Feature Insights**:
   - *Pitch*: Higher for emotions like *anger* and *happiness*; lower for *sadness* and *fear*.
   - *Intensity*: Reflects emotional intensity; *anger* has higher intensity compared to *sadness*.

- **Model Performance**:
   - Average accuracy: **~15-18%** (varies per emotion class).
   - Stronger performance for distinct emotions (*panic*); weaker for overlapping ones (*anxiety, cold-anger*).

- **Visualizations**:
   - Feature distributions for each emotion.
   - Confusion matrix to analyze prediction errors.

---

## 📈 **Future Improvements**

- Use advanced models like **Random Forests** or **Deep Learning** for improved performance.
- Address class imbalance by augmenting underrepresented classes.
- Explore additional features like **MFCCs**, **spectral roll-off**, or **formants**.

---

## 🖥 **Getting Started**

### Prerequisites:
- Python 3.8+
- Install required libraries using:
   ```bash
   pip install parselmouth pandas numpy scikit-learn matplotlib seaborn
   ```

### Running the Project:
1. Clone the repository:
   ```bash
   git clone https://github.com/username/emotion-recognition.git
   cd emotion-recognition
   ```
2. Place your audio files in the designated folder.
3. Run the feature extraction and model training script:
   ```bash
   python main.py
   ```

---

## 🎥 **Visual Results**

- **Feature Distributions**: Understanding pitch and intensity variations across emotions.
- **Confusion Matrix**: Visual breakdown of model predictions vs. true labels.

---

## 💡 **Conclusion**

This project demonstrates the potential of audio-based feature extraction for emotion recognition tasks. While the SVM classifier provides a strong foundation, future exploration with deep learning models can unlock further improvements.

---

<p align="center">⭐ **Feel free to explore, contribute, and enhance the project!** ⭐</p>
