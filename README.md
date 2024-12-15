Here’s a sample README file for project:

Voice Emotion Recognition Project
This project uses speech features such as pitch and intensity to recognize emotions in speech, leveraging machine learning techniques. It processes audio files, extracts relevant features, normalizes them, performs emotion classification using a Random Forest Classifier, and evaluates the performance using metrics like accuracy and F1 score.

Table of Contents
Libraries and Prerequisites
File Structure
Setup Instructions
Features Extraction
Model Training and Evaluation
Visualization
Results
Libraries and Prerequisites
Before running the project, ensure you have the following Python libraries installed:

Required Libraries
parselmouth: A Python interface to the Praat library for speech processing.
numpy: Used for numerical computations.
pandas: For handling and processing data.
sklearn: For machine learning algorithms (Random Forest) and preprocessing (StandardScaler).
matplotlib: For plotting visualizations.
seaborn: For creating enhanced data visualizations.
Installation
Install the required libraries using pip:

bash
Copy code
pip install parselmouth numpy pandas scikit-learn matplotlib seaborn
Additional Software
Praat: The project uses Praat's functionality via the parselmouth library to extract pitch and intensity features from the audio files. Ensure you have the Praat software installed on your system.
File Structure
The file structure is as follows:

bash
Copy code
/project_root
├── /hw3_speech_files
│ ├── audio_files.wav # Audio files for feature extraction
├── /visualization
│ ├── feature_plot.png # Saved feature plots
├── normalized_features.csv # Processed and normalized features
├── classification_results.txt # Saved results of classification
├── Feature.ipynb and Classification.ipynb # Main script for feature extraction and classification
└── README.md # This README file
Setup Instructions
Download the Speech Files:

Make sure the audio files you wish to use for the project are placed in the hw3_speech_files directory.
Create the Visualization Directory:

The project will automatically create a directory named visualization to store the feature plots.
Run the Project:

Execute the Feature.ipynb script to process the audio files, extract features, normalize them, and train the Random Forest Classifier.
bash
Copy code
Features.ipynb Extraction features
The project extracts the following features from each audio file:

Pitch:
Minimum pitch
Maximum pitch
Mean pitch
Intensity:
Minimum intensity
Maximum intensity
Mean intensity
The features are extracted using the parselmouth library, which interacts with Praat's pitch and intensity extraction functions.

Model Training and Evaluation
Normalization
The extracted features are normalized using Z-score normalization by speaker, ensuring that the model training is not biased by speaker-specific variations in pitch and intensity.

Classification
A Random Forest Classifier is used to classify emotions based on the extracted features. The classification experiment is performed using Leave-One-Speaker-Out cross-validation to evaluate the model's performance on unseen speakers.

Evaluation Metrics
The model's performance is evaluated using the following metrics:

Accuracy: The percentage of correct predictions.
Weighted F1 Score: The F1 score weighted by the number of instances per class.
Confusion Matrix: Visual representation of classification results.
Visualization
The project generates visualizations of the extracted features for each emotion. These visualizations are saved in the visualization directory.

The following plots are generated:

Feature Plot: Displays the features (pitch and intensity) for each emotion.
You can view and modify these plots in the visualization folder.

Results
The classification results, including accuracy and weighted F1 score, are saved to a text file (classification_results.txt). The confusion matrix for the best-performing speaker is also displayed.

Conclusion
This project provides a complete workflow for emotion recognition from speech using machine learning, from feature extraction to model evaluation and visualization. The results can be further analyzed or used for improving emotion recognition systems.
