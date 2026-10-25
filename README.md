# Pedestrian Counts Data Analysis (2023)

A comprehensive data analysis and visualization project exploring pedestrian traffic dynamics across various locations throughout 2023. Built using **Pandas** for data manipulation and **Matplotlib** for visualization, this repository provides scripts and notebooks to uncover daily, hourly, weekly, and seasonal foot-traffic patterns across multiple monitoring checkpoints.

---

## 📌 Project Overview

Understanding urban pedestrian volume is crucial for city planning, business placement, and public infrastructure management. This project analyzes hourly pedestrian counts collected over the course of a full year (January 1, 2023 – December 31, 2023) to address key urban mobility questions:
- What are the peak pedestrian traffic hours during the day?
- How does foot traffic shift between weekdays and weekends?
- What are the seasonal and monthly foot-traffic trends?
- How do different spatial checkpoints across the city compare in volume and peak usage?
- Is there a noticeable bias between Inbound (IN) and Outbound (OUT) movement at specific locations?

---

## 📊 Visualizations & Analyses Included

The analytical code includes multi-aspect exploratory data analysis (EDA) categorized into two main perspectives:

### 1. Single-Location Deep Dives
* **Daily Traffic Trend:** Time-series line chart depicting day-to-day fluctuations across the entire year.
* **Hourly Diurnal Pattern:** Aggregated 24-hour profile identifying morning, afternoon, and evening rush hours.
* **Day-of-Week Distribution:** Bar charts comparing commute patterns (Monday–Friday) versus weekend leisure activity.
* **Inbound vs. Outbound Flow:** Comparative trend lines evaluating directional traffic bias over time.
* **Monthly Boxplots:** Statistical distribution showing medians, interquartile ranges, and seasonal variation per month.
* **Top Locations Ranking:** Bar chart ranking the overall highest-volume pedestrian stations in the city network.

### 2. Multi-Location Comparative Analyses
* **Hourly Traffic Comparison across Top Locations:** Overlaid 24-hour traffic profiles for the busiest checkpoints to contrast commercial, residential, and transit hub behaviors.
* **Monthly Trend Comparison across Top Locations:** Multi-line seasonal tracking evaluating how different regions of the city respond to seasonal shifts.

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.8+ installed along with the following libraries:

```bash
pip install pandas matplotlib seaborn kagglehub
```

### Dataset Download

The analysis utilizes the `leilahasan/pedestrian-counts` dataset hosted on Kaggle. You can automatically fetch it via `kagglehub` in Python:

```python
import kagglehub

# Download latest version of the dataset
path = kagglehub.dataset_download("leilahasan/pedestrian-counts")
print("Path to dataset files:", path)
```

---

## 🛠️ Usage Instructions

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/pedestrian-counts-analysis.git
   cd pedestrian-counts-analysis
   ```

2. **Run the Analysis Script / Jupyter Notebook:**
   Load your environment and execute the script:
   ```bash
   python pedestrian_analysis.py
   ```
   *Alternatively, open `pedestrian_analysis.ipynb` in Jupyter Notebook or Google Colab.*

3. **Sample Execution Script:**
   ```python
   import matplotlib.pyplot as plt
   import pandas as pd

   # Load data
   df = pd.read_csv(
       f"{path}/pedestrian-counts-1-jan-31-december-2023 (2).csv"
   )

   # Preprocessing: Datetime formatting
   df['Time'] = pd.to_datetime(df['Time'], format='%d/%m/%Y %H:%M')
   df.set_index('Time', inplace=True)

   # Run visualization code...
```

---

## 📂 Project Structure

```text
.
├── README.md                  # Project documentation
├── pedestrian_analysis.py    # Main Python script with Matplotlib visualizations
├── pedestrian_analysis.ipynb  # Interactive Jupyter Notebook version
└── requirements.txt           # Project dependencies
```

---

## 🛠️ Built With

* **[Python](https://www.python.org/)** - Core programming language
* **[Pandas](https://pandas.pydata.org/)** - Data manipulation and time-series resampling
* **[Matplotlib](https://matplotlib.org/)** - Static data visualization
* **[Kagglehub](https://github.com/Kaggle/kagglehub)** - Seamless Kaggle dataset integration

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
