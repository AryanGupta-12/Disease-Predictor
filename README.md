# Disease-Predictor

## Project Overview

Disease-Predictor is a Python-based web application built using Streamlit that predicts diseases based on user-selected symptoms. Its main purpose is to provide an interactive and educational tool for understanding possible diseases related to given symptoms. The application covers multiple diseases and provides detailed descriptions and recommended precautions for each predicted disease.

## Features

- Interactive symptom selection via multi-select dropdown
- Disease prediction using a pre-trained machine learning model
- Display of disease description and precautionary measures
- Simple, user-friendly web interface through Streamlit

## Tech Stack

- Python 3.x
- Streamlit for the front-end UI
- Libraries: scikit-learn, Keras, TensorFlow, NumPy, Pandas, Joblib, Matplotlib

## Installation / Setup

### Prerequisites
- Python 3.7 or higher
- Linux system dependencies:
  - freeglut3-dev
  - libgtk2.0-dev

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/AryanGupta-12/Disease-Predictor.git
   cd Disease-Predictor
   ```
2. Create and activate a Python virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. (Optional) Install system dependencies:
   ```bash
   sudo apt-get install freeglut3-dev libgtk2.0-dev
   ```

## Running the Application

Run the Streamlit app using:
```bash
streamlit run MLmodel.py
```
This command will start a local web server and open the application UI in your default browser.

## Usage Instructions

- Select symptoms from the multi-select dropdown (maximum 17 symptoms).
- Click the "Predict" button to receive the disease prediction.
- The app will display the predicted disease name, a detailed description, and recommended precautions.
- Use the information provided for educational purposes only.

## Configuration & Environment

- The app relies on data files located in the root directory:
  - `model.h5` (pre-trained model)
  - `scaler.pkl` (for data normalization)
  - `severity.csv` (symptom weights)
  - `symptom_Description.csv` (disease descriptions)
  - `symptom_precaution.csv` (recommended precautions)
- No additional configuration files or environment variables are required.

## Model Details

- The disease prediction model is a Keras deep learning model saved in `model.h5`.
- Input data consists of symptom weights scaled using `scaler.pkl` before prediction.
- The model outputs a predicted disease classification along with the probabilities.
- Training scripts are not included in this repository.

## Testing

- No automated tests are included with this project.

## Limitations & Disclaimer

This application is intended for educational and demonstration purposes only. It is not designed for clinical diagnosis or treatment. Always consult a healthcare professional for medical advice.

## Contribution & License

- No CONTRIBUTING.md file is present.
- No LICENSE file is currently included in the repository.
- Contributions can be made by opening issues or pull requests on the GitHub repository.

---

*Last updated: June 2026*