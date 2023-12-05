

# Statistical Learning Project (Supervised Learning)

==============================

---

Explore a concise overview of the project [here](https://sucologiqsolutions.com/multiclass-classification-project/).

Feel free to review the details.

---

## Project Overview
This project aims to develop a robust statistical learning model for multiclass classification of penguins, leveraging key morphological features. The primary objective is to comprehensively train on all models covered in class, even with the intentional introduction of NA (Not Available) values and outliers for increased complexity and real-world simulation.

The mentioned models have been applied under the assumption of independence, even when considering correlated features like CulmenLength and CulmenDepth, FlipperLength and BodyMass, and Species and Culmen Length/Depth Different penguin species, as we will see in the Correlation Plot incorporated in the project. 

**Scope**
The scope of this project encompasses a thorough exploration of different algorithms and techniques, providing a comprehensive learning experience. The deliberately chosen dataset facilitates a detailed understanding of various models and avoids confining the analysis to a limited set.

**Documentation and Code Transparency**
Ensuring transparency, reproducibility, and comprehension, the project documentation and code maintain a high level of transparency. The penguins dataset used is credited to Dr. Kristen Gorman and the Palmer Station, Antarctica LTER, part of the Long Term Ecological Research Network.

**Project Objective**
The overarching goal is to develop a predictive model precisely classifying penguins into their respective species based on specified morphological features. Achieving this objective contributes valuable insights to statistical learning techniques in species classification, impacting ecological research and enhancing understanding of penguin diversity.

**Target Audience**
This analysis is designed to resonate with researchers, ecologists, and conservationists interested in comprehending and conserving penguin biodiversity. The resulting classification model could become a practical tool for wildlife monitoring programs, supporting ongoing efforts in environmental conservation.

**Project Approach Overview**
The project employs a structured approach to explore various supervised learning models for maximizing testing accuracy. The iterative process involves configuring models with diverse hyperparameters in the first iteration and selecting influential features in the second iteration. The exception is the neural network model, which addresses overfitting through balancing accuracy via Loss Over Epochs.

At the project's conclusion, a comprehensive comparison of all models will be presented, evaluating their performance metrics. This approach enables understanding the impact of hyperparameters, feature selection, and overfitting mitigation on the diverse set of models explored.

------------

## Directory Structure

```plaintext
    ├── LICENSE
    ├── Makefile           			 <- Makefile with commands like `make data` or `make train`
    ├── README.md          			 <- The top-level README for developers using this project.
    ├── data
    │   ├── interim       			 <- Intermediate data that has been transformed.
    │   ├── processed     			 <- The final, canonical data sets for modeling.
    │   └── raw           			 <- The original, immutable data dump.
    │
    ├── docs             			 <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── EDA_Visualizations 			 <- To store images from our EDA & Modeling, etc.
    │
    ├── models             			 <- Trained and serialized models, model predictions, or model summaries
    │   ├── Confusion_Classification_Metrics     <- Visualizations for model evaluation.
    │   └── Evaluation_Metrics            	 <- Visualizations for evaluation metrics.
    │
    ├── notebooks         			 <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                        			    the creator's initials, and a short `-` delimited description, e.g.
    │                         			    `1.0-jqp-initial-data-exploration`.
    │
    ├── references         			 <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            			 <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        			 <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   			 <- The requirements file for reproducing the analysis environment, e.g.
    │                        			    generated with `pip freeze > requirements.txt`
    │
    ├── setup.py          			 <- makes project pip installable (pip install -e .) so src can be imported
    │
    └── tox.ini            			 <- tox file with settings for running tox; see tox.readthedocs.io

--------

## Data Directory

The project's data directory is organized into three subdirectories:
- **Interim:** Contains intermediate data that has undergone transformation during the preprocessing phase.
- **Processed:** Holds the final, canonical data sets prepared for modeling, featuring all necessary enhancements.
- **Raw:** Represents the original, immutable data dump in its untouched state, serving as the foundation for all subsequent data manipulations.

--------

## Preprocessing

The project began by splitting the dataset into training and validation sets to prevent data leakage. The Exploratory Data Analysis (EDA) phase involved handling missing values and outliers separately, utilizing various visualizations such as pivoted tables and scatterplots. 

Correlated variables were identified for treatment in the modeling section. Outliers were imputed using the Interquartile Range (IQR) method, and missing values were addressed using SimpleImputer. Non-normally distributed variables were normalized using standardScaler(). Both numerical and categorical data were encoded appropriately. 

To tackle dataset imbalance, the Synthetic Minority Over-sampling Technique (SMOTE) was applied, generating synthetic samples for the minority class while preserving essential information from the majority class.

--------

## Visualizations

Explore a diverse range of visualizations in the project, including pivoted tables, circle graphs, boxplots, scatterplots, and correlation maps. These visual representations offer profound insights into penguin distribution, species attributes by sex, and attributes by island. Find these visualizations conveniently located in the **EDA_Visualizations folder path**.

--------

## Training  & Usage

Leverage the trained model for predictions by accessing the models stored in the dedicated **"models" folder**, encompassing a suite of 12 distinct models.

--------

## Evaluation

The model undergoes comprehensive evaluation using diverse classification metrics, including AUC values, ROC curves, confusion matrices, classification reports, and additional metrics. For a detailed breakdown of these metrics, please refer to the **"Evaluation_Metrics"** and **"Confusion_Classification_Metrics" folders** inside the **"Models" directory**.

--------

## Results

The modeling approach involved hyperparameter tuning using a grid search with cross-validation across various algorithms. Notably, Logistic Regression models with grid search achieved a remarkable testing accuracy of 96.51%, and KNN models with feature selection led with a high ROC AUC of 99.70%.

Comparison of models revealed the superior performance of Logistic Regression with grid search using all features, excelling in precision (96.41%), recall (96.77%), and F1-score (96.46%). The modeling phase also addressed issues such as overfitting, with the Neural Network demonstrating effective avoidance.

Decision Tree models were excluded due to consistently inferior performance, while KNN and Logistic Regression models were set aside due to a notable disparity between testing and training accuracy, suggesting potential overfitting. Neural Network models were eliminated due to performance divergence and suboptimal metrics.

The Naive Bayes Model with feature selection emerged as the most balanced and reliable choice, displaying strong performance across multiple metrics, minimal difference between training and testing accuracy, and a nuanced understanding of its strengths. This recommendation is based on a comprehensive evaluation of the model's rankings across various dimensions, aligning with the goal of robust and reliable model deployment.

--------

## Contact Information

For questions or collaboration, contact davidsuerocobos99@gmail.com

--------

## References

Notes given in class by Professor Qurat-ul-Ain Azim.

--------

## Project Status

The project has been successfully completed, reaching its culmination.

--------

