# Plant Disease Detection

A CNN-based ML project for classifying plant leaf diseases (Tomato Bacterial Spot, Potato Early Blight, Corn Common Rust). Includes a Streamlit web app and Docker support.

---

## Project Structure

```
Plant-Disease-Detection/
├── main_app.py              # Streamlit web application
├── plant_disease_model.h5   # Pre-trained Keras model (256×256 input)
├── Plant_Disease_Detection.ipynb  # Notebook: data prep + training
├── requirements.txt
├── Dockerfile
├── Test Image/              # Sample leaf images
└── README.md
```

---

## Quick Start (Local)

### Prerequisites

- Python 3.9+
- pip

### Run locally

```bash
git clone <your-repo-url>
cd Plant-Disease-Detection

python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate

pip install -r requirements.txt
streamlit run main_app.py
```

Open **http://localhost:8501**, upload a leaf image, and get a prediction.

---

## Docker

### Build and run with Docker

```bash
# Build image
docker build -t plant-disease-detection:latest .

# Run container (port 8501)
docker run -p 8501:8501 plant-disease-detection:latest
```

---

## Model & Training

- **Input**: RGB image, resized to **256×256**.
- **Output**: One of:
  - `Corn-Common_rust`
  - `Potato-Early_blight`
  - `Tomato-Bacterial_spot`
- **Training**: See `Plant_Disease_Detection.ipynb` for data loading, CNN definition, training, and saving `plant_disease_model.h5`.

---

## Requirements

- **Python**: 3.9+
- **Key packages**: TensorFlow/Keras, Streamlit, OpenCV, NumPy (see `requirements.txt`).

---

## License

Use and modify as needed for your project.
