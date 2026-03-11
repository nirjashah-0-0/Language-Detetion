# Language Detection

## Overview  
This project builds a **language detection** model that predicts the language of a given text snippet using classical machine learning techniques on a multilingual dataset.

## Dataset  
The notebook uses a CSV file named `LanguageDetection.csv` with two main columns:  
- `Text`: the input sentence or phrase.  
- `Language`: the corresponding language label.  

The dataset includes samples from multiple languages, such as:  
- English  
- French  
- Spanish  
- Portuguese  
- Italian  
- Russian  
- Swedish  
- Malayalam  
- Dutch  
- Arabic  
- Turkish  
- German  
- Tamil  
- Danish  
- Kannada  
- Greek  
- Hindi  

## Project Workflow  

### 1. Data Loading and Exploration  
- Load the dataset using **pandas** from `LanguageDetection.csv`.  
- Inspect the distribution of samples per language using `value_counts()` to check class balance.  

### 2. Preprocessing  
- Separate features and labels:  
  - `X` contains the raw text.  
  - `y` contains the language labels.  
- Encode language labels into numeric form using **LabelEncoder** from `sklearn.preprocessing`.  
- Clean the text data by:  
  - Removing symbols, punctuation, and numbers using regular expressions (`re`).  
  - Converting all text to lowercase.  
  - Storing the preprocessed text in a list for later vectorization.  

### 3. Feature Extraction  
- Use **CountVectorizer** from `sklearn.feature_extraction.text` to create a **Bag-of-Words** representation.  
- Transform the preprocessed text into a numerical feature matrix suitable for model training.  

### 4. Train–Test Split  
- Split the data into training and test sets using `train_test_split` from `sklearn.model_selection` with a test size of 20%.  

### 5. Model Training  
- Train a **Multinomial Naive Bayes** classifier (`MultinomialNB`) on the training data.  
- This model is well suited for text classification tasks with discrete count features.  

## Technologies Used  
- **Language:** Python  
- **Libraries:**  
  - Data handling: `pandas`, `numpy`  
  - Text preprocessing: `re`  
  - Feature extraction: `sklearn.feature_extraction.text` (`CountVectorizer`)  
  - Modeling: `sklearn.naive_bayes`, `sklearn.model_selection`, `sklearn.preprocessing`  
  - Visualization (optional EDA): `seaborn`, `matplotlib.pyplot`  

## How to Run  

1. Clone the repository:  
   ```bash
   git clone <your-repo-url>.git
   cd <your-repo-folder>
2. Install dependencies
   ```bash
   pip install -r requirements.txt
3. Launch Jupyter Notebook and open the project file:
   ```bash
   jupyter notebook LanguageDectection
4. Run all cells to:
- Load and preprocess the data
- Vectorize the text
- Train the Naive Bayes model
- Evaluate its language detection performance

## Possible Extensions
- Replace Bag-of-Words with TF-IDF features.
- Experiment with additional models (Logistice Regression, SVM or Neural Network)
- Build a simple web app or API for real-time language detection

Author : Nirja Shah
   
