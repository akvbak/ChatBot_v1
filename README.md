# 🧠 General Knowledge Chatbot with PyTorch

- A basic general knowledge chatbot built with Python and PyTorch. Understands user intents and responds to queries concerning topics such as Geography, Science, Literature, Mathematics, History, Technology, Pop Culture, Fun Facts & Random Trivia and more.
- The bot is designed for educational and exploratory purposes and can be extended easily with new intents and functionalities.

## ✨ Features

- Intent classification using a custom feedforward neural network
- Training with tokenized and lemmatized input text
- General knowledge questions across a wide variety of domains
- Extensible with custom functions using function_mappings
- Lightweight CLI interaction loop for testing

---

## 📁 Project Structure

```

├── main.py               # Python script containing the chatbot logic
├── intents.json          # Contains training data: tags, patterns, and responses
├── chatbot_model.pth     # Saved trained model weights (generated after training)
├── dimensions.json       # Stores model input/output size info (generated after training)
└── README.md             # Project documentation
```

---

## ⚙️ Requirements

- Python 3.6+
- PyTorch
- NumPy
- NLTK

Install dependencies:

```bash
pip install torch numpy nltk
```

Also, run the following once to download required NLTK data:

```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
```

---

## 🚀 How to Run

```bash
git clone https://github.com/akvbak/ChatBot_v1/
python main.py
```

Then interact with the bot via the terminal. Type `exit` to stop the chatbot.

---

## 🏗 How It Works

1. **Data Preparation**  
   The bot reads and parses `intents.json` containing:
   - `tag`: unique label for each intent.
   - `patterns`: example phrases a user might type.
   - `responses`: replies the bot can give.

2. **Training the Model**  
   The chatbot:
   - Tokenizes and lemmatizes all patterns.
   - Creates a bag-of-words vector for each pattern.
   - Trains a simple 3-layer feedforward neural network using PyTorch.

3. **Prediction & Response**  
   - Converts new user input into a bag-of-words vector.
   - Predicts the intent with the highest probability.
   - Returns a random response from the matching intent.

---

## 🔧 Example Usage

```
User: How do I open savings account 2?
Bot: Sure! To open savings account 2, you'll need to verify your identity.

User: Thank you
Bot: You're Welcome

User: exit
```

---

## 📌 Notes

- You can expand the `intents.json` file to support more tags and user inputs.
- Add mappings for tags in `function_mappings` to trigger backend actions or API calls.
- Currently, the chatbot runs in the terminal but can be easily integrated into a web or mobile interface.

---

## 🛠️ Future Improvements
- Add support for contextual conversations
- Integrate with a web interface using Flask or Streamlit
- Extend intents with other topics (sports, finance, health)
- Use pre-trained embeddings like Word2Vec or BERT for better accuracy

---

## 👨🏽‍💻 Author

Created by **Kekeli Akaba** as a learning project for neural networks, intent classification, word tokenization & lemmatization and chatbot development in Python.
