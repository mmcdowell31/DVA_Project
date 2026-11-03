# Baseball Umpire Call Analysis

This project analyzes MLB Statcast pitch-level data to study incorrect umpire calls. It includes exploratory data analysis, data retrieval and processing workflows, and baseline machine-learning models for predicting:

- Any incorrect call
- Missed strikes
- Missed balls

The project was developed for CSE 6242: Data and Visual Analytics.

## Project Overview

A pitch is labeled as an incorrect call when the called result does not agree with the pitch location relative to the strike zone.

The project focuses on two types of incorrect calls:

- **Missed strike**: a pitch outside the strike zone that is called a strike
- **Missed ball**: a pitch inside the strike zone that is called a ball

The modeling notebooks use pitch characteristics and contextual information to estimate the probability of an incorrect call.

## Repository Structure

```text
DVA_Project/
├── data/
│   ├── raw/
│   │   └── statcast.sqlite
│   └── processed/
│       ├── statcast_2016.parquet
│       ├── statcast_2017.parquet
│       ├── statcast_2018.parquet
│       ├── statcast_2019.parquet
│       ├── statcast_2021.parquet
│       ├── statcast_2022.parquet
│       ├── statcast_2023.parquet
│       ├── statcast_2024.parquet
│       ├── statcast_2025.parquet
│       ├── statcast_2026.parquet
│       ├── statcast_missed_balls.parquet
│       └── statcast_missed_strikes.parquet
├── figs/
│   ├── MLP_WrongCall_Confusion.png
│   └── MLP_WrongCall_Diagnostics.png
├── src/
│   ├── data_retrevial.ipynb
│   ├── data_processing.ipynb
│   ├── eda.ipynb
│   ├── baseline_modeling.ipynb
│   └── baseline_modeling_missed_strikes.ipynb
├── .gitignore
└── README.md