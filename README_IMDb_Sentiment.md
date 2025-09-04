# Sentiment Analysis of IMDb Movie Reviews 🎬📊  

## 📌 Project Overview  
This project applies **Machine Learning** techniques to perform **Sentiment Analysis** on IMDb movie reviews. The task is to classify reviews as **positive** or **negative** based on their textual content.  

The project was developed as part of my **Internshala Data Science Training**.  

---

## 📂 Dataset  
- **Source**: Provided by Internshala platform during training.  
- **Details**:  
  - 50,000 reviews in total  
  - Balanced dataset → 25,000 positive, 25,000 negative  
  - Stored in `Imdb.xlsx`  
  - No missing values  

---

## ⚙️ Data Preprocessing  
Steps performed on raw reviews:  
- Removal of HTML tags  
- Removal of non-alphabetic characters  
- Conversion to lowercase  
- Tokenization  
- Stopword removal  
- Lemmatization  
- Added a new column `cleaned_review`  

---

## 🧑‍💻 Feature Engineering  
- **TF-IDF Vectorization**:  
  - Used `TfidfVectorizer`  
  - Shape: `(50000, 5000)`  
- **Additional Features**:  
  - Word count  
  - Character count  
  - Average word length  
- **Final feature set** = TF-IDF + additional features → 5003 features  

---

## 🔀 Train-Test Split  
- 80% Training → 40,000 samples  
- 20% Testing → 10,000 samples  
- Stratified split with `random_state=42`  

---

## 🤖 Models Implemented  
- Logistic Regression  
- Naive Bayes  
- Linear SVM  
- Random Forest  

---

## 🏆 Model Performance  
- **Best Models**: Logistic Regression & Linear SVM  
- **Final Chosen Model**: Logistic Regression (due to stability and interpretability)  

**Hyperparameter Tuning (GridSearchCV on Logistic Regression):**  
- Best Params → `{'C': 1, 'solver': 'lbfgs'}`  
- Cross-validation Accuracy → **88.59%**  
- Test Accuracy → **88.62%**  

---

## 📊 Results  
- Successfully classified reviews into **positive** and **negative** with ~**88.6% accuracy**  
- Demonstrated the effectiveness of TF-IDF + Logistic Regression for text classification  

---

## 🚀 How to Run the Project  

### 1️⃣ Clone the repository  
```bash
git clone https://github.com/your-username/Sentiment-Analysis-of-IMDb-Movie-Reviews.git
cd Sentiment-Analysis-of-IMDb-Movie-Reviews
```

### 2️⃣ Install dependencies  
```bash
pip install -r requirements.txt
```

### 3️⃣ Run the notebook  
Open the Jupyter Notebook and execute step by step:  
```bash
jupyter notebook "Project A (IMDb Movie Review Sentiment Analysis).ipynb"
```

---

## 📌 Future Enhancements  
- Use **word embeddings** (Word2Vec, GloVe, FastText)  
- Implement **deep learning models** (LSTMs, GRU, BERT) for better accuracy  
- Deploy as a **web app** for real-time sentiment prediction  

---

## 📷 Screenshots  
(Add the result screenshots you shared earlier here in the repo and reference them like below)  

![Confusion Matrix](screenshots/sentiment_confusion_matrix.png)  
![Classification Report](screenshots/sentiment_classification_report.png)  

---

## ✨ Author  
**Ayush Saini**  
- Data Science Enthusiast | Machine Learning | NLP  
- [LinkedIn](#) | [GitHub](#)  
