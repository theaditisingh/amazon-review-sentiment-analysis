# 🛍️ Amazon Review Sentiment Analyser

Classifies Amazon product reviews as **Positive**, **Neutral**, or **Negative** using two approaches — a simple TF-IDF baseline and a fine-tuned DistilBERT transformer model.

---

## 📌 What it does

Takes raw Amazon review text as input and predicts the sentiment:
- ⭐ 4–5 stars → **Positive**
- ⭐ 3 stars → **Neutral**
- ⭐ 1–2 stars → **Negative**

---

## 📦 Dataset

- **Source:** [Amazon Product Reviews – Kaggle](https://www.kaggle.com/datasets)
- **Size:** ~50,000 reviews
- **Columns used:** `reviewText` (input), `overall` (star rating → label)

> Dataset not included in this repo. Download from Kaggle and place the CSV in the root folder.

---

## 📊 Model Comparison

| Model | Accuracy | Notes |
|---|---|---|
| TF-IDF + Logistic Regression | _fill yours_ | Fast, lightweight baseline |
| DistilBERT (pre-trained) | _fill yours_ | Transformer-based, much more accurate |

---

## 🗂️ Project Structure

```
├── sentiment_analysis.ipynb   # Main notebook (EDA + training + evaluation)
├── requirements.txt           # Python dependencies
└── README.md
```

---

## 🚀 How to run it

**Option 1 — Google Colab (recommended, free)**

1. Open `sentiment_analysis.ipynb` in [Google Colab](https://colab.research.google.com)
2. Go to **Runtime → Change runtime type → T4 GPU**
3. Download the dataset from Kaggle and upload the CSV to Colab
4. Run all cells top to bottom (`Shift + Enter`)

**Option 2 — Run locally**

```bash
git clone https://github.com/YOUR_USERNAME/amazon-sentiment-analyser.git
cd amazon-sentiment-analyser
pip install -r requirements.txt
jupyter notebook sentiment_analysis.ipynb
```

---

## 🛠️ Tech Stack

- Python 3.10+
- HuggingFace Transformers (`distilbert-base-uncased-finetuned-sst-2-english`)
- Scikit-learn (TF-IDF + Logistic Regression)
- Pandas, Seaborn, Matplotlib
- Google Colab (training environment)

---

## 📝 License

MIT License — free to use and modify.
