# Orange vs Grapefruit Classifier

A deep learning model to classify oranges and grapefruits based on their physical characteristics and color values using Keras neural networks.

## Dataset

The dataset contains 10,000 fruit samples with the following features:

- **Diameter** (float): Physical diameter of the fruit
- **Weight** (float): Physical weight of the fruit
- **Color Values** (RGB): Red, Green, Blue color channels (0-255)

### Data Distribution

- Oranges: 5,000 samples
- Grapefruits: 5,000 samples

## Project Structure

```
orange-vs-grapefruit/
├── orange-vs-grapefruit.ipynb    # Main Jupyter notebook with full pipeline
├── README.md                       # This file
└── .gitignore                      # Git ignore configuration
```

## Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **scikit-learn** - Machine learning utilities & preprocessing
- **Keras** - Deep learning framework
- **NumPy** - Numerical computations

## Pipeline Overview

### 1. Data Collection

- Dataset source: Kaggle - Oranges vs Grapefruit
  - Download: https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit
- Contains 10,000 samples with 6 features (name, diameter, weight, red, green, blue)

### 2. Data Preprocessing

- Label encoding for fruit names (Orange: 1, Grapefruit: 0)
- Feature scaling using MinMaxScaler (normalize to 0-1 range)
- Train-test split (70% training, 30% testing)
