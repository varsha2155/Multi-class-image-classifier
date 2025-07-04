# 🧠 Multi-Class Image Classification with Semi-Supervised Learning

A complete image classification pipeline using **ResNet-18** and **semi-supervised learning**, built from scratch to tackle a 10-class image classification problem using only labeled and unlabeled image data.

---

## 📌 Objective

The goal of this project was to build an **efficient, accurate multi-class image classifier** under strict constraints:

- Phase 1: Train only on labeled image data
- Phase 2: Improve results using unlabeled data via **semi-supervised learning**
- Use only the **ResNet-18** architecture throughout
---

## 🧠 Approach

### 🟦 Phase 1 – Supervised Learning
- Model: `torchvision.models.resnet18`
- Training exclusively on labeled images
- Used data augmentations, learning rate scheduler, and Adam optimizer
- Achieved **92.68% training accuracy** after 15 epochs

📈 Accuracy Progress:
Epoch [1/15] | Accuracy: 18.29%
Epoch [10/15] | Accuracy: 69.92%
Epoch [15/15] | ✅ Final Accuracy: 92.68%


### 🟧 Phase 2 – Semi-Supervised Learning
- Used pseudo-labeling on unlabeled images
- Retained only predictions with high confidence (probability > 0.9)
- Combined labeled + pseudo-labeled data for re-training
- Produced significantly improved generalization on unseen test images

---

## 📂 Project Files

| File                          | Description                                |
|------------------------------|--------------------------------------------|
| `ResNet18_Solution.ipynb`    | Complete Colab notebook with all code      |
| `phase1_predictions.csv`     | Predictions using labeled data only        |
| `phase2_predictions.csv`     | Predictions using semi-supervised training |
| `README.md`                  | Project overview and documentation         |

---

## 🔧 Environment & Tools

- Python 3.10+
- PyTorch + torchvision
- PIL, pandas, numpy
- Google Colab for training and testing
- Confidence thresholding + pseudo-labeling

---

## ✨ Key Highlights

- ✅ ResNet-18 used in both phases
- 🧠 Pseudo-labeling strategy carefully implemented with softmax + confidence filter
- 📊 Final outputs match the exact format required for evaluation
- 🧹 Code is modular, reproducible, and designed for easy experimentation

---

## 🙋‍♀️ Author

**Varsha S**  
🎓 Final Year AI & Data Science  
📫 Email: varsha2155@gmail.com  
🌐 [GitHub](https://github.com/varsha2155)  

---

## 📁 Future Improvements

- Use other SSL techniques like FixMatch or MixMatch
- Hyperparameter tuning via grid search or Optuna
- Try ResNet-34 and compare generalization performance

---

## 📝 License

This project is open-source and for academic and learning purposes only.

