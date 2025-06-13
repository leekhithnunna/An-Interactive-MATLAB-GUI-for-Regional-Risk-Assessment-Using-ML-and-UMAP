# An-Interactive-MATLAB-GUI-for-Regional-Risk-Assessment-Using-ML-and-UMAP
The tool is a MATLAB-based interactive GUI that uses standardization, UMAP, and clustering techniques to predict regional climate adaptation capacity, allowing users to input climate and agricultural indicators and visualize vulnerability and adaptation potential.

# 🌍 Climate Adaptation Cluster Predictor

> A MATLAB GUI-based application that predicts regional climate vulnerability clusters using machine learning and UMAP dimensionality reduction.

---

## 🔥 Features

- ✅ **User-Friendly GUI** built with App Designer.
- 📊 **9 Key Climate Indicators** (like Temperature, Rainfall, CO₂, Crop Yield, etc.).
- 🔁 **Data Standardization** for fair model input.
- 📉 **UMAP for 9D → 2D Projection** with visual feedback.
- 🧠 **Clustering Models**: KMeans and GMM for robust predictions.
- 📍 **Interactive Visualization** using Stanford’s UMAP Viewer (v4.4).
- 💡 **Cluster Insights** for risk-level interpretation.
- ⚠️ Handles common errors: input validation, dimension mismatches, etc.

---

## 🧪 Dataset Input Fields

| Field Name                  | Description                                |
|----------------------------|--------------------------------------------|
| `Average_Temperature_C`    | Mean regional temperature in Celsius       |
| `Total_Precipitation_mm`   | Annual rainfall in mm                      |
| `CO2_Emissions_MT`         | Carbon emissions in metric tons            |
| `Crop_Yield_MT_per_HA`     | Crop productivity per hectare              |
| `Extreme_Weather_Events`   | Count of weather disasters                 |
| `Irrigation_Access_`       | Percentage access to irrigation (0–10)     |
| `Pesticide_Use_KG_per_HA`  | Pesticide application rate                 |
| `Fertilizer_Use_KG_per_HA` | Fertilizer use per hectare                 |
| `Soil_Health_Index`        | Soil quality index (0–100)                 |

---

## 🚀 How It Works

1. 🧾 User enters values for 9 climate/agri indicators in the GUI.
2. 📐 Inputs are normalized using the training mean (`mu`) and std (`sigma`).
3. 🧠 Data is passed through the trained `KMeans` or `GMM` model.
4. 🔍 UMAP transforms 9D → 2D for visual cluster placement.
5. 🧭 Cluster index is displayed + visual feedback is shown on UMAP plot.
6. ✅ Final checklist confirms input sanity and model confidence.

---

## 🧠 Models Used

- **UMAP (Uniform Manifold Approximation and Projection)**  
  `→` For nonlinear dimensionality reduction from 9D to 2D.
- **KMeans & GMM**  
  `→` For unsupervised climate vulnerability clustering.
- **Standardization**  
  `→` Inputs are normalized before clustering.

---

## 🛠 Requirements

- MATLAB R2021b or newer
- UMAP Toolbox (included: `run_umap.m`)
- Statistics and Machine Learning Toolbox
- App Designer support (for GUI apps)
- Java enabled (for UMAP GUI viewer)

---

## 🧑‍💻 Usage

1. Open `ClimatePredictor.mlapp` in MATLAB.
2. Click **Run** ▶️
3. Fill in the input fields.
4. Click **Predict Cluster**
5. Explore the UMAP visualization.
6. Done 🎉

---

## ⚠️ Common Errors

| Error Message                        | Fix                                                   |
|-------------------------------------|--------------------------------------------------------|
| "Invalid input in ..."              | Input must be numeric and non-empty.                  |
| "Cannot retrieve the java frame..." | Make sure GUI is fully initialized before calling UMAP.|
| "Not enough input arguments"        | Pass `app` as argument to `final_checklist(app)`       |

---

## 📌 Acknowledgements

- 💻 UMAP by [Leland McInnes et al.](https://github.com/lmcinnes/umap)
- 🧪 MATLAB adaptation: [Herzenberg Lab, Stanford University]
- 🎨 GUI and logic by Leekhith Nunna (Amrita Vishwa Vidyapeetham)

---

## 📄 License

MIT License — free to modify and use for academic and research purposes.

---

## 🙌 Contributing

Feel free to open an issue or PR if you'd like to:
- Improve clustering logic
- Add more features to the GUI
- Optimize for different datasets (e.g., other countries)

---

## 📬 Contact

**Leekhith Nunna**  
📧 `leekhithnunna1269@gmail.com`  
📍 Amrita Vishwa Vidyapeetham  
🔗 [GitHub](https://github.com/leekhithnunna)

---
