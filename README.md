# Music Genre Classification & Recommendation System 🎶📊

## Overview

This project provides a genre-based music recommendation system using YouTube Music. The tool analyzes songs from a local dataset and provides personalized recommendations based on genre preferences using the ytmusicapi library to fetch music data from YouTube Music.

The system allows you to explore music by genre, analyze audio features, and get recommendations based on your preferred genres. The tool uses a comprehensive dataset of songs with various audio features and genres to provide accurate and diverse recommendations.

---

## Features

- **YouTube Music Integration:** Fetches music data and recommendations using ytmusicapi.
- **Genre-Based Recommendations:** Get personalized song recommendations based on your preferred music genres.
- **Dataset Analysis:** Analyzes audio features from a comprehensive local dataset.
- **Interactive Visualizations:** Generates charts and plots to explore genre distributions and audio features.
- **Music Discovery:** Discover new songs based on genre preferences and audio characteristics.

---

## Directory Structure

A clean project structure is crucial for organization and scalability.

````
musicgenreclassification/
│
├── data/
│   ├── dataset.csv               \# Your initial dataset with songs and genres
│   └── trained_dataset.csv       \# Processed dataset for recommendations
│
├── notebooks/
│   └── analysis.ipynb           \# The main Jupyter Notebook for analysis and recommendations
│
├── visualizations/
│   └── (generated charts)        \# Folder to save generated plots
│
├── .gitignore                    \# To ignore files from version control
├── README.md                     \# This file\!
└── requirements.txt              \# A list of all necessary Python packages
````

---

## Setup & Installation

Follow these steps to get the project running on your local machine.

### 1. Prerequisites

- Python 3.8 or higher
- Internet connection to access YouTube Music via ytmusicapi

### 2. Install Dependencies

It's highly recommended to use a virtual environment to keep dependencies isolated.

```bash
# Create and activate a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Install the required packages from the requirements file
pip install -r requirements.txt
````

-----

## How to Use

1.  Place your initial `dataset.csv` file inside the `data/` folder (should contain songs with genre labels and audio features).
2.  Launch Jupyter Lab from your terminal:
    ```bash
    jupyter lab
    ```
3.  Open the `analysis.ipynb` notebook located in the `notebooks/` directory.
4.  In the notebook, specify your preferred genre(s) to get personalized recommendations.
5.  Run all the cells in the notebook from top to bottom.
6.  The system will:
    - Analyze your dataset
    - Connect to YouTube Music via ytmusicapi
    - Generate genre-based recommendations
    - Display visualizations of genre distributions and audio features

-----

## Technologies Used

  - **Data Analysis:** Pandas, NumPy
  - **API Interaction:** ytmusicapi (YouTube Music)
  - **Visualization:** Plotly, Matplotlib, Seaborn
  - **Machine Learning:** Scikit-learn (for genre classification)
  - **Environment:** Jupyter Lab
