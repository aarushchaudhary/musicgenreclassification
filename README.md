# Spotify Song Feature Analyzer & Visualizer 🎶📊

## Overview

This project provides a tool to analyze the audio features of any song from Spotify. You can input a Spotify track URL, and the tool will fetch its metadata and audio features (like `danceability`, `energy`, and `valence`) using the Spotify Web API.

The primary feature is a comparative visualization that plots the song's audio profile on a **radar chart** against the average profile of all songs in a local dataset. This allows for an instant visual comparison of a song's characteristics. The tool also augments the local dataset by adding the newly analyzed song, allowing the collection to grow over time.

---

## Features

- **Fetch from Spotify:** Retrieves detailed track info and audio features using just a song's URL.
- **Comparative Analysis:** Calculates the average audio profile from a local CSV dataset.
- **Interactive Visualization:** Generates a radar chart to visually compare a new song against the dataset average.
- **Data Augmentation:** Appends the newly fetched song's data to the local dataset for future analysis.

---

## Directory Structure

A clean project structure is crucial for organization and scalability.

````
spotify-song-analyzer/
│
├── data/
│   ├── dataset.csv               \# Your initial, raw dataset
│   └── trained_dataset.csv       \# The growing dataset with new songs
│
├── notebooks/
│   └── analysis.ipynb           \# The main Jupyter Notebook for all your work
│
├── visualizations/
│   └── chart.png                \# Folder to save generated plots
│
├── .gitignore                    \# To ignore files from version control
├── config.py                     \# To safely store your Spotify API credentials
├── README.md                     \# This file\!
└── requirements.txt              \# A list of all necessary Python packages
````

---

## Setup & Installation

Follow these steps to get the project running on your local machine.

### 1. Prerequisites

- Python 3.8 or higher
- A Spotify Developer account to get API credentials. You can create one [here](https://developer.spotify.com/dashboard/).

### 2. Install Dependencies

It's highly recommended to use a virtual environment to keep dependencies isolated.

```bash
# Create and activate a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Install the required packages from the requirements file
pip install -r requirements.txt
````

### 3\. Add Spotify API Credentials

You need to add your personal Spotify API credentials to the project.

1.  Create a file named `config.py` in the root directory.

2.  Add your Client ID and Client Secret to this file like so:

    ```python
    # config.py
    CLIENT_ID = 'YOUR_CLIENT_ID_HERE'
    CLIENT_SECRET = 'YOUR_CLIENT_SECRET_HERE'
    ```

**Important:** The `.gitignore` file is already configured to ignore `config.py`, so you won't accidentally commit your secret keys to a version control system like Git.

-----

## How to Use

1.  Place your initial `dataset.csv` file inside the `data/` folder.
2.  Launch Jupyter Lab from your terminal:
    ```bash
    jupyter lab
    ```
3.  Open the `song_analysis.ipynb` notebook located in the `notebooks/` directory.
4.  In the notebook, find the cell where the `track_url` is defined and replace the placeholder with the Spotify URL of the song you want to analyze.
5.  Run all the cells in the notebook from top to bottom.
6.  The interactive radar chart will be displayed directly in the notebook. The `music_dataset_augmented.csv` file in the `data/` folder will be automatically updated with the new song's data.

-----

## Technologies Used

  - **Data Analysis:** Pandas
  - **API Interaction:** Spotipy
  - **Visualization:** Plotly
  - **Environment:** Jupyter Lab
