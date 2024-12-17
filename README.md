# Assignment 1 - Simplified Custom Object Detection

This assignment is designed for the **Deep Network Development** course and focuses on creating, training, and evaluating a **custom object detection model** while comparing its performance with an existing fine-tuned model (e.g., YOLO).

---

## Task Description

Your task involves developing a simplified object detection model where each image contains only a single object. The workflow includes synthetic dataset creation, model development, evaluation, and comparison with an existing object detection model.

### **Specific Tasks**

#### 1. **Dataset Creation**
   - Select at least **3 objects** (avoid offensive, inappropriate, and violent objects).
   - Remove the background from the chosen objects, ensuring only the object remains.
   - Collect background images from different locations and scenarios.
   - Generate a synthetic dataset by:
     - Randomly inserting one object into a background image at a random location.
     - Saving the coordinates of the inserted objects to create bounding boxes.
   - Format the bounding boxes appropriately for training (e.g., `[x,y,w,h]` or YOLO format).
   - Implement a **PyTorch Dataset class** to manage the dataset.
   - Split the dataset into **training**, **validation**, and **test** sets.

#### 2. **Model Development**
   - Design a **Convolutional Neural Network (CNN)**-based architecture for object detection.
     - Include a backbone for **feature extraction**.
     - Add two output branches:
       - **Class probabilities**: Equal to the number of chosen objects.
       - **Bounding box regression**: Output size of 4 for the coordinates.
   - Experiment with:
     - Different layers and hyperparameters.
     - Regularization techniques to improve generalization.
   - Define an optimizer, loss function, and set the number of training epochs.
   - Optimize both **classification** and **bounding box regression** losses.
   - Choose at least **3 evaluation metrics**:
     - Examples: Precision, Recall, F1-score, mAP.
   - Visualize performance metrics and model predictions.

#### 3. **Existing Model Comparison**
   - Load an existing object detection model (e.g., YOLO).
   - Fine-tune the model on your synthetic dataset.
   - Monitor and visualize **losses** and **evaluation metrics** during fine-tuning.
   - Compare the performance of the **custom model** and the **fine-tuned existing model**.
   - Visualize predictions from both models and explain any observed differences.
   - Provide insights into potential improvements for the custom model.

---

## Guidelines

- Follow the sections provided in the notebook to guide your implementation but adapt as needed.
- **Read all instructions carefully** to ensure all requirements are met.
- Avoid using external Python files. **All code should be contained within the notebook**.
- Do **not upload** the dataset or model weights.
- Include the following details at the beginning of your notebook:
  - **Name**
  - **Neptun ID**
  - **Network details**
  - **Chosen objects**
- Add **explanations** throughout your code and results section, detailing:
  - Your design choices.
  - Observations.
  - Potential improvements.

---

## Defense Preparation

Prepare answers to the following example questions:

1. **What is object detection?**
2. **What are the key components of a CNN architecture commonly used in object detection?**
3. **How does data augmentation improve the performance of an object detection model?**
4. **Describe the role of anchor boxes in object detection algorithms such as YOLO and SSD.**
5. **Explain the difference between localization and classification in object detection.**
6. **How do you evaluate the performance of an object detection model? Mention common metrics.**
7. **What are the challenges of training a custom object detection model, and how can they be addressed?**
8. **What is transfer learning, and how can it be applied in fine-tuning pre-trained models?**
9. **What techniques prevent overfitting in object detection models? Why are they important?**
10. **Discuss the trade-offs between speed and accuracy when selecting an object detection model for real-time applications.**



