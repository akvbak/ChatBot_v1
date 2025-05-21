# 🧠 Banking Chatbot with PyTorch

A basic banking and finance chatbot built with Python and PyTorch. Understands user intents using NLP and responds intelligently to queries like opening accounts, card issues, and more.

## ✨ Features

- Recognizes over 100 banking-related intents (e.g., account opening, card issues, balance inquiries).
- Trained on custom `intents.json` with example phrases and corresponding responses.
- Uses bag-of-words model and PyTorch neural network for intent classification.
- Supports custom action mapping (e.g., running a function when an intent is matched).
- Extensible and easy to train or retrain with new intents.

---

## 📁 Project Structure

.
├── main.py # Python script containing the chatbot logic
├── intents.json # Contains training data: tags, patterns, and responses
├── chatbot_model.pth # Saved trained model weights (generated after training)
├── dimensions.json # Stores model input/output size info (generated after training)

---

## ⚙️ Requirements

- Python 3.6+
- PyTorch
- NumPy
- NLTK

Install dependencies:

```bash
pip install torch numpy nltk
