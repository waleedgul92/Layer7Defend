# Edge IIoT Intrusion Detection System (IDS)

This repository contains a Jupyter Notebook (`GDSC.ipynb`) demonstrating an Intrusion Detection System (IDS) for Edge IIoT (Industrial Internet of Things) environments. The project focuses on analyzing network traffic data to identify and classify various types of cyberattacks using machine learning techniques.

## Table of Contents

  - [Project Overview](https://www.google.com/search?q=%23project-overview)
  - [Dataset](https://www.google.com/search?q=%23dataset)
  - [Key Features](https://www.google.com/search?q=%23key-features)
  - [Installation](https://www.google.com/search?q=%23installation)
  - [Usage](https://www.google.com/search?q=%23usage)
  - [Attack Types Analyzed](https://www.google.com/search?q=%23attack-types-analyzed)
  - [Contributing](https://www.google.com/search?q=%23contributing)
  - [License](https://www.google.com/search?q=%23license)

## Project Overview

The `GDSC.ipynb` notebook implements a comprehensive data analysis and machine learning pipeline to detect and classify cyberattacks in an Edge IIoT dataset. The primary goal is to build a robust model capable of distinguishing between normal network behavior and various attack patterns.

## Dataset

The project utilizes the `ML-EdgeIIoT-dataset.csv` dataset, which contains network traffic data from an Edge IIoT environment. This dataset is crucial for training and evaluating the intrusion detection model.

## Key Features

  - **Exploratory Data Analysis (EDA):** Initial data inspection, including viewing the head of the dataset and checking for missing values using `df.head()` and `df.isna().sum()`. Visualizations for data health checks are performed using `missingno.bar`.
  - **Data Preprocessing:**
      * Conversion of `frame.time` column to datetime objects.
      * Validation and analysis of IP address-related columns (`ip.src_host`, `ip.dst_host`, `arp.src.proto_ipv4`, `arp.dst.proto_ipv4`).
  - **Target Variable Analysis:** In-depth exploration of `Attack_label` and `Attack_type` distributions to understand the nature of the target classes. The notebook identifies potential class imbalance issues within the dataset, which can bias machine learning models.
  - **Feature Engineering/Selection:** The notebook emphasizes selecting useful features from the dataset and dropping irrelevant ones based on domain knowledge.
  - **Machine Learning (Implied):** While specific model training steps are not fully provided in the snippet, the presence of `scikit-learn` and `GridSearchCV` indicates that machine learning models, likely a `RandomForestClassifier`, are tuned and evaluated to classify attack types.

## Installation

1.  Clone this repository:
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```
2.  Install the required Python packages (as indicated in the notebook):
    ```bash
    pip install matplotlib seaborn pandas numpy ydata_profiling missingno scikit-learn imbalanced-learn plotly
    ```
3.  Ensure you have the `ML-EdgeIIoT-dataset.csv` file in the same directory as the `GDSC.ipynb` notebook.

## Usage

1.  Open the Jupyter Notebook:
    ```bash
    jupyter notebook GDSC.ipynb
    ```
2.  Run through the cells to perform data loading, preprocessing, and analysis.
3.  Further develop the machine learning model as per the project's objectives.

## Attack Types Analyzed

The dataset used in this project includes a variety of cyberattack types, such as:

  * MITM
  * DDoS\_TCP
  * DDoS\_UDP
  * SQL\_injection
  * Ransomware
  * Normal traffic

## Contributing

Contributions are welcome\! Please feel free to open issues or submit pull requests.

## License

This project is licensed under the MIT License.
