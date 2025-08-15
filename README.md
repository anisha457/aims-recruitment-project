# aims-recruitment-project
# Visual Grounding Model for Phrase-to-Image Region Matching

## Description
This project implements a deep learning model to perform visual grounding, localizing image regions corresponding to descriptive phrases or sentences. The model is trained on the Flickr30k Entities dataset and includes data preparation, model training, inference, and visualization pipelines — fully implemented and tested in a Kaggle notebook.

---

## Setup Instructions

1. **Clone or download the project files**

2. **Set up Python environment**

   It is recommended to use a virtual environment:
   
python3 -m venv env
source env/bin/activate # On Windows use: env\Scripts\activate


3. **Install dependencies**

pip install -r requirements.txt


4. **Prepare Dataset**

- The project uses the Flickr30k Entities dataset.
- If using locally, download and extract the dataset.
- Organize images and XML annotations as expected by the code (refer to dataset folder structure).
- If running on Kaggle, attach the dataset via the "Add Input" button.

---

## Usage Instructions

### Run Training

python model_training.py


This script will:

- Load and preprocess the dataset.
- Build the visual grounding model.
- Train with balanced batches and weighted loss.
- Output training logs and evaluation metrics.

---

### Run Inference Demo

python inference.py --image_path <path_to_image> --query "<text query>"


- Returns the cropped region of the image matched by the query.

---

### Visualize Bounding Boxes

python visualization.py --image_path <path_to_image> --annotation_path <path_to_xml>


- Displays ground-truth bounding boxes for debugging and analysis.

---

## Project Structure

- `model_training.py` — Training pipeline
- `inference.py` — Perform phrase-to-region matching inference
- `visualization.py` — Functions for drawing bounding boxes on images
- `requirements.txt` — Python package dependencies
- `README.md` — This setup and usage guide

---

## Notes

- This code is extracted and adapted from Kaggle notebook version to standalone scripts.
- Ensure correct file paths and dataset formatting as per your environment.
- For Kaggle notebook users, export your notebook as a `.py` file to run locally or modify as needed.

---

## Contact

For questions or support, please refer to notebook comments or contact the author.


