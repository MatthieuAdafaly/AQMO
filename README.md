# 📊 AQMO Data Analysis Notebooks
This notebook is distributed under the license: https://www.etalab.gouv.fr/licence-ouverte-open-licence/
This repository contains a set of Jupyter notebooks to process, analyze, and visualize AQMO air quality data.

To make these notebooks work, you need to have a sub folder called 'Data' in the same folder

## 🔧 Notebook Overview

There are **four main notebooks** in this project:

### 1. `Data_Import.ipynb` (**required first step**)
This notebook prepares the dataset by importing and processing raw data into a `.pkl` (pickle) file.

**⚠️ Must be run first** before any further analysis or visualization.

Or if you want, you can download the data without a long processing time by running the code below :

```python
from rudi_node_read.rudi_node_reader import RudiNodeReader

rudi_node_url = 'https://opendata.fenix.rudi-univ-rennes1.fr'
rudi_node_info = RudiNodeReader(server_url=rudi_node_url)

meta_id = '9e64890a-7d31-4ad8-8011-356e0ef2fceb'
dwnld_tag = 'Downloading'
dwnld_dir = './data_test'

print(dwnld_tag, f"media for metadata '{meta_id}':", rudi_node_info.download_files_for_metadata(meta_id, dwnld_dir))
```

---

### 2A. `Mobile_Data_Exploration_With_Map.ipynb` (for interactive map visualization)

- Offers a **visual and interactive** map-based exploration of the mobile sensor data.
- You can apply filters such as:
  - **Date**
  - **Location**
  - **Sensor**
- Good choice if you're interested in **exploring trends visually**.

When you run this code, a window will open and remain open until you click the "Quit" button. It will display two calendars: one for the start date and one for the end date. The data will be filtered to include only measurements taken between these two dates. You can also select which sensors to include or exclude.

Additionally, you can filter the data using a GeoJSON file. To create this file, first click the "Confirm" button without selecting a GeoJSON file — this will generate the initial map. On the map, use the rectangle tool (the square icon in the top-left corner) to draw a selection area. Then, click the "Export" button (in the top-right corner) to save the rectangle as a GeoJSON file. After that, you can load this file by clicking the "Load Rectangle" button, and then clicking "Confirm" to apply the filter.

Don't forget to click the "Quit" button when you're done — this is necessary to allow the next cell to be activated.
---

### 2B. `Filter_Data.ipynb` + `Data_Exploration.ipynb` (for non-visual, in-depth analysis)

- These notebooks perform **detailed data filtering and statistical analysis**.
- Includes both **mobile and stationary sensor data**.
- Suitable for use cases where:
  - You want **global trends**.
  - You need **faster performance** (no heavy visualization rendering).
  
The first notebook allows you to filter the data by sensor, date, and more. You must run this code if you want to launch the Data_exploration notebook. You can simply run all cells if you don’t want to make any modifications.
If you want to make changes, you need to edit the notebook directly.
After, that you are free to run the second notebook.
---

## 🚀 Workflow Summary

| Step | Notebook                          | Description                                                               |
|------|-----------------------------------|---------------------------------------------------------------------------|
| 1    | `Data_Import.ipynb`              | Load and preprocess raw data into a `.pkl` file                           |
| 2A   | `Mobile_Data_Exploration_With_Map.ipynb` | Explore data visually using interactive maps                             |
| 2B   | `Filter_Data.ipynb` + `Data_Exploration.ipynb` | Filter and analyze data without visualization (includes stationary data) |

---

## 📁 Requirements

Be sure to install required Python libraries in a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
pip install -r requirements.txt
```
