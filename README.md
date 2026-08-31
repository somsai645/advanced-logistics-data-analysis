# Advanced Data Analysis and Visualization in Logistics

## Project Overview

This project demonstrates how Python can be used to simulate, clean, analyze, and visualize logistics data for data-driven operational decision-making.

The analysis uses a **hypothetical dataset of 300 shipments** and focuses on important logistics performance measures such as delivery time, shipment volume, transportation cost, fuel cost, delay, damage rate, and on-time delivery.

The project was developed as an academic submission for **Advanced Data Analysis and Visualization in Logistics**.

---

## Objectives

The main objectives of this project are to:

- Simulate a realistic logistics dataset using Python.
- Introduce and handle missing values to demonstrate data-cleaning techniques.
- Perform Exploratory Data Analysis (EDA).
- Calculate descriptive statistics and identify relationships among logistics variables.
- Analyze logistics performance by transportation mode and region.
- Create visualizations to identify trends, distributions, cost drivers, and potential bottlenecks.
- Generate practical recommendations for improving logistics efficiency.
- Produce a professional analytical report using the results.

---

## Dataset Description

The dataset contains **300 simulated shipment records**.

### Main Variables

| Variable | Description |
|---|---|
| `Shipment_ID` | Unique identifier for each shipment |
| `Date` | Shipment date |
| `Region` | Operating region: North, South, East, or West |
| `Transport_Mode` | Transportation method: Road, Rail, Air, or Sea |
| `Distance_km` | Shipment distance in kilometres |
| `Shipment_Volume_kg` | Shipment volume/weight in kilograms |
| `Promised_Time_hr` | Promised delivery time in hours |
| `Delivery_Time_hr` | Actual delivery time in hours |
| `Delay_Hours` | Shipment delay in hours |
| `Transport_Cost_INR` | Transportation cost in Indian Rupees |
| `Fuel_Cost_INR` | Estimated fuel-related cost in Indian Rupees |
| `Damage_Rate` | Estimated shipment damage rate |
| `On_Time` | Indicates whether delivery met the promised time |
| `Operational_Efficiency_kg_hr` | Shipment volume delivered per delivery hour |

The simulation uses controlled probabilities and mathematical relationships to create realistic variation across regions, transportation modes, distances, delays, and costs.

---

## Technologies Used

- **Python 3**
- **Pandas** – data manipulation and analysis
- **NumPy** – numerical simulation and calculations
- **Matplotlib** – data visualization
- **python-docx** – generation of the analytical Word report

---

## Project Workflow

The project follows the workflow below:

```text
Data Simulation
      ↓
Data Quality Issues Introduced
      ↓
Data Cleaning & Preprocessing
      ↓
Exploratory Data Analysis
      ↓
Statistical & Correlation Analysis
      ↓
Data Visualization
      ↓
Business Interpretation
      ↓
Logistics Recommendations
      ↓
Final Analytical Report
```

---

## Data Cleaning and Preprocessing

To demonstrate practical data-quality handling, missing values are intentionally introduced into selected numerical variables.

Missing values are created in:

- `Distance_km`
- `Shipment_Volume_kg`
- `Transport_Cost_INR`

The preprocessing stage identifies these missing observations and fills them using appropriate numerical imputation methods before the analysis is performed.

This step is important because incomplete logistics records can distort averages, correlations, cost calculations, and operational conclusions.

---

## Exploratory Data Analysis

The analysis includes:

- Central tendency measures such as mean, median, and standard deviation.
- Distribution analysis of delivery times.
- Comparison of average delays across transportation modes.
- Relationship between shipment distance and transportation cost.
- Correlation analysis among major numerical logistics variables.
- Regional on-time delivery performance.
- Daily delay trends.
- Operational efficiency calculations.

These analyses help transform raw shipment information into measurable operational insights.

---

## Visualizations

The Python script generates the following six visualizations:

### 1. Delivery-Time Distribution
**File:** `01_delivery_distribution.png`

A histogram showing the distribution of delivery times across shipments.

**Purpose:**  
Helps identify the typical delivery-time range, variation, and unusually long deliveries.

### 2. Average Delay by Transportation Mode
**File:** `02_delay_by_mode.png`

A bar chart comparing average shipment delays for Road, Rail, Air, and Sea transportation.

**Purpose:**  
Helps identify transportation modes that may require operational improvement or better scheduling buffers.

### 3. Distance vs Transportation Cost
**File:** `03_distance_cost.png`

A scatter plot showing the relationship between shipment distance and transportation cost.

