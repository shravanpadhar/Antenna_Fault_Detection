#  Antenna Fault Detection & Diagnostics
### *Automated Classification of Physical Degradation using Machine Learning*

A comprehensive machine learning project designed to detect and classify physical faults in modern antenna systems by mapping electromagnetic signatures to structural conditions.

## 📋 Project Overview
Traditional antenna maintenance relies on time-consuming and often dangerous manual inspections. This project provides a **data-driven alternative**, utilizing RF parameters to automatically identify physical degradation. By analyzing features such as Return Loss and VSWR, we can distinguish between healthy systems and various failure modes like bending, humidity, or broken elements.


## 🎯 Objectives
* **Exploratory Data Analysis (EDA):** Identify patterns in electromagnetic signatures across different fault types.
* **Unsupervised Clustering:** Apply K-Means to validate the natural grouping of physical faults.
* **Model Development:** Build high-precision classifiers to automate fault detection.
* **Model Evaluation:** Compare performance across multiple algorithms (Random Forest, SVM, Logistic Regression).

## 📊 Dataset
* **Dataset Source:** [Kaggle - Antenna Fault Detection Dataset](https://www.kaggle.com/datasets/amineipad/antenna-fault-detection-dataset)
* **Dataset Creator:** [Amine Amn (amineipad)](https://www.kaggle.com/amineipad)
* **Size:** 1,500 perfectly balanced samples
* **Target Variable:** `Fault_Type` (0 = Healthy/OK, 1-5 = Specific Faults)
* **Key Features:** * **S11 (dB):** Return Loss
    * **VSWR:** Voltage Standing Wave Ratio
    * **Gain (dBi):** Antenna Gain
    * **Eff (%):** Radiation Efficiency
    * **BW (MHz):** Bandwidth
    * **Z_Real/Z_Imag:** Complex Input Impedance

### Dataset Credits
This project uses the "Antenna Fault Detection Dataset" created by Amine Amn. We extend our gratitude for providing this high-quality, ML-ready synthetic dataset for research.

## 🚀 Getting Started

### Prerequisites
```text
python >= 3.8
pandas >= 1.3.0
numpy >= 1.21.0
matplotlib >= 3.4.0
seaborn >= 0.11.0
scikit-learn >= 1.0.0
```
## 🚀 Installation & Getting Started

### 1. Clone the Repository
```bash
git clone [https://github.com/YOUR_USERNAME/Antenna_Fault_Detection.git](https://github.com/YOUR_USERNAME/Antenna_Fault_Detection.git)
cd Antenna_Fault_Detection
```
### 2. Install Dependencies
```bash
pip install -r requirements.txt
```
### 3. Load the Dataset
```bash
import kagglehub

# Download latest version
path = kagglehub.dataset_download("amineipad/antenna-fault-detection-dataset")
print("Path to dataset files:", path)
```
## 📁 Project Structure

```text
Antenna_Fault_Detection/
│
├── Dataset/
│   └── antenna_dataset.csv                     
│
├── notebooks/
│   └── rf-fault-detection-k-means-tiers.ipynb  # Main EDA & Modeling notebook
│
├── .gitignore
├── README.md
└── requirements.txt
```

## 📓 Notebooks
### 1. RF Fault Detection & Classification
File: rf-fault-detection-k-means-tiers-random-forest.ipynb
Author: Shravan Padhar

### Key Steps:
* **Data Cleaning:** IQR-based outlier removal and Z-score normalization.
* **Clustering:** Elbow Method analysis showing an optimal k=6 (matching the 6 physical conditions).
* **Classification:** Training and comparison of Random Forest, SVM, and Gradient Boosting.
* **Interpretability:** Visualizing the distinction between "Healthy" and "Degraded" states via scatter plots.

## 🔍 Key Findings from EDA
* **Perfect Separability:** The electromagnetic signatures of the six fault types are highly distinct, allowing for near-perfect classification.
* **Critical Features:** Gain, Efficiency, and Bandwidth show the highest variance across fault types.
* **Physical-Digital Correlation:** Unsupervised clusters aligned 1:1 with known fault labels, validating that physical changes create unique mathematical fingerprints in the RF spectrum.

## 🛠️ Technologies Used
* Python 3.8+
* Scikit-learn: For Random Forest, SVM, and K-Means.
* Pandas & NumPy: For data engineering.
* Seaborn & Matplotlib: For high-quality RF signature visualization.

##  📈 Project Status
* Data Cleaning & Preprocessing
* Exploratory Data Analysis
* Unsupervised Clustering (K-Means)
* Model Development (Random Forest/SVM)
* Model Evaluation
* Real-time Monitoring API Integration

## 📝 License
This project is for educational and research purposes. Please refer to the original dataset license on Kaggle (MIT/Public Domain).

## 📧 Contact
* Notebook Author: Shravan Padhar[Shravan Padhar (shravanpadhar)](https://www.kaggle.com/shravanpadhar)
* Project Link: [Kaggle Notebook](https://www.kaggle.com/code/shravanpadhar/rf-fault-detection-k-means-tiers-random-forest)
* For questions or suggestions, please open an issue in this repository.


