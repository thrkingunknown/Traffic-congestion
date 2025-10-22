# Traffic Congestion Analysis - Bangalore City

A comprehensive data analysis project focused on understanding and analyzing traffic patterns across major roads and intersections in Bangalore city. This project uses exploratory data analysis (EDA) and machine learning techniques to identify traffic congestion patterns and provide actionable insights.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thrkingunknown/Traffic-congestion/blob/main/Traffic_conjestion.ipynb)

## 📁 Repository Structure

```
Traffic-congestion/
│
├── README.md                      # Project documentation (this file)
└── Traffic_conjestion.ipynb       # Main Jupyter notebook with complete analysis
```

## 📊 Dataset

This project utilizes the **Bangalore City Traffic Dataset** from Kaggle, which captures detailed traffic patterns across major roads and intersections in Bangalore. The dataset includes:

- **Traffic Volume**: Number of vehicles at specific locations
- **Average Speed**: Speed of traffic flow
- **Congestion Level**: Level of traffic congestion
- **Area Name**: Geographic area in Bangalore
- **Road/Intersection Name**: Specific road or intersection
- **Travel Time Index**: Relative travel time compared to free-flow conditions
- **Incident Reports**: Number of traffic incidents
- **Road Capacity Utilization**: Percentage of road capacity being used
- **Weather Conditions**: Weather during measurement
- **Environmental Impact**: Environmental metrics

**Dataset Source**: [Bangalore City Traffic Dataset](https://www.kaggle.com/datasets/preethamgouda/banglore-city-traffic-dataset)

## 🔧 Dependencies and Installation

### Required Libraries

```python
# Data Processing
pandas
numpy

# Data Visualization
matplotlib
seaborn
plotly

# Machine Learning
scikit-learn

# Data Import
kagglehub
```

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/thrkingunknown/Traffic-congestion.git
   cd Traffic-congestion
   ```

2. **Install required packages:**
   ```bash
   pip install pandas numpy matplotlib seaborn plotly scikit-learn kagglehub
   ```

3. **Open the notebook:**
   ```bash
   jupyter notebook Traffic_conjestion.ipynb
   ```
   
   Or use Google Colab by clicking the badge at the top of this README.

## 📓 Notebook Structure

The `Traffic_conjestion.ipynb` notebook is organized into the following sections:

### 1. Introduction and Data Loading
- Dataset import from Kaggle using `kagglehub`
- Initial data exploration and setup
- Data loading and preprocessing

### 2. Exploratory Data Analysis (EDA)

The notebook includes 9 comprehensive visualizations:

#### **2.1 Heat Map**
- Visualizes traffic volume across different areas and intersections
- **Key Insight**: Koramangala and Indiranagar show consistently high traffic volumes

#### **2.2 SunBurst Chart**
- Hierarchical view of traffic patterns by area and road/intersection
- **Key Insight**: Major areas like Koramangala and Indiranagar have multiple high-traffic intersections

#### **2.3 Scatter Plot**
- Relationship between traffic volume and average speed
- Color-coded by congestion level
- **Key Insight**: Inverse relationship between traffic volume and average speed; higher volume leads to slower speeds

#### **2.4 Box Plot**
- Distribution of Travel Time Index across different areas
- **Key Insight**: Koramangala shows high variability in travel times, indicating inconsistent traffic conditions

#### **2.5 Pie Chart**
- Distribution of incident reports across areas
- **Key Insight**: M.G. Road and Koramangala account for the majority of traffic incidents

#### **2.6 Histogram**
- Distribution of road capacity utilization
- **Key Insight**: Many roads operate at or near full capacity, indicating infrastructure strain

#### **2.7 Radial Bar Chart**
- Average congestion levels by area
- **Key Insight**: M.G. Road and Koramangala have consistently high congestion levels

#### **2.8 Density Plot**
- Traffic volume vs. average speed density contours
- **Key Insight**: Most traffic operates within specific speed and volume ranges

#### **2.9 Stacked Bar Chart**
- Traffic volume by weather conditions across areas
- **Key Insight**: Clear weather sees higher traffic volumes, suggesting weather-dependent travel patterns

### 3. K-Means Clustering Analysis

Machine learning approach to identify traffic pattern clusters:

#### **Data Preparation**
- Feature selection of relevant traffic metrics
- Data standardization using `StandardScaler`
- Dimensionality reduction using PCA (Principal Component Analysis)

#### **Elbow Method**
- Determines optimal number of clusters (k)
- Visualizes inertia across different k values

#### **Clustering Results**

**Cluster 0 - Moderate Traffic Areas:**
- Lower traffic volumes
- Moderate congestion levels
- Road capacity utilization: 75-80%
- Lower environmental impact
- Represents less urbanized or off-peak areas

**Cluster 1 - High Congestion Areas:**
- Higher traffic volumes
- Elevated congestion levels
- Higher road capacity utilization
- Greater environmental impact
- Represents highly urbanized, congested areas

#### **Visualization**
- Multi-panel visualization showing distribution of various metrics across clusters
- Includes traffic volume, average speed, congestion level, capacity utilization, and more

### 4. Rule-Based Inference

- Aggregates traffic data by area and road
- Calculates mean values for key metrics
- Provides rule-based insights for traffic management

## 🎯 Key Findings

1. **Geographic Hotspots**: Koramangala, Indiranagar, and M.G. Road are primary congestion areas
2. **Traffic Patterns**: Clear inverse relationship between traffic volume and average speed
3. **Infrastructure Utilization**: Many roads operate at or near full capacity
4. **Incident Correlation**: High-traffic areas also show higher incident rates
5. **Weather Impact**: Traffic patterns vary significantly with weather conditions
6. **Cluster Insights**: Two distinct traffic pattern clusters identified - moderate and high congestion areas

## 🚀 Usage

### Running the Analysis

1. **Execute cells sequentially**: The notebook is designed to run from top to bottom
2. **Data Import**: First cell downloads the dataset from Kaggle
3. **EDA Section**: Run all visualization cells to see interactive plots
4. **ML Section**: Execute clustering cells to reproduce machine learning analysis

### Customization

You can modify the analysis by:
- Changing visualization parameters (colors, chart types)
- Adjusting the number of clusters in K-Means
- Adding additional features to the clustering analysis
- Implementing different machine learning algorithms

## 📈 Visualizations

The notebook generates interactive visualizations using Plotly, including:
- Heat maps
- Sunburst charts
- Scatter plots
- Box plots
- Pie charts
- Histograms
- Radial bar charts
- Density contour plots
- Stacked bar charts

All visualizations are interactive and can be zoomed, panned, and explored.

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Create a Pull Request

## 📝 Future Enhancements

Potential areas for expansion:
- Time-series analysis of traffic patterns
- Predictive modeling for traffic forecasting
- Integration with real-time traffic data
- Optimization algorithms for traffic management
- Mobile application for traffic alerts

## 📄 License

This project is open source and available for educational and research purposes.

## 👥 Author

Created by [thrkingunknown](https://github.com/thrkingunknown)

## 🙏 Acknowledgments

- Dataset provided by [Preetham Gouda](https://www.kaggle.com/preethamgouda) on Kaggle
- Traffic data sourced from Bangalore City Traffic Department
- Analysis conducted using Python data science ecosystem

---

**Note**: This analysis is for educational and research purposes. For official traffic management decisions, please consult local traffic authorities.