**Purpose:**  
Helps identify distance-related cost drivers and understand how transportation expenditure changes with route length.

### 4. Logistics Correlation Heatmap
**File:** `04_correlation_heatmap.png`

A correlation matrix visualizing relationships among major numerical logistics variables.

**Purpose:**  
Helps detect variables that move together and supports identification of potential cost, delay, and efficiency drivers.

### 5. On-Time Delivery by Region
**File:** `05_region_ontime.png`

A regional comparison of the percentage of shipments delivered on time.

**Purpose:**  
Supports regional performance benchmarking and helps identify areas requiring operational attention.

### 6. Daily Delay Trend
**File:** `06_delay_trend.png`

A time-series chart showing how average shipment delays change over the simulated period.

**Purpose:**  
Helps identify periods of rising delays, operational instability, or potential bottlenecks.

---

## Key Analytical Insights

The simulated analysis is designed to demonstrate several important logistics insights:

- **Transportation mode influences delivery performance.** Road shipments are modelled with stronger exposure to congestion and therefore can show higher delay levels than faster or less congestion-sensitive modes.
- **Distance is an important cost driver.** Longer transportation routes generally require higher transportation expenditure.
- **Shipment volume and delivery time can be evaluated together to measure operational efficiency.**
- **Regional differences can reveal variations in service performance.** Comparing on-time delivery rates helps management identify stronger and weaker operating regions.
- **Correlation analysis provides a quick way to identify relationships between distance, volume, delivery time, delay, and cost.**
- **Delay trends can be monitored over time** to identify periods where logistics operations may require intervention.

Because the dataset is simulated, these insights are intended for academic demonstration rather than real-world operational reporting.

---

## Recommendations

Based on the analytical framework, the following recommendations can support logistics decision-making:

1. **Improve route planning** for long-distance shipments to reduce unnecessary transportation time and cost.
2. **Monitor road transportation closely** in areas with high congestion risk.
3. **Use regional performance dashboards** to compare on-time delivery rates and detect weak-performing areas.
4. **Track cost per shipment and cost per kilometre** to identify inefficient routes or modes.
5. **Use historical delay patterns** to improve promised delivery times and scheduling buffers.
6. **Monitor operational efficiency** using shipment volume delivered per delivery hour.
7. **Combine cost and service-level metrics** rather than optimizing transportation cost alone.

---

## Repository Structure

A recommended GitHub repository structure is:

```text
advanced-logistics-data-analysis/
│
├── create_logistics_report.py
├── logistics_simulated_cleaned.csv
├── README.md
│
└── logistics_analysis_assets/
    ├── 01_delivery_distribution.png
    ├── 02_delay_by_mode.png
    ├── 03_distance_cost.png
    ├── 04_correlation_heatmap.png
    ├── 05_region_ontime.png
    └── 06_delay_trend.png
```

The Word report can also be included in the repository as an optional submission document.

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/advanced-logistics-data-analysis.git
cd advanced-logistics-data-analysis
```

### 2. Install the required libraries

```bash
pip install numpy pandas matplotlib python-docx
```

### 3. Run the Python script

```bash
python create_logistics_report.py
```

### 4. Generated Outputs

The script generates:

- Logistics visualization images.
- A cleaned CSV dataset.
- A Word analysis report.

> **Note:** The script currently uses `/mnt/data/` paths for some generated outputs because it was created in a controlled submission environment. When moving the project to GitHub, these paths can be changed to relative project paths such as `./logistics_analysis_assets/` for easier execution on another computer.

---

## Reproducibility

A fixed NumPy random seed (`42`) is used in the simulation. This makes the generated dataset and analytical results reproducible when the script is run under the same software environment.

---

## Limitations

This project has several limitations:

- The dataset is **hypothetical and simulated**, not collected from a real logistics company.
- The relationships among variables are generated using assumptions and probability distributions.
- The cost and delay models are illustrative and should not be treated as real industry benchmarks.
- The analysis does not include real-world constraints such as vehicle capacity, traffic API data, warehouse inventory, driver schedules, or actual fuel-price fluctuations.

---

## Academic Value

This project demonstrates the practical application of Python for:

- Logistics data preparation
- Exploratory data analysis
- Statistical interpretation
- Data visualization
- Performance measurement
- Cost analysis
- Operational decision-making

It provides an end-to-end example of how logistics data can be converted into useful management insights through analytical techniques.

---

## License

This project is intended for **educational and academic purposes**.

---

## Author

**Student Project – Advanced Data Analysis and Visualization in Logistics**

Repository: `advanced-logistics-data-analysis`
