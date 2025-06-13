# 📌 Project Title (Phase 1 – Classification Attempt)

**Climate Vulnerability Predictor (Classification Model)**  
*A Supervised Machine Learning Approach to Classify Regional Adaptation Levels Based on Climate Features*

---

## 📄 Description

This project was the **initial supervised learning attempt** to **classify regions into discrete climate adaptation categories** based on 9 climate and agriculture indicators. The goal was to label inputs into fixed classes such as "Low Risk", "Moderate Risk", or "High Risk". We built multiple classification models like **SVM, Decision Tree, Random Forest, and Logistic Regression** using MATLAB.

---

## 🔥 Features Attempted

- Supervised classification pipeline.
- Manual label assignment based on heuristics (e.g., thresholding CO₂, Rainfall).
- Evaluated models using Accuracy, Precision, Recall, and F1-Score.
- Performed Z-score normalization and PCA.
- GUI Input for prediction (Prototype Level).
- Attempted one-hot encoding for nominal values (if present).

---

## 🧪 Input Features

Same 9 indicators as final project:

- Average Temperature  
- Rainfall  
- CO₂ Emissions  
- Crop Yield  
- Extreme Weather Events  
- Irrigation Access  
- Pesticide Use  
- Fertilizer Use  
- Soil Health Index  

---

## 🤖 Models Tested

| Model               | Result / Accuracy |
|---------------------|-------------------|
| Decision Tree       | ~47%              |
| SVM (Linear)        | ~50%              |
| Random Forest       | ~51%              |
| Logistic Regression | ~49%              |

---

## 💥 Why This Approach Failed

Despite testing various classifiers, **none of the models gave reliable accuracy**. Here's why:

1. 🔍 **No Ground Truth Labels**  
   We didn't have real-world labels for what defines "High Risk" vs. "Low Risk" regions. Labels were artificially created using thresholding — which introduced bias and noise.

2. 📉 **Low Class Separability**  
   Visualizations (PCA, t-SNE) showed **high overlap** between classes. This means the features didn't form clean boundaries, which classifiers rely on.

3. ⚖️ **Class Imbalance + Noise**  
   The classes weren't balanced, and the synthetic labeling added ambiguity. Models overfit to noise or predicted the majority class.

4. 🧠 **Lack of Domain Justification**  
   Unlike medical datasets or sentiment analysis, we couldn't explain what made our labeling scheme "right" — which is dangerous in climate modeling.

5. 🌀 **Better Suitability for Clustering**  
   The data seemed more like **continuous adaptation space** rather than distinct buckets. So, **unsupervised learning** made more sense.

---

## 📌 Decision to Pivot

After extensive analysis, we realized:

> “Climate adaptation is better understood as a *continuum* than as discrete classes.”

Hence, we switched to **clustering using UMAP + KMeans/GMM**, which:

- Doesn’t require labels.  
- Finds *natural groups* in data.  
- Works even when boundaries between regions are fuzzy.  

---

## 🛠 Lessons Learned

- Always validate label quality before choosing supervised learning.
- Clustering is great when boundaries are unclear or expert labels are unavailable.
- Visual inspection (via UMAP/PCA) is a **critical pre-modeling step**.

---


---

## 📉 Evaluation Snapshot

```text
Classifier: Random Forest
Accuracy: 21.2%

## 🙌 Credits
- Developed by Leekhith Nunna,
- Amrita Vishwa Vidyapeetham
