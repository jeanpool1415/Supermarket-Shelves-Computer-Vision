# Supermarket-s-Shelves

# Supermarket Shelf Product Identification using Computer Vision

## Project Purpose and Goals

Retail suppliers face challenges in ensuring that their products are correctly placed on supermarket shelves according to contractual agreements. Traditionally, this process requires manual verification, leading to high operational costs.

This project develops an AI-powered system that detects and highlights similar products on shelves using computer vision. By automating product monitoring through images, suppliers can remotely verify placement without deploying personnel, ensuring compliance with shelf space agreements.

## Dataset
The model was fine-tuned using SKU-110K, a dataset containing 110,000 images of store shelves with dense product arrangements.

## Methodologies Used
- Object Detection: YOLOv10 was fine-tuned for product identification (10 epochs, initial proof-of-concept).
- Feature Extraction: A combination of CLIP, DINOv2, and ResNet-18 (equal weighted embeddings) was used due to a lack of labeled data.
- Clustering: HDBSCAN was applied to group similar products, assigning unique colors for differentiation.

## Key Findings
High-quality images improve accuracy, while cluttered shelves pose challenges.
Simple product designs are easier to recognize than those with intricate details.
Combining multiple feature extractors improved product grouping, but fine-tuning is needed for better separation.

## Limitations and Improvements
Lack of labeled data prevents full model fine-tuning.
Clustering precision can be improved with contrastive learning.
Next Steps: Implement self-supervised learning to enhance embeddings and develop a user-friendly dashboard for suppliers to upload images and receive insights.
