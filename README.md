# README for Support Vector Machine Visualization

## Overview
This Python project demonstrates a **Support Vector Machine (SVM)** classifier with linear kernel, visualizing the decision boundary on a 2D dataset.

## Features
- Loads data from a CSV file
- Trains an SVM model with linear kernel
- Visualizes data points and decision boundaries
- Displays support vector margins

## Requirements
- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib

## Installation
```bash
pip install pandas numpy scikit-learn matplotlib
```

## Usage

1. **Prepare your data**: Create a `Data.csv` file with features in columns and the target label in the last column.
   
   Example format:
   ```
   Feature1,Feature2,Label
   1.5,2.3,0
   2.1,3.4,1
   ...
   ```

2. **Run the script**:
   ```bash
   python svm_classifier.py
   ```

3. **View the output**: A matplotlib window will display the scatter plot with decision boundaries.

## How It Works

1. **Data Loading**: Reads features (X) and labels (y) from `Data.csv`
2. **Model Training**: Trains an SVM with:
   - Kernel: Linear
   - Regularization parameter (C): 0.5
3. **Visualization**: 
   - Blue/red points represent different classes
   - Solid black line: decision boundary
   - Dashed black lines: support vector margins (±1)

## Parameters

| Parameter | Value | Description |
|-----------|-------|-------------|
| kernel | 'linear' | Type of kernel function |
| C | 0.5 | Regularization strength (lower = more regularization) |
| grid points | 30×30 | Resolution of decision boundary mesh |

## Example Output
A 2D scatter plot with:
- Data points colored by class
- Decision boundary and margin lines
- Labeled axes (Feature 1, Feature 2)

## Notes
- Currently optimized for 2D datasets
- Modify grid resolution (30) for faster/more detailed boundaries
- Adjust C parameter to control overfitting

## License
MIT

---
## Contact
Mail: m14332121@gmail.com

---

Feel free to customize this README further based on your specific needs!
