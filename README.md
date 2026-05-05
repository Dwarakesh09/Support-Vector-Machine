# Support Vector Machine

A comprehensive Python implementation of Support Vector Machine (SVM) algorithms with detailed documentation and practical examples.

## Overview

This repository contains implementations of Support Vector Machine algorithms, demonstrating core machine learning concepts including classification, regression, and kernel methods. The project is designed for educational purposes and serves as a reference implementation for understanding SVM fundamentals.

## Features

- **Classification Models**: Binary and multi-class classification using SVM
- **Regression Support**: Support Vector Regression (SVR) implementation
- **Kernel Methods**: Multiple kernel implementations (linear, RBF, polynomial, sigmoid)
- **Data Preprocessing**: Utilities for data normalization and feature scaling
- **Evaluation Metrics**: Comprehensive model evaluation and performance analysis
- **Visualizations**: Plotting utilities for decision boundaries and model insights

## Requirements

- Python 3.7 or higher
- NumPy
- Scikit-learn
- Matplotlib
- Pandas

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Dwarakesh09/Support-Vector-Machine.git
cd Support-Vector-Machine
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Basic Classification Example

```python
from svm import SupportVectorMachine
from sklearn.datasets import load_iris

# Load dataset
iris = load_iris()
X, y = iris.data, iris.target

# Create and train model
model = SupportVectorMachine(kernel='rbf', C=1.0)
model.fit(X, y)

# Make predictions
predictions = model.predict(X)

# Evaluate
accuracy = model.score(X, y)
print(f"Accuracy: {accuracy:.4f}")
```

## Documentation

Detailed documentation for each module is available in the `docs/` directory:

- **[Algorithm Overview](docs/algorithm_overview.md)**: Theoretical foundations of SVMs
- **[API Reference](docs/api_reference.md)**: Complete function documentation
- **[Examples](examples/)**: Practical usage examples

## Project Structure

```
Support-Vector-Machine/
├── README.md
├── requirements.txt
├── src/
│   ├── svm.py                 # Core SVM implementation
│   ├── kernels.py             # Kernel implementations
│   └── utils.py               # Utility functions
├── examples/
│   ├── classification.py       # Classification examples
│   ├── regression.py           # Regression examples
│   └── visualization.py        # Visualization examples
└── tests/
    └── test_svm.py            # Unit tests
```

## Key Concepts

### Support Vector Machine
SVM is a supervised learning algorithm that finds the optimal hyperplane to separate different classes in a high-dimensional space. It's effective for both linear and non-linear classification problems through the use of kernel tricks.

### Kernel Methods
This implementation supports multiple kernel functions:
- **Linear**: Best for linearly separable data
- **RBF (Radial Basis Function)**: Effective for non-linear problems
- **Polynomial**: Useful for polynomial decision boundaries
- **Sigmoid**: Similar to neural network activation

## Performance

The implementation has been tested on various datasets including:
- Iris Dataset: ~97% accuracy
- MNIST Subset: ~95% accuracy
- Synthetic Datasets: Validated on custom non-linear problems

## Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Dwarakesh09**

## References

- Vapnik, V. (1995). The Nature of Statistical Learning Theory
- Cortes, C., & Vapnik, V. (1995). Support Vector Networks
- Schölkopf, B., & Smola, A. J. (2002). Learning with Kernels

## Disclaimer

This is an educational implementation. For production use, consider using established libraries like scikit-learn, which offer optimized and thoroughly tested SVM implementations.

---

For questions or issues, please open an [issue](https://github.com/Dwarakesh09/Support-Vector-Machine/issues) on GitHub.
