```markdown
# General Health Query Chatbot

An AI-powered chatbot designed to answer general health-related queries based on a medical Q&A dataset. This project leverages advanced Natural Language Processing (NLP) techniques and pre-trained models like Bio_ClinicalBERT to provide accurate and context-aware responses.

---

## 🚀 Features
- **Symptom Checker**: Answers questions about symptoms and possible conditions.
- **Disease Information**: Provides information about diseases and their treatments.
- **Medication Guidance**: Offers general advice on medications.
- **Mental Health Support**: Responds to queries related to mental health.
- **Secure API Deployment**: Deployed via Flask with ngrok for testing.

---

## 📖 Table of Contents
1. [Motivation](#motivation)
2. [Technologies Used](#technologies-used)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Project Structure](#project-structure)
6. [Contributing](#contributing)
7. [License](#license)

---

## 💡 Motivation
The chatbot addresses the growing need for accessible, reliable, and instant health information. It aims to assist users in understanding their health concerns while emphasizing that it does not replace professional medical advice.

---

## 🛠️ Technologies Used
- **Python**: Core programming language.
- **Hugging Face Transformers**: For Bio_ClinicalBERT model integration.
- **Flask**: Backend framework for API deployment.
- **PyTorch**: For model training and fine-tuning.
- **ngrok**: To expose the local server for testing.

---

## 🖥️ Installation

### Prerequisites
1. Python 3.8 or above
2. Google Colab (optional, but recommended for training)
3. Hugging Face account (for tokenized access to models)

### Steps
1. Clone the repository:
   ```
   git clone https://github.com/yourusername/health-query-chatbot.git
   cd health-query-chatbot
   ```
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. Set up Hugging Face access:
   ```
   from huggingface_hub import login
   login(token="YOUR_HUGGINGFACE_TOKEN")
   ```

4. Run the Flask app:
   ```
   python app.py
   ```

5. Start ngrok (for testing):
   ```
   ngrok http 5000
   ```

---

## 📚 Usage

### Interacting with the Chatbot via API
1. Start the Flask app (as shown in Installation).
2. Use the `ngrok` public URL to send POST requests:
   ```
   curl -X POST -H "Content-Type: application/json" \
   -d '{"query": "What are symptoms of depression?"}' \
   https:///chat
   ```

### Example Response:
```
{
  "response": "Common symptoms of depression include sadness, lack of energy, and loss of interest in activities."
}
```

---

## 📂 Project Structure

```
health-query-chatbot/
├── main.py                 # Flask API code
├── model_training.ipynb    # ipynb notebook for training the model
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
├── data/                   # Medical datasets used for training
│   ├── Mental_Health_FAQ.csv  
│   ├── HealthCare_Chatbot.csv  
│   └── Multi_Class_Medical.csv  
└── saved_model/            # Directory containing saved model and tokenizer files
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add feature"`).
4. Push to your branch (`git push origin feature-name`).
5. Open a pull request.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
