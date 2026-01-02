Skin Cancer Classification using CNN & Transfer Learning

This project builds an end-to-end pipeline to classify different types of skin cancer from clinical images using deep learning. The focus was on creating a reliable, reproducible workflow while handling real dataset challenges such as patient leakage and severe class imbalance.

🔍 Objective

Classify skin cancer images into multiple diagnostic classes using deep learning and evaluate the model fairly and robustly.

📂 Dataset

Real clinical image dataset (DERM12345)

Metadata-driven processing

Patient-wise split to avoid leakage

Separate Train / Validation / Test sets

🧠 Approach
1️⃣ Data Handling

Cleaned metadata and grouped relevant diagnostic classes

Implemented patient-wise splitting to avoid the same patient appearing in multiple sets

Created reproducible PyTorch dataset and dataloaders

2️⃣ Handling Class Imbalance

Used class-weighted loss

Applied targeted data augmentation for minority classes
→ Result: Improved recall and stability on under-represented cancer types

3️⃣ Model Development

Two model pipelines were developed and evaluated:

Custom CNN

ResNet-18 (Transfer Learning)

Training strategy:

Monitored validation performance

Saved best checkpoint

Reduced overfitting using augmentation + weighted learning

4️⃣ Evaluation

Measured:

Per-class Precision, Recall, F1

Confusion Matrix

Misclassification analysis

Exported structured performance reports

→ Result: ResNet-18 provided better generalization and more consistent performance across classes.
