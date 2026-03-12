
# Hate Speech Detection System

## 📌 Project Overview
This project implements a **Hate Speech Detection System** using **Natural Language Processing (NLP)** and **Deep Learning** techniques.  

The system analyzes text comments and classifies them into three categories:

- **Hate Speech**
- **Offensive Language**
- **Safe / Neutral**

The goal of this system is to help detect harmful or abusive content in online platforms automatically.

---

# 🎯 Project Objectives

The main objectives of this project are:

- Automatically detect hate speech in text.
- Classify comments into hate, offensive, or safe categories.
- Improve online content moderation using AI.
- Apply deep learning techniques to real-world NLP problems.

---

# 🧠 Technologies Used

The following technologies and libraries were used in this project:

- **Python**
- **PyTorch**
- **Hugging Face Transformers**
- **NLTK**
- **Scikit-learn**
- **Pandas**
- **NumPy**

---

# 📊 Datasets Used

The model was trained using multiple datasets to improve performance and generalization:

1. **Hate Speech and Offensive Language Dataset**
2. **TweetEval Hate Speech Dataset**
3. **TweetEval Offensive Language Dataset**

These datasets were merged into a single dataset before training.

---

# 🔄 Data Preprocessing

Before training the model, the text data was cleaned using several preprocessing steps:

- Converting text to lowercase
- Removing URLs
- Removing mentions (@username)
- Removing hashtags symbols
- Removing numbers
- Removing punctuation
- Removing extra spaces

Example:

Original text:
```

"I hate you!!!"

```

After preprocessing:
```

hate you

```

---

# 🏗 Model Architecture

The project uses a transformer-based model:

**XLM-RoBERTa Base**

This model is designed for multilingual natural language processing and performs well on text classification tasks.

---

# ⚙️ Training Configuration

| Parameter | Value |
|--------|--------|
| Model | XLM-RoBERTa |
| Epochs | 7 |
| Batch Size | 16 |
| Max Length | 160 |
| Optimizer | AdamW |
| Learning Rate | 2e-5 |

To address **class imbalance**, weighted cross-entropy loss was used during training.

---

# 📈 Model Evaluation

The model was evaluated using standard classification metrics:

- **Precision**
- **Recall**
- **F1-score**
- **Accuracy**

### Classification Report

```

```
          precision    recall  f1-score   support

    hate       0.53      0.71      0.61      1042
```

offensive       0.88      0.82      0.85      4626
safe       0.85      0.84      0.84      3468

```
accuracy                           0.82      9136
```

macro avg       0.75      0.79      0.77      9136
weighted avg       0.83      0.82      0.82      9136

```

Overall **Accuracy: 82%**

---

# 🔍 Prediction Example

Example input:
```

I hate you

```

Model output:
```

Prediction: Hate

```

Another example:
```

You are amazing

```

Model output:
```

Prediction: Safe

````

---

# 🚀 How to Run the Project

### 1️⃣ Install Dependencies

```bash
pip install transformers torch datasets nltk scikit-learn pandas numpy
````

---

### 2️⃣ Train the Model

Run the notebook or Python script to train the model.

---

### 3️⃣ Test the Model

Example:

```python
classify_text_confidence("You are stupid")
```

Output:

```
Offensive
```

---

# 📂 Project Structure

```
HateSpeechDetection
│
├── data
│
├── preprocessing
│
├── training
│
├── evaluation
│
├── model
│
└── README.md
```

---

# 🔮 Future Improvements

Possible improvements include:

* Adding Arabic hate speech detection
* Improving the detection of hate speech class
* Increasing dataset size




