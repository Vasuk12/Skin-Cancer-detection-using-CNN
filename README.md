Skin Cancer Classification using Deep Learning
Overview

This project develops an end-to-end deep learning pipeline to classify different types of skin cancer from clinical images. The focus is on building a reliable and reproducible workflow while addressing real dataset challenges such as class imbalance, patient-level data leakage, and fair evaluation.

Dataset and Preparation

The dataset consists of real clinical skin cancer images along with metadata. The data was cleaned and diagnostic classes were organized meaningfully. A patient-wise split was implemented to ensure that images from the same patient never appear across training, validation, and test sets, preventing leakage and providing an unbiased evaluation setup.

Handling Class Imbalance

The dataset contained significant class imbalance, where certain cancer types had far fewer samples. This was addressed using class-weighted loss during training along with targeted data augmentation applied more heavily to minority classes. These techniques improved recall and stability for under-represented cancer categories and prevented the model from biasing toward majority classes.

Model Development

Two model pipelines were created and compared. The first used a custom CNN designed specifically for the dataset. The second approach used transfer learning with ResNet-18, fine-tuned on the dataset to leverage pretrained feature representations. Both models were trained using a structured training workflow with reproducible data loaders, monitored validation metrics, and automatic saving of the best-performing checkpoints. ResNet-18 demonstrated better generalization and reduced overfitting compared to the custom CNN.

Evaluation and Results

Model performance was evaluated using detailed per-class precision, recall, and F1-score, along with confusion matrices and misclassification analysis instead of relying only on overall accuracy. This helped identify performance differences across cancer categories and provided insights into failure patterns. Structured outputs, including reports and visualizations, were generated to validate and analyze the results. The final outcome was a robust classification pipeline with fair evaluation and improved performance on minority cancer classes.

Summary

This project demonstrates the design of a practical and reliable deep learning system for medical image classification. It emphasizes correct data handling, responsible evaluation, and engineering discipline rather than only achieving a single performance metric. The work provides a strong base for future extensions such as deployment, ONNX export, performance benchmarking, or integration into clinical workflows.
