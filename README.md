# Product Image Classification for E-commerce

## Overview

This project focuses on classifying fashion product images into e-commerce categories using deep learning. The goal is to help online stores automatically organize product images, improve product tagging, and make product search faster and more consistent.

## Team Members

* Fares Samara - 20220553
* Bassam Aljazaeri - 20220547

## Project Idea

Online stores usually contain thousands of product images. Manually organizing these images is slow and may cause mistakes. This project uses image classification to automatically predict the product category from an input image.

## Dataset

The project uses the Fashion Product Images (Small) dataset from Kaggle.

Dataset link:
https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-small

## Classes

The original project scope included:

* Accessories
* Bags
* Clothing
* Shoes

In the final executed Milestone 3 notebook, the evaluated classes were:

* Accessories
* Clothing
* Shoes

## Model

The final selected model is MobileNetV2 with transfer learning.

The model uses:

* MobileNetV2 pretrained on ImageNet
* Input image size: 224 x 224 x 3
* Data augmentation: random flip, rotation, zoom, and contrast
* Classification head: GlobalAveragePooling, Dense layer, Dropout, and Softmax
* Fine-tuning with a small learning rate

## Results

The final MobileNetV2 model achieved:

| Metric             | Score  |
| ------------------ | ------ |
| Test Accuracy      | 98.93% |
| Weighted Precision | 98.94% |
| Weighted Recall    | 98.93% |
| Weighted F1-score  | 98.93% |

## Demo

The notebook includes an inference function:

```python
predict_product_image(image_path)
```

This function takes a product image path, preprocesses the image, runs the trained model, and returns:

* Predicted class
* Confidence score
* Class probabilities

## Files in This Repository

```text
Product-Image-Classification-for-Ecommerce/
│
├── project pattern (2).zip
└── README.md
```

## Technologies Used

* Python
* TensorFlow / Keras
* MobileNetV2
* KaggleHub
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

## How to Run

1. Download or clone this repository.
2. Extract the ZIP file.
3. Open the notebook file in Google Colab or Jupyter Notebook.
4. Run the cells from top to bottom.
5. Make sure the Kaggle dataset is available.
6. Use the prediction function to test a new product image.

## Conclusion

This project shows that transfer learning is effective for product image classification. MobileNetV2 achieved strong results and performed better than the baseline CNN model. The project includes training, evaluation, confusion matrix analysis, prediction examples, and a notebook-based demo.
