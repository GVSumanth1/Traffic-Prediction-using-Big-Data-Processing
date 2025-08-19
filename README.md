Traffic violations are common in urban areas, and predicting them helps law enforcement and planners manage roads better. This project uses big data techniques and deep learning to capture daily patterns of violations.

**Dataset Overview:**
Source: Montgomery County, Maryland (USA) – Traffic Violations Dataset
Size: 2M+ records, 43 columns

**Data Cleaning Process:**
Identified Issues: Missing values in Search Reason, Color, DL State
Mismatched datatypes
Rows missing date or geolocation

Used **Dask** for parallel and memory efficient CSV handling (as i worked on large dataset)
Dask is mainly used for Faster loading & transformation with chunking, and for preprocessing and grouping before modeling

**Why I chose LSTM?**
Remembers long-term patterns
Works well with time series data
Captures seasonality, day of week, and monthly trends

**My Model Setup**
Input: Rolling 30-day window
Architecture: 1 LSTM layer + 1 Dense output
Loss: Mean Squared Error (MSE)
Training: 10 epochs, batch size 32
Final Performance: MSE ≈ 15,000


**Geographic Analysis**
Built an interactive heatmap using Pydeck
Showed violation density across the county

**Learnings:**
Dask for scalable big data processing
Using LSTM
Analyse & Identify traffic patterns for better road safety planning
