# 🏎️ Formula 1 Data Engineering & Analysis Pipeline

This repository contains an end-to-end pipeline for retrieving, cleaning, storing, and analyzing **Formula 1 historical racing data**.  
It supports structured data ingestion from the **Ergast Developer API**, transformation into consistent tabular formats, and exploration through summary statistics and visualizations.

---

## 🚦 Key Features

### ✔ Programmatic Data Retrieval  
Uses the **Ergast F1 API** to fetch:

- Race results  
- Driver standings  
- Constructor standings  
- Circuits and tracks  
- Qualifying results  
- Pit stop summaries  
- Race schedules  

### ✔ Local Caching  
Fetched data is stored in:

- CSV files  
- SQLite databases  
- Local API cache files  

This avoids redundant API calls and ensures efficient reproducibility.

### ✔ Clean & Unified Data  
Raw API responses are standardized, merged, and validated into structured datasets suitable for analysis.

### ✔ Reproducible Analysis Workflow  
Includes:

- Step-by-step notebooks  
- Documented methodology in Quarto  
- Visualizations and summary analytics  

---

## 📂 Repository Structure

At a high level, the repository contains the following components:

---

### **📘 Quarto Documents**

A collection of `.qmd` files that document the full project workflow, including:

- Data source documentation  
- Retrieval logic  
- Cleaning and transformation steps  
- Analysis methodology  
- Testing approach  
- Reproducibility practices  

These provide a narrative explanation of the pipeline from start to finish.

---

### **📓 Jupyter Notebooks**

Interactive notebooks used for structured data processing and exploratory analysis:

- **`data_extract.ipynb`** — Retrieves raw Formula 1 datasets from the Ergast API and caches them locally.  
- **`clean.ipynb`** — Cleans, standardizes, and merges raw API data into structured analytical tables.  
- **`summarystats.ipynb`** — Generates descriptive statistics and season-level summary metrics.  
- **`viz.ipynb`** — Creates exploratory visualizations of driver, constructor, and race performance.

---

### **📁 Data and Cache Files**

Includes raw, intermediate, and processed data:

- CSV files with race results, standings, schedules, circuits, pit stops, and merged datasets  
- SQLite databases (`f1_data.db`, etc.) for efficient local storage  
- API cache files (e.g., `ergast_cache.sqlite`) to prevent repeated data downloads

These assets support reproducibility and fast iteration.

---

### **🛠 Python Utilities and Tests**

- **`data_loading_functions.py`** — Contains reusable helper functions for loading and querying datasets.  
- **`test_data_processing.py`** — Basic tests verifying data integrity, schema consistency, and correctness of the cleaning steps.

---

### **📎 Supporting Files**

- **`requirements.txt`** — Python dependencies for running notebooks and scripts  
- **`styles.css`** — Styling for Quarto-rendered documents  
- Additional project artifacts such as `poster.pdf` and `commitgraph.jpg`

---
