# Handwritten Digit Recognition

## Introduction

This project implements a **Handwritten Digit Recognition** system using
a neural network built with TensorFlow/Keras. The model is trained on
pixel data representing handwritten digits (0--9) and predicts digit
labels from input images.

The workflow includes: - Data loading from CSV - Preprocessing and
normalization - One-hot encoding labels - Train/validation split -
Neural network training - Model evaluation - Test predictions

------------------------------------------------------------------------

## Table of Contents

-   Installation
-   Usage
-   Features
-   Dependencies
-   Dataset Format
-   Model Architecture
-   Training
-   Evaluation
-   Prediction
-   Troubleshooting
-   Contributors
-   License

------------------------------------------------------------------------

## Installation

``` bash
pip install numpy pandas matplotlib scikit-learn tensorflow
```

------------------------------------------------------------------------

## Usage

1.  Place dataset files:

```{=html}
<!-- -->
```
    Train.csv
    test.csv

2.  Run:

``` bash
jupyter notebook Handwritten_Digit_Recognition.ipynb
```

------------------------------------------------------------------------

## Features

-   CSV-based dataset loading
-   Data normalization
-   One-hot encoded labels
-   Train-validation split
-   TensorFlow/Keras neural network
-   Model accuracy visualization
-   Test dataset prediction

------------------------------------------------------------------------

## Dependencies

-   Python 3.x
-   NumPy
-   Pandas
-   Matplotlib
-   Scikit-learn
-   TensorFlow / Keras

------------------------------------------------------------------------

## Dataset Format

### Train.csv

-   First column: Label (0--9)
-   Remaining columns: Pixel values (784 values for 28×28 image)

### test.csv

-   Contains only pixel values
-   No labels

------------------------------------------------------------------------

## Model Architecture

    Input: (28, 28, 1)
    Flatten
    Dense (128, ReLU)
    Dense (10, Softmax)

Loss: categorical_crossentropy\
Optimizer: adam\
Metric: accuracy

------------------------------------------------------------------------

## Training

``` python
history = model.fit(
    X_train,
    y_train,
    epochs=10,
    batch_size=32,
    validation_data=(X_val, y_val)
)
```

------------------------------------------------------------------------

## Evaluation

``` python
val_loss, val_accuracy = model.evaluate(X_val, y_val)
```

------------------------------------------------------------------------

## Prediction

``` python
predictions = model.predict(X_test)
digits = predictions.argmax(axis=1)
```

------------------------------------------------------------------------

## Troubleshooting

**File not found**\
Check dataset paths.

**Shape mismatch**\
Ensure reshape to:

    (-1, 28, 28, 1)

------------------------------------------------------------------------

## Contributors

-   Your Name

## License

MIT License
