## 📝 Random Text Generator using Trigram Markov Model (Python)

This Python project implements a **random text generator** based on a **trigram Markov model**, trained on the popular **20 Newsgroups dataset**. The model learns the structure and style of the training corpus and can generate new, realistic-looking text.

---

### 📌 Key Features

- Trains a trigram-based Markov chain model on a raw text corpus.
- Randomly generates new text sequences based on learned word transitions.
- Supports training on custom datasets (default: 20 Newsgroups).
- Simple, lightweight implementation — no deep learning required!

---

### 🧠 How It Works

1. Tokenize text data into words.
2. Build a trigram dictionary:  
   `{ (w1, w2): [w3_1, w3_2, ...] }`
3. Start with a random bigram seed.
4. Sample next words from the trigram distribution to build a text sequence.

---

### 📦 Requirements

- Python 3.7+
- `sklearn` (for loading 20 Newsgroups)
- `nltk` (for basic tokenization)

Install dependencies:
```bash
pip install scikit-learn nltk
```

### 📚 Dataset

Uses the **20 Newsgroups** dataset from `sklearn.datasets`:
```python
from sklearn.datasets import fetch_20newsgroups
```

You can replace it with any corpus of your own.

---

### 🔧 Configurable Options

| Option | Description |
|--------|-------------|
| `text_length` | Number of words to generate |
| `start_seed` | Optional manual bigram to begin generation |
| `min_word_freq` | Frequency threshold to filter rare tokens |
| `lowercase` | Enable/disable case normalization |

---

### 📈 Possible Extensions

- [ ] Add smoothing for unseen trigrams
- [ ] Support punctuation-aware generation
- [ ] Train with bigram or 4-gram variants
- [ ] Save/load model from disk (pickle or JSON)
- [ ] Add CLI and stream generation mode

