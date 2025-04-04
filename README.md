# 🌐 Internet Speed Analysis Project  

*A comprehensive analysis of global internet performance metrics, including download/upload speeds and latency, with interactive visualizations and geospatial insights.*

---

## 📖 **Project Overview**  
This project investigates internet speed metrics across different regions and countries, comparing fixed broadband and mobile connections. By leveraging Python’s data analysis and visualization tools, it provides actionable insights into global internet performance trends, latency issues, and regional disparities. The analysis includes:  
- **Data cleaning** and preprocessing of raw speed test data.  
- **Exploratory Data Analysis (EDA)** to uncover patterns and anomalies.  
- **Geospatial visualizations** to map performance metrics globally.  
- **Interactive dashboards** for dynamic exploration of the data.  

---

## 📌 **Key Features**  

### **1. Data Processing**  
- **Data Loading**: Imports datasets from multiple sources (e.g., Ookla Speedtest, government reports).  
- **Cleaning**: Handles missing values, outliers, and inconsistencies.  
  - Median imputation for missing latency metrics (`avg_lat_down_ms`, `avg_lat_up_ms`).  
  - Normalization of speed units (e.g., converting Mbps to Kbps).  
- **Preprocessing**: Aggregates data by region, country, and connection type.  

### **2. Visualizations**  
- **Interactive Charts**:  
  - **Bar/Pie Charts**: Compare average speeds across top-performing countries.  
  - **Treemaps**: Hierarchical view of speed distribution by region.  
  - **Scatter Plots**: Correlation between download and upload speeds.  
  - **Line Graphs**: Trend analysis over time (if time-series data exists).  
- **Geospatial Maps**:  
  - Folium/Plotly maps to visualize speeds on a global scale.  
  - Heatmaps for latency hotspots.  

### **3. Comparative Analysis**  
- Fixed vs. mobile connection performance.  
- Regional benchmarks (e.g., North America vs. Southeast Asia).  
- Latency impact on user experience.  

---

## 📊 **Datasets Used**  
The analysis relies on:  
1. **Ookla Speedtest Data** (or similar):  
   - Metrics: Download/upload speeds (Kbps/Mbps), latency (ms).  
   - Granularity: Tile-level (geospatial) and country-level summaries.  
   - Format: Parquet files (e.g., `2024-04-01_performance_fixed_tiles.parquet`).  

2. **Mobile Speed Data** (e.g., `mobile_year_2022_quarter_03.csv`):  
   - Columns: `Country`, `avg_d_kbps`, `avg_u_kbps`, `avg_lat_ms`.  

3. **Geospatial Data**:  
   - GPS tiles for mapping (`tile_x`, `tile_y`, `quadkey`).  

*Note: Large datasets are excluded via `.gitignore`; placeholder paths are provided for reproducibility.*  

---

## 🛠️ **Technologies**  
- **Python Libraries**:  
  - `pandas`: Data manipulation.  
  - `plotly`/`matplotlib`: Interactive visualizations.  
  - `geopandas`: Geospatial mapping.  
  - `numpy`: Numerical operations.  
- **Tools**:  
  - Jupyter Notebook (for exploratory analysis).  
  - Google Colab (optional cloud execution).  

---

## 🚀 **Setup & Execution**  

### **Prerequisites**  
- Python 3.8+  
- Jupyter Notebook or Google Colab.  

### **Installation**  
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/Internet-Speed-Analysis.git
   cd Internet-Speed-Analysis
   ```  
2. Install dependencies:  
   ```bash
   pip install pandas plotly geopandas matplotlib folium
   ```  

### **Running the Analysis**  
1. Launch Jupyter Notebook:  
   ```bash
   jupyter notebook
   ```  
2. Open `Internet_Speed_Project.ipynb` and execute cells sequentially.  

---

## 📂 **Repository Structure**  
```
Internet-Speed-Analysis/
├── data/                    # Placeholder for datasets (excluded via .gitignore)
│   ├── fixed_tiles.parquet  # Example path
│   └── mobile_data.csv      
├── Internet_Speed_Project.ipynb  # Main analysis notebook
├── README.md               # This file
├── requirements.txt        # Dependency list
└── .gitignore              # Excludes large/data files
```

---

## 📸 **Sample Outputs**  
Top 5 Countries by Download Speed:
![image](https://github.com/user-attachments/assets/5ffce237-9e2b-421f-9df4-2b8fdb6d186f)


---

## 🤝 **Contributing**  
Contributions are welcome! Open an issue or submit a PR for:  
- Additional datasets.  
- Enhanced visualizations (e.g., D3.js integration).  
- Machine learning models for speed prediction.  

---

## 📜 **License**  
MIT License. See [LICENSE](LICENSE) for details.  

