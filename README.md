# Waste Classification using Transfer Learning

## Problem Statement
This project aims to develop an automated waste classification system using machine learning techniques. The goal is to accurately categorize waste items into organic and recyclable classes, addressing the critical environmental challenge of waste management.

## Dataset
The dataset used for this task consists of images of various waste items, categorized into two classes: organic and recyclable. 
- **Source**: [Waste Classification Data on Kaggle](https://www.kaggle.com/datasets/techsash/waste-classification-data)
- **Size**: Large dataset with 22,564 training images and 2,513 test images.
- **Relevance**: Highly relevant to the mission of improving waste management and recycling efforts.
- **Type**: Image dataset, suitable for computer vision tasks.
- **Classes**: Two classes - Organic and Recyclable

This dataset provides a diverse collection of waste item images, making it ideal for training models to distinguish between recyclable and organic waste.

## Evaluation Metrics
The following metrics were used to assess the performance of our fine-tuned models:

1. **Accuracy**: Measures the overall correctness of the model's predictions.
2. **Loss**: Indicates the model's prediction error (lower is better).
3. **Precision**: Measures the accuracy of positive predictions.
4. **Recall**: Measures the model's ability to find all positive instances.
5. **F1 Score**: Harmonic mean of precision and recall, providing a balanced measure of the model's performance.


## Model Comparison

| Model       | Accuracy | Loss   | Precision | Recall | F1 score |
|-------------|----------|--------|-----------|--------|----------|
| VGG16       | 0.8623   | 0.4336 | 0.4635    | 0.3768 | 0.4157   |
| ResNet50    | 0.6717   | 2.0066 | 0.4466    | 0.3498 | 0.3923   |
| DenseNet121 | 0.9180   | 0.2871 | 0.4423    | 0.3795 | 0.4085   |

![image](https://github.com/user-attachments/assets/398f8e5a-f7ad-4ca6-8cf8-c0f6a2a2da52)


## Findings and Discussion

### Strengths of Transfer Learning
1. **Improved Performance**: All models achieved good accuracy, with DenseNet121 performing exceptionally well at 92.75% accuracy on the test set.
2. **Reduced Training Time**: By using pre-trained models, we significantly reduced the time and computational resources required for training.
3. **Generalization**: The models, especially DenseNet121, showed good generalization to the waste classification task despite being pre-trained on a different dataset.

### Limitations
1. **Model-Specific Performance**: Not all pre-trained models performed equally well. ResNet50, for instance, struggled with this specific task.
2. **Fine-tuning Challenges**: Finding the right balance of frozen and trainable layers, as well as optimal learning rates, required experimentation.
3. **Potential Overfitting**: Some models showed signs of overfitting, suggesting a need for more robust regularization techniques.

### Conclusion
Transfer learning proved highly effective for our waste classification task, with DenseNet121 emerging as the best-performing model. This approach allowed us to leverage complex architectures and pre-learned features to achieve high accuracy in our specific domain, demonstrating the power of transfer learning in addressing real-world environmental challenges.
