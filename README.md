#AutoPaperClassifier

## Document Intelligence: BERT-Powered PDF Classifier with FastAPI

This project demonstrates how to build a BERT-based document classification pipeline that processes research papers in PDF format and predicts their relevance to a specific category — such as whether a paper shares a dataset. It integrates Natural Language Processing with modern backend APIs to make the model accessible via a simple HTTP interface.

---

## 🔍 Use Case

Designed for scenarios where you want to:
- Automatically classify scientific papers or business documents.
- Identify papers that share open datasets for research aggregation.
- Build intelligent search pipelines over large collections of academic PDFs.

---

## 🧠 What’s Inside?

### 1. Transformer-based Text Classifier
- Uses `bert-base-uncased` from Hugging Face Transformers.
- Fine-tuned for binary/multiclass classification on parsed PDF text.

### 2. PDF Parsing and Preprocessing
- Extracts text from PDF files using `PyMuPDF` (via `fitz`).
- Prepares inputs compatible with BERT tokenization.

### 3. FastAPI Backend
- Exposes a `/predict/` endpoint for uploading PDF files.
- Returns the model’s prediction in a simple JSON response.

---

## 📁 Project Structure
├── api/
│ └── app.py # FastAPI app to serve the model
├── model/
│ ├── bert_classifier.py # Model architecture
│ └── inference.py # Load model & inference logic
├── saved_model/
│ ├── model.pt # Trained model weights
│ └── label_encoder.joblib # Fitted LabelEncoder
├── experiment_01_document_classifier.ipynb # Training + Evaluation
├── requirements.txt
└── README.md


## 🚀 Getting Started

### 1. Clone the repository
    ```bash
    git clone https://github.com/yourusername/document-intelligence-api.git
    cd document-intelligence-api


### 2. Set up virtual environment
    ```bash
    python -m venv ml-env
    source ml-env/bin/activate
    pip install -r requirements.txt
### 3. Run the FastAPI app
    ```bash
    uvicorn api.app:app --reload
    
## 🧩 Future Extensions
###Support multilingual models (e.g. xlm-roberta).

###Add PDF metadata + citation extraction.

###Train on larger corpora using scientific datasets like S2ORC.

###Deploy as a microservice in a cloud or containerized environment.

## 📄 License
This project is licensed under the MIT License.

## 💡 Inspiration
Originally built as part of an end-to-end GenAI workflow to explore intelligent document understanding using transformer models and scalable APIs.

Thankyou :)


