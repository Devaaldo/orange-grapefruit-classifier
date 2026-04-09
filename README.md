# Fruit Classification with Neural Networks: Orange vs Grapefruit

Binary classification of oranges and grapefruits using a feedforward neural network trained on physical and color features.

## Dataset

Source: [Kaggle — Oranges vs Grapefruit](https://www.kaggle.com/datasets/joshmcadams/oranges-vs-grapefruit)

| Feature | Type | Description |
|---------|------|-------------|
| diameter | float | Physical diameter of the fruit |
| weight | float | Physical weight of the fruit |
| red | int | Red channel value (0–255) |
| green | int | Green channel value (0–255) |
| blue | int | Blue channel value (0–255) |

10,000 samples — 5,000 oranges, 5,000 grapefruits (balanced).

## Project Structure

```
orange-grapefruit-classifier/
├── notebooks/
│   └── orange-vs-grapefruit.ipynb   # Full pipeline notebook
├── data/                             # Place dataset CSV here (not tracked)
├── requirements.txt
├── .gitignore
└── README.md
```

## Pipeline

1. **EDA** — class distribution, feature histograms, correlation heatmap, boxplots
2. **Preprocessing** — label encoding, train-test split (70/30, stratified), MinMaxScaler (fit on train only)
3. **Model** — Sequential NN: `Input(5)` → `Dense(64, relu)` → `Dropout(0.3)` → `Dense(32, relu)` → `Dropout(0.2)` → `Dense(1, sigmoid)`
4. **Evaluation** — accuracy, loss curves, classification report, confusion matrix

## Results

| Metric | Score |
|--------|-------|
| Test Accuracy | ~92% |
| Optimizer | Adam |
| Loss | Binary Crossentropy |

## Setup

```bash
git clone https://github.com/Devaaldo/orange-grapefruit-classifier.git
cd orange-grapefruit-classifier
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/orange-vs-grapefruit.ipynb
```

## Tech Stack

Python 3.x, TensorFlow/Keras, scikit-learn, Pandas, NumPy, Matplotlib, Seaborn
