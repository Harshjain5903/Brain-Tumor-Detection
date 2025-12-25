# Brain-Tumor-Detection

## Project Overview

Brain-Tumor-Detection is a deep learning-based web application for detecting and classifying brain tumors from MRI images. The project leverages transfer learning using the VGG16 model and provides a user-friendly interface for uploading MRI images and receiving predictions about tumor presence and type.

## Features
- **Deep Learning Model:** Utilizes VGG16 for transfer learning to classify MRI images into four categories: pituitary, glioma, meningioma, and no tumor.
- **Web Interface:** Built with Flask, allowing users to upload MRI images and view predictions and confidence scores.
- **Visualization:** Includes data visualization and model performance plots in the provided Jupyter notebook.
- **End-to-End Pipeline:** From data preprocessing and augmentation to model training, evaluation, and deployment.

## Project Structure
```
Brain Tumor Detection/
├── main.py                  # Flask web application
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation
├── models/
│   ├── brain_tumour_detection_using_deep_learning.ipynb  # Jupyter notebook for model development
│   └── model.h5            # Trained Keras model
├── sample MRI Images/       # Example MRI images
├── templates/
│   └── index.html           # HTML template for Flask app
├── uploads/                 # Uploaded images (runtime)
├── venv*/                   # Python virtual environments (not needed for deployment)
```

## How It Works
1. **Model Training:**
   - The Jupyter notebook (`models/brain_tumour_detection_using_deep_learning.ipynb`) contains all steps for data loading, preprocessing, augmentation, model building (using VGG16), training, evaluation, and saving the trained model as `model.h5`.
2. **Web Application:**
   - The Flask app (`main.py`) loads the trained model and provides a web interface for users to upload MRI images and receive predictions.

## Setup Instructions

### 1. Clone the Repository
```sh
git clone https://github.com/<your-username>/Brain-Tumor-Detection.git
cd Brain-Tumor-Detection
```

### 2. Create and Activate a Virtual Environment (Recommended)
```sh
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```sh
pip install -r requirements.txt
```

### 4. Download or Train the Model
- If you have a pre-trained `model.h5`, place it in the `models/` directory.
- To train your own model, open and run the notebook at `models/brain_tumour_detection_using_deep_learning.ipynb` (requires dataset in the correct structure).

### 5. Run the Flask Web Application
```sh
python main.py
```
- The app will be available at `http://127.0.0.1:5000/`.

### 6. Using the Web App
- Open the web page in your browser.
- Upload an MRI image (JPG/PNG).
- View the prediction and confidence score.

## Notes
- The `uploads/` folder is used to store images uploaded via the web interface.
- The `sample MRI Images/` folder contains example images for testing.
- The virtual environment folders (`venv311/`, `venv38/`, and any `venv*/`) are not required for deployment and should not be committed to version control. These are now excluded via `.gitignore`.
- The `models/model.h5` file (large model file) is also excluded from version control for repository cleanliness. Place your trained model here manually if needed.

## Requirements
- Python 3.8+
- See `requirements.txt` for all Python dependencies (TensorFlow, Flask, etc.)

## Credits
- Model architecture and training pipeline based on VGG16 and Keras.
- Web interface built with Flask and Bootstrap.

## License
This project is for educational and research purposes only. Please check the repository for license details.