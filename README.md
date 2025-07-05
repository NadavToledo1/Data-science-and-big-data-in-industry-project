# 🧠 Skin Cancer Detection with Multimodal Deep Learning

## 👨‍🔬 Project by:
- Nadav Toledo  
- Niv Shifrin  
- Eyal Shubeli  

---

## 📌 Overview

Skin cancer, particularly **melanoma**, is one of the most dangerous cancers globally, with over **350,000 new cases** diagnosed last year. Early detection is critical — when caught early, melanoma has a **>95% survival rate**. However, long specialist wait times and limited access to dermatology expertise delay diagnosis, increasing the risk of metastasis and death.

This project presents an **AI-based solution** that leverages **dermoscopic images and structured metadata** to detect skin cancer more efficiently and accurately, supporting medical professionals with early diagnosis.

---

## 🎯 Objectives

- Improve **early melanoma detection** using AI.
- Combine **visual and structured patient data** to enhance diagnostic performance.
- Reduce false negatives and unnecessary biopsies.
- Create a scalable, real-world clinical decision support tool.

---

## 🗃️ Data

Provided by the [International Skin Imaging Collaboration (ISIC)](https://www.isic-archive.com/), the dataset includes:

- **3D whole-body images**
- **Dermoscopy tiles** (15x15 mm cropped lesion images)
- **Structured metadata**, including:
  - Patient information (age, gender, location)
  - Image metadata (capture conditions)
  - Diagnostic labels
  - Lesion geometry
  - Color & texture features

---

## 🔧 Data Preparation

- **Image Processing**: Normalized and resized.
- **Metadata Pipeline**: Handled missing values, encoded categorical features, and scaled numerical features.
- **Class Distribution**: Maintained across training, validation, and test sets.

---

## 🧪 Baseline Models

To benchmark performance, we developed three separate models:
1. **Image-only CNN**
2. **Metadata-only XGBoost**
3. **Combined features with XGBoost**

---

## 🧠 Main Model – Multimodal Deep Neural Network

We designed a custom architecture that:
- Combines image embeddings with structured metadata.
- Learns joint feature representations.
- Uses **class weighting**, **dropout**, and **early stopping** to manage imbalance and prevent overfitting.
- Applies **threshold optimization** to maximize **Balanced Accuracy**.

---

## 📊 Results

| Model Type              | AUC  | Balanced Accuracy | Recall(Class 1) |
|------------------------|------|-------------------|--------|
| Image-only             | 0.8071 | 0.7324              | 0.6456   |
| Metadata-only          | 0.9294 | 0.6806              | 0.3671   |
| Combined (XGBoost)     | 0.935 | 0.6314              | 0.2658   |
| **Multimodal DL (Main)**| **0.8516** | **0.7935**         | **0.7468** |

> ⚠️ **Key Insight**: AUC alone is not sufficient in imbalanced medical data. Balanced Accuracy and Recall provide a more realistic view of model performance in clinical settings.

---

## 🔍 Error Analysis

- The **Multimodal Deep Learning model** showed the best overall performance across all key metrics.
- It outperformed all baselines and provided the **best balance between false negatives and false positives** — critical in medical diagnostics.
- Demonstrated that **synergy between visual and metadata features** captures deeper patterns than either input alone.

---

## ⚖️ Legal & Ethical Considerations

- AI used as a **decision support tool**, not a replacement for physicians.
- Current **liability frameworks** do not fully support autonomous diagnosis.
- Regulatory bodies (e.g., FDA) approve AI tools only in **assistive roles** for now.

---

## 🚀 Industry Context & Relevance

Recent developments include:
- **DermaSensor (2024)**: First FDA-approved AI tool for primary care skin cancer detection.
- **Fraunhofer Full-Body Scanner (2025)**: 6-minute automated assessment system.

Our project aligns with this technological shift and demonstrates a viable path toward more **accessible, scalable, and accurate skin cancer screening**.

---

## ✅ Conclusion

This project:
- Successfully built a **multimodal deep learning model** for melanoma detection.
- Validated the approach with strong results and meaningful clinical metrics.
- Highlighted the value of combining **structured and unstructured data**.
- Offers a **promising proof of concept** for real-world deployment in primary care and teledermatology.

---

## 📂 Project Structure

├── EDA

├── ProjectNotebook

├── Presentation

├── README


---

## 🤝 Acknowledgements

This work would not have been possible without the **International Skin Imaging Collaboration (ISIC)** and its open dataset initiative. We are grateful for their efforts in advancing AI-assisted dermatology.

---

