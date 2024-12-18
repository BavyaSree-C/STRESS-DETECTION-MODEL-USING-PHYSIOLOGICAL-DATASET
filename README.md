# 🌟 **Stress Detection Using Deep Learning Algorithms** 🌟  

🚀 **STRESS-DETECTION-MODEL-USING-PHYSIOLOGICAL-DATASET**  
> A deep learning-based project to detect stress using physiological signals from the [WESAD Dataset](https://archive.ics.uci.edu/ml/datasets/WESAD+%28Wearable+Stress+and+Affect+Detection%29).  

---

## 📁 **Dataset**  
### **WESAD Dataset**  
- **Source**: [WESAD Dataset](https://archive.ics.uci.edu/ml/datasets/WESAD+%28Wearable+Stress+and+Affect+Detection%29)  
- Contains synchronized physiological signals and labels to analyze emotional states.  
- Data extracted specifically from subject files **S2.pkl** and **S3.pkl**.  

### **Extracted Signals**  
- Chest Accelerometer (**ACC**) in x, y, z axes.  
- Electrocardiogram (**ECG**).  
- Electromyography (**EMG**).  
- Electrodermal Activity (**EDA**).  
- Temperature.  
- Respiration.

---

## 🛠️ **Preprocessing Steps**  
### **Label Segmentation**  
- Differentiated states: `baseline`, `stress`, `amusement`, and `meditation`.  

### **Outlier Detection & Filtering**  
- Applied **Interquartile Range (IQR)** method:  
  - `Lower Bound = Q1 - 1.5 * IQR`  
  - `Upper Bound = Q3 + 1.5 * IQR`  
  - Data outside this range was flagged and removed.  

### **Data Normalization**  
- Standardized signals for consistent ranges and improved model performance.  

### **Label Distribution**  
- Verified counts of samples across different emotional states.  

---

## 📊 **Data Transformation & Feature Engineering**  
1. **Correlation Analysis**  
   - Explored relationships among features like `EDA`, `ACC`, `Temperature`.  
2. **Segmentation by Emotional State**  
   - Organized data by states for targeted analysis and visualization.  
3. **Final Output**  
   - Saved processed data in **CSV format** for modeling.  

---

## 💻 **Modeling Approaches**  
### **Approach 1 - Raw Data**  
- Basic preprocessing only, used as a baseline.  

### **Approach 2 - Autoencoder Compression**  
- Compressed and encoded the dataset using an autoencoder.  

### **Approach 3 - SMOTE + Standardization**  
- Balanced dataset with **SMOTE** to improve detection of minority classes.  

---

## 🧠 **Deep Learning Models Implemented**  
1. **LSTM (Long Short-Term Memory)**  
   - Captures temporal dependencies for stress detection.  

2. **Attention-Based LSTM**  
   - Enhances focus on significant features in sequences.  

3. **Transformer Model**  
   - Leverages **self-attention** for long-range dependency analysis.  

---

## 📚 **References**  
1. [Schmidt, P. et al. (2018)](https://dl.acm.org/doi/10.1145/3242969.3242985) - WESAD Dataset Overview.  
2. [Nigam, K. et al. (2021)](https://eudl.eu/doi/10.4108/eai.14-5-2021.169919) - Improved Stress Detection Approach.  
3. [Fang, R. et al. (2022)](https://ieeexplore.ieee.org/document/9995121) - Over-fitting and Redundancy Prevention.  
4. [Liapis, A. et al. (2021)](https://www.mdpi.com/2079-9292/10/13/1550) - Advancing Stress Detection.  
5. [Stržinar, Ž. et al. (2023)] - Frequency Spectrum Analysis for Stress Detection.  
6. [Garg, P. et al. (2021)](https://dl.acm.org/doi/10.1145/3397482.3450732) - Stress Detection with Wearables.  

---

