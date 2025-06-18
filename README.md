# 🧠 Code Review Optimization using NLP & Neural Networks  
Classifying refactoring vs. non-refactoring commit messages using supervised and unsupervised learning

## 📌 Overview  
This project investigates whether a Git commit message indicates a **refactoring change** or not — a key insight to optimize developer time and improve software quality. We built both unsupervised and supervised models to automate this classification.

> Built as part of DSCI-644 (Rochester Institute of Technology)

## 🎯 Goals  
- Identify differences in performance between **unsupervised clustering** and **supervised classification**
- Enable **automated detection** of refactoring efforts in commit histories
- Reduce manual effort in **code review pipelines**

## 📊 Key Results  
| Method               | Description                        | Accuracy |
|----------------------|------------------------------------|----------|
| Feedforward NN       | Supervised binary classification   | **95.7%** |
| KMeans + TF-IDF      | Unsupervised clustering (k=2)      | Qualitative only |

---

## 🛠️ Tech Stack  
- **Language**: Python  
- **Modeling**: TensorFlow/Keras, Scikit-learn  
- **NLP**: CountVectorizer, TF-IDF  
- **Tools**: Jupyter Notebooks, Pandas, NumPy, Matplotlib  

---

## 🧪 Experiments

### ✅ Supervised Classification (Neural Network)
- **Preprocessing**: Tokenization, stopword removal, vectorization using `CountVectorizer`
- **Architecture**: 3 Dense layers, ReLU activations, dropout for regularization
- **Loss/Opt.**: Binary cross-entropy + Adam optimizer
- **Split**: 80/20 training/validation  
- **Result**: Achieved 95.7% test accuracy in identifying refactoring commit messages

### 🔍 Unsupervised Clustering (TF-IDF + KMeans)
- **Vectorization**: TF-IDF transformation
- **Clustering**: KMeans with k=2 (refactor vs. non-refactor)
- **Outcome**: Generated interpretable clusters, but lacked label alignment for accuracy scoring

---

## 📂 Repo Structure
