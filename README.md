# Gesture Language Translator - Alphabets

This project is a **Gesture Language Translator** that recognizes **American Sign Language (ASL) alphabets** using deep learning.  
It allows training, evaluation, and prediction of hand gesture images representing alphabets.

---

## Project Structure

Gesture Language Translator - Alphabet/
│── asl_model.h5              # Pre-trained model
│── class_labels.json         # Mapping of class indices to alphabet labels
│── config.py                 # Configuration settings (paths, parameters)
│── data_loader.py            # Data loading and preprocessing utilities
│── evaluate.py               # Model evaluation script
│── model.py                  # Model architecture definition
│── predict.py                # Run predictions on test images
│── train.py                  # Train the model
│── asl_alphabet_test/        # Sample test images
│    ├── A_test.jpg
│    ├── B_test.jpg
│    ├── ... (rest of alphabets, plus `space` and `nothing`)
|── asl_alphabet_train/       # sample train images
|    ├── A
|         ├── A1.jpg, A2.jpg, ...
|    ├──  B
|         ├── B1.jpg, B2.jpg, ...
|    ├──  c
|         ├── ...(rest of alphabets, plus `space` and `nothing`)

---

## Features

- Recognizes **ASL alphabets** from hand gesture images.
- Includes a **pre-trained model** (`asl_model.h5`) for quick testing.
- Scripts for:
  - **Training** a custom model.
  - **Evaluating** model performance.
  - **Predicting** gestures on test images.
- Configurable settings via `config.py`.

---

## Installation

1. Clone this repository or extract the ZIP.  
2. Download the pre-trained model [`asl_model.h5`](https://drive.google.com/file/d/1GpHC9BSq9g7qIDXa6EsAf0gJ-I8kGow1/view?usp=drivesdk) and place it in the project root folder.  
3. Install dependencies:
   ```bash
    pip install -r requirements.txt
   
---

## Training the Model

To train the model from scratch:

    python train.py

This will:

- Load dataset paths from config.py
- Build the model from model.py
- Save the trained model as asl_model.h5

---

## Evaluating the Model

To evaluate the trained model:

    python evaluate.py

This outputs:

- Accuracy & loss
- Classification metrics
- Confusion matrix

---

## Predicting Gestures

Run predictions on sample images:

    python predict.py --image asl_alphabet_test/A_test.jpg

Example output:

    Predicted: A
    Confidence: 98.7%

---

## Configuration

Modify training/testing parameters in config.py:

- Dataset paths
- Batch size
- Learning rate
- Epochs

---

## Future Enhancements

- Real-time gesture recognition using webcam.
- Extend to word-level translation.
- Improve robustness with larger datasets.

---

## Author

Developed by Vishnu Prasad A, BE. ECE

For learning, research, and assistive technology development.

---
