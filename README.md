## EnvironNet- A Trash Image Classification Project

Building a **Custom Convolutional Neural Network (CNN)** to classify trash images into **10 categories**:
**shoes, battery, trash, clothes, plastic, paper, metal, glass, cardboard, biological.**

1. **Dataset Preparation**

   * Each class has **1000 images**.
   * The dataset is split into **Train, Validation, and Test** sets.
   * Data augmentation (rotation, flips, color jitter, etc.) is applied **only to the training set** to improve generalization.
   * Validation and Test sets use the **original images** only (no augmentation).

2. **Model Architecture**
   * Input: **224×224 RGB images**.
   * CNN layers with **Conv → ReLU → BatchNorm → MaxPool**.
   * Fully connected layers with **Dropout** for regularization.
   * Output: **10 softmax probabilities** (multi-class classification).

3. **Training Setup**

   * **Loss Function**: CrossEntropyLoss.
   * **Optimizer**: Adam with learning rate **0.001** and **L2 weight decay**.
   * **Scheduler**: ReduceLROnPlateau to lower learning rate when validation loss stops improving.
   * **Regularization**: Dropout (0.5) + Weight Decay (1e-4).
   * **EarlyStopping** is used to avoid overfitting.

---

## 📊 Evaluation Reports

1. **Accuracy** (Train, Validation, Test)
2. **Loss curves** (Training vs Validation loss across epochs)
3. **Accuracy curves** (Training vs Validation accuracy across epochs)
4. **Classification Report** (Precision, Recall, F1-score per class)
5. **Confusion Matrix** (which classes are being confused)
6. **Inference examples** (show a few test images with predicted labels + confidence)
