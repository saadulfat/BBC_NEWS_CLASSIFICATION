# 📰 BBC News Text Classifier

A machine learning project that classifies BBC news articles into one of five categories using Natural Language Processing (NLP) techniques and a Logistic Regression classifier.

---

## 📌 Project Overview

The objective of this project is to build a multiclass text classification model capable of automatically categorizing news articles based on their content.

The classifier predicts one of the following categories:

* 💼 Business
* 🎭 Entertainment
* 🏛️ Politics
* ⚽ Sport
* 💻 Technology

This project demonstrates the complete machine learning pipeline, including data preprocessing, feature extraction, model training, evaluation, and prediction on custom text.

---

## 📂 Dataset

**Dataset:** BBC News Dataset

The dataset contains **2,225** BBC news articles labeled into five different categories.

| Feature    | Description                  |
| ---------- | ---------------------------- |
| `text`     | Full news article            |
| `category` | News category (target label) |

### Category Distribution

* Business
* Entertainment
* Politics
* Sport
* Technology

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* NLTK
* Matplotlib
* Seaborn

---

## ⚙️ Methodology

### 1. Data Loading

The BBC News dataset was loaded from a CSV file into a Pandas DataFrame.

### 2. Data Preprocessing

The following preprocessing steps were applied:

* Converted text to lowercase
* Removed punctuation
* Removed English stopwords
* Preserved meaningful words for feature extraction

### 3. Train-Test Split

The dataset was split into:

* **80% Training Data**
* **20% Testing Data**

A fixed random state was used to ensure reproducible results.

### 4. Feature Extraction

The textual data was transformed into numerical vectors using **TF-IDF (Term Frequency–Inverse Document Frequency)**.

TF-IDF was chosen because it highlights important words while reducing the influence of very common words across documents.

### 5. Model Training

A **Logistic Regression** classifier was trained on the TF-IDF features.

This model was selected because it:

* Performs well on sparse text data
* Is computationally efficient
* Serves as a strong baseline for text classification
* Is simple to interpret and implement

---

## 📊 Model Evaluation

The trained model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

The classifier achieved approximately **95–98% accuracy**, demonstrating strong performance in distinguishing between the five news categories.

---

## 📁 Project Structure

```
BBC-News-Text-Classifier/
│
├── BBC_News_Classifier.ipynb
├── bbc-text.csv
├── requirements.txt
└── README.md
```

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/BBC-News-Text-Classifier.git
cd BBC-News-Text-Classifier
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```
BBC_News_Classifier.ipynb
```

Run all cells sequentially.

---

## 🧪 Testing the Model

After training, you can enter your own news headline or article, for example:

```
Apple announced a new AI-powered chip designed for future smartphones and laptops.
```

Expected prediction:

```
Technology
```

---

## 📈 Future Improvements

Possible enhancements include:

* Applying stemming or lemmatization
* Hyperparameter tuning using GridSearchCV
* Comparing multiple classifiers (Naive Bayes, Support Vector Machine, Random Forest)
* Using pretrained language models such as BERT for improved performance
* Deploying the classifier as a web application using Flask or Streamlit

---

## 📝 Assumptions

* The dataset labels are accurate and suitable for supervised learning.
* English stopwords are removed during preprocessing.
* No stemming or lemmatization is applied.
* Default TF-IDF parameters provide a strong baseline representation of the text.

---

## 📚 Key Learning Outcomes

This project demonstrates:

* Text preprocessing for NLP
* TF-IDF feature extraction
* Multiclass text classification
* Logistic Regression for NLP tasks
* Performance evaluation using standard classification metrics
* Building an end-to-end machine learning workflow in Python

---

## 👨‍💻 Author

Developed as part of a machine learning assignment to demonstrate practical text classification using Python and Scikit-learn.
