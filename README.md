# Plant Disease Detection

CNN-based plant leaf disease classification (Tomato Bacterial Spot, Potato Early Blight, Corn Common Rust). Streamlit app + Docker.

## Structure

```
Plant-Disease-Detection/
├── app/
│   ├── main_app.py              # Streamlit app
│   ├── plant_disease_model.h5   # Pre-trained model (256×256)
│   ├── Plant_Disease_Detection.ipynb   # Training notebook
│   └── test_images/             # Sample leaf images
├── requirements.txt
├── Dockerfile
├── .gitignore
└── README.md
```

## Run locally

From repo root:

```bash
pip install -r requirements.txt
streamlit run app/main_app.py
```

Open http://localhost:8501

## Docker

From root Directory:

```bash
docker build -t plant-disease-detection:latest .
docker run -p 8501:8501 plant-disease-detection:latest
```
