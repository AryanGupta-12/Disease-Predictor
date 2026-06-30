# Disease Predictor

A web application using machine learning to predict diseases based on selected symptoms. Built using Streamlit, this app provides descriptions and precautions for predicted diseases.

---

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Model & Data Details](#model--data-details)
- [Configuration](#configuration)
- [Testing](#testing)
- [Screenshots / Demo](#screenshots--demo)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Features

- Predicts diseases based on user-selected symptoms.
- Provides detailed disease descriptions.
- Lists recommended precautions for each disease.
- Interactive web UI powered by Streamlit.

## Tech Stack

- Python 3.x
- Streamlit
- scikit-learn
- Keras & TensorFlow
- Pandas & NumPy
- Joblib

## Project Structure

- `MLmodel.py`: Main Streamlit app script.
- `model.h5`: Serialized machine learning model.
- `scaler.pkl`: Preprocessing scaler model.
- `X.npy`: Dataset features.
- `symptom_Description.csv`: Disease descriptions.
- `symptom_precaution.csv`: Disease-specific precautions.
- `severity.csv`: Symptoms with weights.
- `requirements.txt`: Python dependencies.
- `packages.txt`: OS dependencies.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AryanGupta-12/Disease-Predictor.git
   cd Disease-Predictor
   ```
2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Install OS-level dependencies (on Debian/Ubuntu):
   ```bash
   sudo apt-get install freeglut3-dev libgtk2.0-dev
   ```

## Usage

1. Run the Streamlit app:
   ```bash
   streamlit run MLmodel.py
   ```
2. Open your browser and go to:
   `http://localhost:8501`
3. Select up to 17 symptoms from the multi-select box.
4. Click **Predict** to see the predicted disease along with its description and recommended precautions.

## Model & Data Details

- The app uses a machine learning classification model saved as `model.h5`.
- Input features are weighted symptoms scaled by a pre-trained scaler `scaler.pkl`.
- Disease descriptions and precautions are loaded from CSV files.
- The model and data are included in the repository.
- This app is for educational and informational purposes only and not intended for medical diagnosis.

## Configuration

- No additional configuration or environment variables are required.
- All data files and models are local.

## Testing

- No automated tests are included in this repository.

## Screenshots / Demo

*(Add screenshots here if available)*

## Contributing

- Fork the repository.
- Create a feature branch: `git checkout -b fix/kan11`.
- Commit your changes with meaningful messages.
- Push your branch and create a pull request.

## License

*(Add license information here if available)*

## Contact

- Maintainer: Aryan Gupta
- GitHub: [https://github.com/AryanGupta-12](https://github.com/AryanGupta-12)
