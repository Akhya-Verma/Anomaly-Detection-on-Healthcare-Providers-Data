 # 🏥 Unsupervised Anomaly Detection on Healthcare Providers Data
This project applies unsupervised machine learning techniques to detect anomalies (e.g., fraud or unusual billing patterns) in Medicare healthcare providers’ data.
By leveraging Autoencoders for anomaly detection, the system identifies providers whose financial or service-related data significantly deviates from normal patterns. This can assist in fraud detection, compliance monitoring, and improving data quality in healthcare.

---
## 🚀 Features
# Data Cleaning & Preprocessing:
- Handled missing values and non-numeric entries
- Applied Label Encoding for categorical variables
- Normalized numerical data using MinMaxScaler and StandardScaler
- Reduced skewness and imbalance in feature distributions

# Outlier Detection Techniques Implemented
- Z-Score Method
- IQR Method
- Winsorization
- Autoencoder-based Anomaly Detection (final model)

# Anomaly Detection Models Explored:
- Isolation Forest – for partition-based anomaly detection.
- DBSCAN – for density-based clustering and outlier detection.
- KNN (Unsupervised Adaptation) – for distance-based anomaly scoring.
- Autoencoders (Final Model) – selected for their ability to learn compressed representations and reconstruct normal patterns effectively.


# Visualization & EDA
- Boxplots, scatter plots, distribution plots
- Correlation heatmap for feature relationships
- Bubble plots and animated scatter plots for anomaly visualization
- Funnel charts comparing different outlier detection methods

  
# Anomaly Detection with Autoencoders
- Trained an unsupervised Autoencoder model to reconstruct healthcare provider data
- Reconstruction error used as anomaly score
- High-error samples flagged as anomalies
  
# Interactive Input
- Users can input provider details (e.g., Medicare amounts, number of beneficiaries, gender)
- The model predicts whether the entry is anomalous or non-anomalous
  
# TF-IDF Analysis
 - Text data (e.g., HCPCS descriptions) vectorized using TF-IDF
- Heatmap visualization of most frequent terms

---
## 📊 Dataset  

The dataset used: **Healthcare Providers.csv**  

Includes details such as:  
- National Provider Identifier  
- Provider Credentials, Gender, and Location  
- Number of Medicare Services and Beneficiaries  
- Financial attributes: Medicare Allowed Amount, Submitted Charge Amount, Payment Amount, Standardized Amount  
- HCPCS Drug Indicators & Descriptions  

---

🔬 Workflow  

### Data Preprocessing  
- Cleaned categorical and numerical features  
- Encoded gender, city, entity type, and drug indicators  

### Exploratory Data Analysis (EDA)  
- Checked skewness, correlations, and feature distributions  
- Visualized anomalies with multiple statistical techniques  

### Outlier Detection Methods  
- Z-Score, IQR, Winsorization (for benchmarking)  
- Autoencoder reconstruction error (final anomaly detection approach)  

### Model Training (Autoencoder)  
- Input features scaled using **StandardScaler**  
- Trained an autoencoder with encoder-decoder layers  
- Set anomaly threshold using 95th percentile reconstruction error  

### Evaluation & Visualization  
- Compared anomalies detected by different techniques  
- Plotted anomalies on scatterplots & bubble plots  
- Provided animated anomaly detection visualization  

### Deployment Preparation  
- Model and encoders saved with **Pickle**  
- User input function for real-time anomaly checking  

---

📈 **Example Outputs**  
- Correlation Heatmap of healthcare financial features  
- Boxplots highlighting outliers detected by Z-Score, IQR, Winsorization  
- Scatter Plot marking anomalous providers in red  
- TF-IDF Heatmap of medical service descriptions  
- Animated Visualization of anomaly detection in Medicare data  

---

🛠️ **Tech Stack**  
- **Python Libraries**:  
  - Pandas, NumPy, Matplotlib, Seaborn, Plotly  
  - Scikit-learn (preprocessing, scaling, metrics)  
  - TensorFlow / Keras (for Autoencoder)  
  - Scipy (statistical analysis)  
  - ipywidgets (interactive visualization)  

---

📌 **Future Enhancements**  
- Incorporate **DBSCAN** and **Isolation Forest** for comparison  
- Extend anomaly detection to time-series healthcare billing data  
- Build a **Streamlit** web app for easy user interaction  
- Add explainability module for anomalies (e.g., **SHAP values**)  

---

📝 **Conclusion**  
This project demonstrates how **Autoencoders** can effectively detect anomalies in healthcare provider datasets by identifying unusual billing patterns and service anomalies.  
The solution combines **statistical techniques**, **unsupervised deep learning**, and **rich visualizations** to aid fraud detection and healthcare compliance monitoring.  

