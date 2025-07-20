# 👗 Fashion Product Attribute Prediction (Multi-Output Image Classification)

A deep learning project using **EfficientNetB0** to classify fashion product images into multiple attributes: **gender**, **article type**, **base color**, and **season**. The model is trained on the **Fashion Product Images Dataset** from Kaggle.

---

## 📌 Project Summary

| Component           | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| 🧠 Model             | Transfer learning using EfficientNetB0                                 |
| 🎯 Task              | Multi-label classification of product attributes                       |
| 📊 Attributes        | `gender`, `articleType`, `baseColour`, `season`                        |
| 📁 Dataset Source    | [Kaggle - Fashion Product Images](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset) |

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Sudeep2411/Fashion_product.git
cd Fashion_product
```

### 2️⃣ Create Virtual Environment
```bash
python -m venv venv
```

### 3️⃣ Activate Virtual Environment
- Windows:
```bash
venv\Scripts\activate
```
- macOS/Linux:
```bash
source venv/bin/activate
```

### 4️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 📁 Project Structure

```
Fashion_product/
├── models/
│   ├── final_fashion_model.h5       # Trained model
│   ├── label_encoders.pkl           # Encoded dictionaries for all labels
│   ├── metadata.json                # Mapping for labels to categories
│   └── training_log.csv             # Training/validation logs
│
├── notebook/
│   └── fashion-styles.ipynb         # Main notebook (EDA + model training)
│
├── screenshots/
│   ├── screenshot1.png
│   ├── screenshot2.png
│   └── screenshot3.png              # Visuals from testing/demo
│
├── requirements.txt                 # Python package dependencies
└── README.md                        # Project documentation
```

---

## 📊 Dataset Overview

| Field         | Description                          |
|---------------|--------------------------------------|
| ID            | Image file name                      |
| Gender        | Men, Women, Boys, Girls, Unisex      |
| Base Colour   | Primary color of the product         |
| Article Type  | Jeans, T-Shirts, Shoes, etc.         |
| Season        | Summer, Fall, Winter, Spring         |

- Images: 44,000+
- Format: `.jpg`
- Metadata: `styles.csv`

> Make sure to download and extract the dataset from Kaggle before training:
> [Fashion Product Images Dataset](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset)

---

## 🧠 Model Overview

- **Architecture**: EfficientNetB0 (pretrained on ImageNet)
- **Input Size**: 224x224x3
- **Training Strategy**:
  - Custom head for 4 outputs
  - Categorical Cross-Entropy losses for each output
  - Early stopping + learning rate scheduler
- **Output Labels**:
  - 4 heads: gender, articleType, baseColour, season

---

## ✅ Model Evaluation

| Attribute      | Accuracy |
|----------------|----------|
| Gender         | 96.2%    |
| Base Colour    | 84.5%    |
| Article Type   | 89.3%    |
| Season         | 79.8%    |

- Metrics: Accuracy per attribute + multi-output loss
- Evaluated on unseen test set
- Tested also on Amazon screenshots (qualitative testing)

---

## 📌 Key Features

- 🔍 Image preprocessing pipeline using OpenCV
- 📊 Encoded categorical metadata
- 💾 Saved model and label encoders for reuse
- 📈 Training history visualized and saved

---

## 🛠️ Tools & Libraries

| Tool            | Purpose                         |
|-----------------|----------------------------------|
| Python 3.8+     | Core language                   |
| TensorFlow/Keras| Deep learning model             |
| scikit-learn    | Label encoding + metrics        |
| OpenCV          | Image preprocessing             |
| Pandas, NumPy   | Data manipulation               |
| Matplotlib      | Data visualization              |

---

## 🙌 Acknowledgments

- [Kaggle Dataset](https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset)
- [EfficientNet Paper](https://arxiv.org/abs/1905.11946)
- TensorFlow/Keras community

---

## 📜 License

This project is licensed under the **MIT License**.
