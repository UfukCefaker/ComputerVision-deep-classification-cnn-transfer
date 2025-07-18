# ComputerVision-deep-classification-cnn-transfer


---

## 🧠 Models Implemented

### 🔹 SimpleCNN
- 5 convolutional blocks
- 2 fully connected layers
- Optional dropout (0.3 and 0.5)

### 🔹 ResidualCNN
- Based on SimpleCNN
- Additional residual blocks after Conv2 and Conv4

### 🔹 MobileNetV2 (Transfer Learning)
- Scenario 1: Only final FC layer trained
- Scenario 2: Last two convolutional blocks + FC layer fine-tuned

---

## 🔧 Training Settings

- Optimizer: Adam
- Loss: CrossEntropyLoss
- Epochs: 50
- Learning rates: 0.0001 / 0.001 / 0.005
- Batch sizes: 32 / 64

---

## 📊 Results Summary

| Model              | Val Accuracy | Test Accuracy |
|-------------------|--------------|----------------|
| SimpleCNN          | 58.91%       | 50.91%         |
| ResidualCNN        | 63.27%       | 50.18%         |
| MobileNetV2 (S1)   | 88.00%       | 74.91%         |
| MobileNetV2 (S2)   | **90.18%**   | **79.27%**     |

---

## 📈 Key Insights

- Transfer learning with MobileNetV2 dramatically outperformed scratch CNNs.
- Fine-tuning deeper layers (Scenario 2) improved test accuracy.
- Dropout rate of 0.3 helped generalization in both custom CNNs.
- Residual connections improved validation accuracy, but not test generalization.

---

## 👨‍💻 Author

**Ufuk Cefaker**  
Computer Vision Lab - Hacettepe University  
Student ID: 2220356171

---

## 📄 Report

You can find the full detailed report [here](./report.pdf).

