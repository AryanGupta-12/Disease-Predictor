# Disease Predictor
A web-based machine learning application built with Streamlit to predict diseases based on input symptoms.

## Features
- Symptom-based disease prediction
- Displays disease description and recommended precautions
- Supports selection of up to 17 symptoms

## Tech Stack and Architecture
- Python 3.x
- Streamlit for interactive UI
- TensorFlow/Keras model loaded with joblib
- Pandas and NumPy for data handling and processing
- Pre-trained machine learning model usage (no training required)

## Installation
1. Clone the repository
2. Create a virtual environment and activate it:

```bash
python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
```

3. Install required Python packages:

```bash
pip install -r requirements.txt
```

4. Install OS-level dependencies listed in `packages.txt` (for Debian/Ubuntu):

```bash
sudo apt-get install $(cat packages.txt)
```

## Configuration
Ensure the following files are present in the project root directory:
- `model.h5` (pre-trained model file)
- `scaler.pkl` (scaler for input normalization)
- `X.npy` (input data file)
- CSV files: `severity.csv`, `symptom_Description.csv`, `symptom_precaution.csv`

No additional environment variables are required.

## Usage
### Running the App

Run the Streamlit app with:

```bash
streamlit run MLmodel.py
```

The app will be available at [http://localhost:8501](http://localhost:8501).

### How to Use
- Select symptoms from the multi-select list (maximum 17).
- Click the **Predict** button.
- The app will display the predicted disease name, a description, and suggested precautions.

## Model and Disease Prediction Details
- Supported diseases correspond to entries in `symptom_Description.csv`.
- Inputs are symptom severity weights from `severity.csv`.
- Maximum 17 symptoms can be selected as input features.
- The model predicts the disease and provides prediction confidence.

## Data Files Description
- `symptom_Description.csv`: Contains descriptions of diseases.
- `severity.csv`: Lists symptoms along with their severity weights.
- `symptom_precaution.csv`: Provides recommended precautions for each disease.
- `model.h5`: Pre-trained ML model file.
- `scaler.pkl`: Input scaler used for feature normalization.
- `X.npy`: Numpy array of training data inputs.

## Project Structure
- `MLmodel.py`: Main Streamlit application file.
- `requirements.txt`: Python dependencies.
- `packages.txt`: OS-level dependencies.
- Various CSV and model files supporting the application.

## Testing
No automated tests are included in this repository. Testing is manual by running the app and validating predictions.

## Deployment
This is a Streamlit application suitable for deployment on Streamlit Cloud or any server supporting Python and Streamlit.

## Contributing
Contributions are welcome. Please open an issue or pull request for improvements.

## License
_(Add license information here if applicable)_

## Contact
Maintainer: Aryan Gupta
Email: gargaryan81@gmail.com

---

*This README was generated to document the Disease Predictor application.*
