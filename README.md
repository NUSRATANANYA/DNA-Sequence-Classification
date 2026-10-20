Title: Comparative Evaluation of Traditional Machine Learning and Deep Learning Models for DNA Sequence Classification

Overview

This project investigates seven-class gene-family classification from DNA sequences using traditional machine-learning algorithms and a deep-learning model. The experiments use DNA sequences from the Human, Chimpanzee, and Dog files in the selected Kaggle dataset.

Important: The prediction target is the gene-family class, not the species.

Project Links

- Dataset Citation: N. Singh, "DNA Sequence Dataset," Kaggle. Available at: "DNA Sequence Dataset" (https://www.kaggle.com/datasets/nageshsingh/dna-sequence-dataset). Accessed October 19, 2026.
- GitHub Repository: "DNA-Sequence-Classification" (https://github.com/NUSRATANANYA/DNA-Sequence-Classification)
- Research Paper: "DNA Sequence Classification Research Paper" (https://github.com/NUSRATANANYA/DNA-Sequence-Classification/blob/main/1099_Internship%20Paper(DNA_Sequence_Classification).pdf)
- Notebook: "DNA Sequence Classification Notebook" (https://github.com/NUSRATANANYA/DNA-Sequence-Classification/blob/main/dna-sequence.ipynb)

Work Completed

- Downloaded and examined the DNA sequence dataset from Kaggle.
- Combined and prepared the Human, Chimpanzee, and Dog source files.
- Prepared a combined dataset containing 6,882 records.
- Defined a seven-class gene-family classification task.
- Split the data into training and test sets using an 80:20 stratified split with "random_state=42".
- Represented DNA sequences using k-mer count features for traditional machine-learning models.
- Evaluated SVM using k-mer sizes of 3, 4, 5, and 6.
- Implemented and evaluated four classification models:
  - Multinomial Naive Bayes
  - Support Vector Machine (SVM)
  - XGBoost
  - One-dimensional Convolutional Neural Network (1D CNN)
- Evaluated model performance using accuracy, macro precision, macro recall, macro F1-score, and macro ROC-AUC.
- Compared the models and reviewed class-wise SVM errors.
- Prepared plots for model comparison, k-mer comparison, and class-wise error rates.
- Prepared a research paper describing the methodology, experiments, results, limitations, and future work.

Dataset Summary

- Dataset Source: Kaggle

- Combined Records: 6,882

- Training Records: 5,505

- Test Records: 1,377

- Training/Testing Split: 80:20

- Number of Target Classes: 7

Target Classes

1. G protein-coupled receptor
2. Tyrosine kinase
3. Tyrosine phosphatase
4. Synthetase
5. Synthase
6. Ion channel
7. Transcription factor

Models and Feature Representation

- Multinomial Naive Bayes: k-mer count features

- SVM: k-mer count features (k = 3, 4, 5, and 6)

- XGBoost: k-mer count features

- 1D CNN: One-hot-encoded DNA sequences

Workflow

1. Downloaded and combined the DNA sequence datasets.
2. Cleaned the data and prepared seven gene-family classes.
3. Split the dataset into training (80%) and testing (20%) sets.
4. Extracted k-mer features and performed one-hot encoding.
5. Trained Naive Bayes, SVM, XGBoost, and 1D CNN models.
6. Evaluated model performance using five metrics.
7. Compared the results and generated performance graphs.

Experimental Results

Results on the selected test split:

## Experimental Results

| Model | Accuracy | Macro Precision | Macro Recall | Macro F1-score | Macro ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Naive Bayes | 0.6550 | 0.6701 | 0.6605 | 0.6489 | 0.8765 |
| SVM | 0.9434 | 0.9476 | 0.9420 | 0.9446 | 0.9924 |
| XGBoost | 0.9339 | 0.9533 | 0.9198 | 0.9348 | 0.9964 |
| 1D CNN | 0.8635 | 0.8708 | 0.8440 | 0.8527 | 0.9806 |

Main Findings

1. SVM achieved the highest accuracy (94.34%) and macro F1-score (0.9446) among the evaluated models.
2. XGBoost achieved the highest macro ROC-AUC (0.9964).
3. The SVM experiment using six-mer features performed best among the tested k-mer sizes.
4. These results apply to the selected dataset and test split. Independent external validation has not yet been performed.

Limitations and Future Work

1. The current evaluation uses one dataset and one train/test split.
2. External validation on an independent dataset has not yet been performed.
3. Repeated stratified cross-validation and evaluation on an untouched independent test set would strengthen the findings.
4. Future work could investigate class-specific errors and the biological relevance of important k-mers using appropriate biological annotations.


