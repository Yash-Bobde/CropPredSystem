# Neural Network-Based Crop Recommendation System  

## Project Overview  
A **Neural Network-Based Decision Support System** designed to help farmers select the most **suitable crops** based on **soil parameters, weather conditions, and market trends**.  

**Technologies Used:** Python, TensorFlow, Keras, Pandas, Matplotlib  
**Models Used:** RNN (LSTM) for price prediction, CNN for crop classification  

---

## Problem Statement  
Farmers lack **data-driven guidance** for choosing crops, leading to **low yields and financial losses**. This system provides **personalized recommendations** by analyzing:  
- **Soil Composition**: Nitrogen, Phosphorus, Potassium, pH  
- **Weather Conditions**: Temperature, Humidity, Rainfall  
- **Market Trends**: Crop price per hundredweight (CWT)  

Example: If a farmer has **acidic soil & low rainfall**, the model suggests **potatoes** (thrives in such conditions).  

---

## Data Sources  
**Datasets used:**  
- [United States Department of Agriculture](https://quickstats.nass.usda.gov/) – Crop pricing trends  
- [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/4GBWFV) – Soil & weather parameters  

**Final Dataset Features:** Soil nutrients, weather data, crop pricing history  

---

## Model Architecture  
This project integrates a **hybrid CRNN (CNN + RNN) model**:  

### **RNN (LSTM) – Crop Price Prediction**  
- Learns **historical price trends**  
- **Output:** Predicted price per CWT  

### **CNN – Crop Classification**  
- Takes **RNN-predicted price + soil & weather data**  
- **Output:** Best crop recommendation  

**Model Flow:**  
**Historical Data** → **RNN (Predicts Price per CWT)** → 📈 **CNN (Final Crop Recommendation)**  


---

## Challenges & Future Enhancements  
### **Challenges**  
- Limited dataset (only 4 crops available)  
- Price data is **dynamic & inconsistent**  

### **Future Improvements**  
Expand dataset (more crops & soil parameters)  
Introduce **regional-specific recommendations**  
Add **crop rotation feature**  
Build **mobile/web app for farmers**  
