
# **AI vs Human Text Classification: Detecting AI-Generated Text**

## **Overview**
This project aims to classify text as either **human-written** or **AI-generated** using machine learning techniques. By analyzing a dataset of essays, we explored linguistic, semantic, and stylistic features to build an accurate and interpretable model. The pipeline includes data preprocessing, feature extraction, dimensionality reduction using PCA, and model training with several classifiers. 

The final model, leveraging a Random Forest classifier with PCA-transformed features, achieved an accuracy of **93.21%**, making it a tool for distinguishing AI-generated text from human-written text.

The dataset and inspiration for this project came from the **Kaggle competition**: [Detect AI-Generated Text](https://www.kaggle.com/competitions/llm-detect-ai-generated-text).

---

## **Features**
1. **Balanced Dataset**: 
   - Addressed class imbalance by undersampling the majority class.
2. **Feature Engineering**: 
   - Extracted advanced text-based features, such as:
     - **Basic Statistics**: Word count, character count, sentence count.
     - **Syntactic Patterns**: Part-of-speech counts, syntactic diversity, burstiness.
     - **Lexical Metrics**: Type-token ratio (TTR), lexical density, unique word ratio.
     - **Readability Scores**: Gunning Fog Index, SMOG Index.
     - **Semantic Features**: Sentence coherence and semantic density using Sentence-BERT embeddings.
3. **Dimensionality Reduction**: 
   - Applied Principal Component Analysis (PCA) to focus on the most informative patterns.
4. **Model Training**:
   - Tested multiple classifiers (Random Forest, SVM, Gradient Boosting) and optimized Random Forest for the best results.
5. **Evaluation**:
   - Used an 80/20 train-test split and assessed performance.

---

## **Highlights**
- **Accuracy**: Final model achieved **93.21%** accuracy with 11 PCA components.
- **Visualization**: Used PCA for dimensionality reduction and visualized the class separability of the dataset.
- **Comparative Analysis**: Tested multiple classifiers, with Random Forest outperforming SVM and Gradient Boosting.

---

## **Project Pipeline**

1. **Data Exploration**:
   - Loaded and inspected the dataset for class imbalance and statistical properties (word count, sentence count, etc.).

2. **Feature Extraction**:
   - Engineered features to capture linguistic and stylistic nuances.

3. **Dimensionality Reduction**:
   - Performed PCA to reduce the feature space, balancing simplicity and variance retention.
   - Evaluated models with both 2 components (for visualization) and 11 components (for high performance).

4. **Model Training and Testing**:
   - Split the dataset into 80% training and 20% testing.
   - Compared Random Forest, SVM, and Gradient Boosting classifiers, selecting Random Forest for its superior performance.
   - Saved the best-performing model for deployment.

5. **Evaluation**:
   - Highlighted strengths and limitations of the methods used.
   - Proposed future improvements, including expanding datasets and exploring deep learning techniques.

---

## Acknowledgements**
- The dataset and inspiration for this project came from the Kaggle competition.
- Special thanks to O’Donnell Data Science and Research Computing Institute for their support and guidance throughout this project.
