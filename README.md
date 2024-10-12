# PushPin Detection and Classification

## Objective

The goal of this project is to develop a quality control visual inspection system that can automatically determine if a box of push pins is acceptable or should be rejected. The system will utilize object detection to identify and classify good and bad pins, enabling automated inspection based on visual data.

## Problem Statement

You are tasked with building an AI-based quality control system for a company that manufactures push pins. Each box contains 15 bins, with exactly one good pin per bin. Your objective is to create a visual inspection system that detects and classifies pins into different categories. Based on the classification, the box will either be accepted or rejected.

## Classes

- **Good Pins**: Pins that meet quality standards.
- **Bad Pins**: Pins that do not meet quality standards.

## Data Preparation

### Original Dataset

The dataset consists of a total of 310 images, categorized as follows:

- **Good Pins**: 138 images
- **Bad Pins**: 172 images

Each image is prefixed with either "good" or "bad" to facilitate easy differentiation.

### Data Preparation

![image](https://github.com/user-attachments/assets/46e7586c-9df2-4264-b1b1-8cde811f419f)


### Data Augmentation

To enhance the model's robustness, various data augmentation techniques were applied:

**External Augmentation:**
- Horizontal and Vertical Flips
- Bounding Box Exposure Adjustment: Between -10% and +10%

**Internal Augmentation:**
- Blurring (Gaussian Blur, Median Blur)
- Color Adjustments (To Grayscale, CLAHE)

### Dataset Split Post-Augmentation

![image](https://github.com/user-attachments/assets/e4bee04d-d3cf-4c24-902c-bdb4d5f11c8d)

## Steps
- Benchmark Models: Compare the performance of YOLOv8 and YOLOv11 on the prepared dataset.
- Train the Object Detection Model: Select the best-performing model and train it using the prepared dataset.
- Evaluate Performance: Assess the model’s performance on validation data to ensure accuracy and reliability.
- Logic for Acceptance or Rejection: Implement a decision-making logic to classify boxes as acceptable or rejectable based on the model’s predictions on the test dataset.

## Conclusion

This project aims to streamline the quality control process for push pins, improving efficiency and reducing human error in inspections. By leveraging AI for visual inspection, the system will enhance overall product quality and ensure customer satisfaction.
