# Smart Skincare Recommender 💆‍♀️🌿

A machine learning-powered solution for personalized skincare product recommendations based on ingredient analysis and user skin types. This project explores the intersection of dermatology and AI to deliver tailored, explainable cosmetic suggestions for dry, oily, combination, and sensitive skin types.

## 🧠 Project Overview

Millions struggle with ineffective skincare routines due to generic product suggestions. This project uses data science to:

- Predict skincare product effectiveness based on ingredients and skin type compatibility
- Identify key active ingredients (e.g., retinol, hyaluronic acid, vitamin C)
- Deliver top-N product recommendations tailored to each user profile

## 🔬 Dataset

*File*: cosmetics.csv  
- Ingredients (raw and processed)
- Binary flags for skin types: Dry, Oily, Sensitive, Combination
- User ratings (proxy for product effectiveness)

If the full dataset can't be shared, a synthetic sample is included for demonstration purposes.

## 🧹 Preprocessing & Feature Engineering

- Tokenized and standardized ingredient lists
- Created binary flags for key actives (e.g., has_retinol)
- Used CountVectorizer to transform ingredient text
- Engineered skin type compatibility features

## 🛠️ Models Used

### 🧪 Supervised Learning
- Logistic Regression
- Random Forest
- Gradient Boosting
- *CatBoost* (best performance)
- Evaluation: Accuracy, Precision, Recall, F1-Score

### 📊 Unsupervised Learning
- Gaussian Mixture Models (GMM) for product clustering
- PCA for dimensionality reduction and cluster visualization

## 📈 Results

| Model         | Accuracy | Recall | F1 Score |
|---------------|----------|--------|----------|
| Logistic Reg. | 65.4%    | 68.1%  | 75.4%    |
| Random Forest | 70.8%    | 86.0%  | 82.0%    |
| CatBoost 🔥   | *75.2%| **94.8%| **85.6%*|

✅ Custom thresholding (0.40) boosted recall to improve top-product detection.  
✅ GMM clustering revealed 5 meaningful product archetypes (e.g., “Hydrating Brighteners”).

## 🧴 Personalized Recommendation Engine

Given a user's skin type:
- Filters compatible products
- Ranks by model-predicted effectiveness
- Scores for ingredient relevance and cluster similarity
- Returns top 5 tailored product suggestions

## 📌 Key Features

- Ingredient analysis for skin-type targeting
- Data-driven ranking with model + clustering hybrid logic
- Interpretability via binary ingredient flags
- Scalable ML pipeline

## 📚 Files in this Repository

| File                         | Description |
|------------------------------|-------------|
| skincare_analysis_notebook.ipynb | Jupyter notebook with all preprocessing, modeling, and recommendation logic |
| cosmetics.csv              | Dataset used (share a sample if proprietary) |
| bmin_final_report.pdf      | Detailed write-up of the project methodology and results |
| BMIN Project Proposal.docx | Initial research proposal |
| requirements.txt           | Required Python packages |
| .gitignore                 | Git-ignore config |
| LICENSE                    | MIT License (default) |

## 🚀 How to Use

```bash
# Clone the repo
git clone https://github.com/ishwarimulay29/smart-skincare-recommender
cd smart-skincare-recommender

# Install dependencies
pip install -r requirements.txt

# Launch notebook
jupyter notebook skincare_analysis_notebook.ipynb
