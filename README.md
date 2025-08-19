#  Traffic Prediction using Big Data Processing

Traffic violations are common in urban areas, and predicting them helps law enforcement and planners manage roads better.  
This project uses **big data techniques** and **deep learning** to capture daily patterns of violations.

---

##  Dataset Overview
- **Source**: Montgomery County, Maryland (USA) – *Traffic Violations Dataset*  
- **Size**: 2M+ records, 43 columns  

---

##  Data Cleaning Process
### Identified Issues
- Missing values in `Search Reason`, `Color`, `DL State`  
- Mismatched datatypes  
- Rows missing date or geolocation  

### Solution
- Used **Dask** for parallel and memory-efficient CSV handling  
- Dask is mainly used for:  
  - Faster loading & transformation with **chunking**  
  - Preprocessing and grouping before modeling  

---

##  Why I chose LSTM?
- Remembers **long-term patterns**  
- Works well with **time-series data**  
- Captures **seasonality**, **day-of-week**, and **monthly trends**  

---

##  My Model Setup
- **Input**: Rolling 30-day window  
- **Architecture**: 1 LSTM layer + 1 Dense output  
- **Loss Function**: Mean Squared Error (MSE)  
- **Training**: 10 epochs, batch size 32  
- **Performance**: MSE ≈ 15,000  

---

##  Geographic Analysis
- Built an **interactive heatmap** using Pydeck  
- Showed violation density across the county  

---

##  Learnings
- Using **Dask** for scalable big data processing  
- Applying **LSTM** for time-series prediction  
- Analysing and identifying **traffic patterns** for better road safety planning  

---
