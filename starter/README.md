# Purpose of this Folder

This folder should contain the scaffolded project files to get a student started on their project. This repo will be added to the Classroom for students to use, so please do not have any solutions in this folder.

# StyleSense Product Recommendation Classifier

## Project Overview

This project is part of the Udacity Data Scientist Nanodegree and focuses on building a complete machine learning pipeline. The goal is to predict whether a customer would recommend a clothing product based on a review they left and additional features like their age and the product category.

The solution is meant to help StyleSense, a fast-growing online fashion retailer, handle missing recommendation labels by using existing review text and metadata to predict customer sentiment. This will enable StyleSense to make better product decisions, surface trending products, and improve overall customer satisfaction.

## Project Structure

dsnd-pipelines-project-dragm13/
├── data/
│ └── reviews.csv # Provided dataset
├── model/
│ └── final_model.pkl # Saved machine learning pipeline
├── notebook.ipynb # Jupyter Notebook with code and analysis
├── requirements.txt # Dependencies
└── README.md # This file

## How to Run This Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/dsnd-pipelines-project.git
cd dsnd-pipelines-project

### 2. Install dependencies

python3 -m pip install -r requirements.txt

### 3. Launch the notebook

jupyter notebook notebook.ipynb

### 4. Features Used

The machine learning model uses the following features:

Age: Age of the reviewer

Positive Feedback Count: How many users found the review helpful

Review Text: Free text describing the customer's experience

Review Length: Word count of the review

Division Name, Department Name, Class Name: Categorical product categories

### 5. Machine Learning Pipeline

The project uses a Scikit-learn pipeline to combine all processing and modeling steps, ensuring clean, repeatable, and modular code.

### 6. Preprocessing Steps

Numerical data: Median imputation + standard scaling

Categorical data: Most frequent imputation + one-hot encoding

Text data: TF-IDF vectorization with stop words removed (English)

### 7. Model
RandomForestClassifier inside the pipeline

Trained and fine-tuned using cross-validation and grid search

Full integration with preprocessing steps

### 8. Model Evaluation
The model was evaluated using accuracy, precision, recall, and F1 score.

Confusion matrices and classification reports are included in the notebook.

### 9. Hyperparameter Tuning
The model was fine-tuned using GridSearchCV with 3-fold cross-validation. Parameters tuned:

{
  "classifier__n_estimators": [100, 200],
  "classifier__max_depth": [None, 10, 20],
  "classifier__min_samples_split": [2, 5]
}

### 10. Highlights
End-to-end ML pipeline using Pipeline and ColumnTransformer

Handles numeric, categorical, and text features

Integrated grid search and cross-validation


