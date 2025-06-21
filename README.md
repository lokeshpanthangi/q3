# Fruit Classification with a Perceptron

This project implements a simple perceptron model from scratch using Python and NumPy to classify fruits (Apples vs. Bananas) based on their physical characteristics. The entire workflow, from data loading and preprocessing to model training and evaluation, is contained within the `percetron.ipynb` Jupyter Notebook.

## 🍎🍌 Project Overview

The goal of this project is to build a binary classifier that can distinguish between apples and bananas. The model is a single-layer perceptron with a sigmoid activation function, trained using gradient descent.

## 📊 Dataset

The dataset used for training and testing the model is `fruit.csv`. It contains 98 samples with the following features:

*   `length_cm`: The length of the fruit in centimeters.
*   `weight_g`: The weight of the fruit in grams.
*   `yellow_score`: A score from 0 to 1 indicating the yellowness of the fruit.
*   `label`: The class label, where `1` represents a banana and `0` represents an apple.

## 🚀 Getting Started

To run this project, you will need to have Python, Jupyter Notebook, and the following libraries installed:

*   NumPy
*   Pandas
*   Matplotlib
*   Scikit-learn

### Running the Project

1.  Clone this repository to your local machine.
2.  Ensure you have the required libraries installed (`pip install numpy pandas matplotlib scikit-learn`).
3.  Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
4.  Open the `percetron.ipynb` notebook and run the cells sequentially to see the model training and evaluation process.

## 📈 Results

The model is trained for 500 epochs and achieves **100% accuracy** on the held-out test set. The training process, including the decrease in loss and increase in accuracy over epochs, is visualized within the notebook.

The final trained model weights are saved to `model_weights.csv`.

## 🤖 Making Predictions

The notebook includes a function `predict_fruit` that can be used to classify a new, unseen fruit. You can provide the length, weight, and yellow score of a fruit to get a prediction.

Example:
```python
my_fruit = np.array([17.0, 140, 0.01]) # A long, light, not-so-yellow fruit
prediction, confidence = predict_fruit(my_fruit, train_mean, train_std, weights)
print(f"Prediction: '{prediction}' with {confidence:.2%} confidence.")
# Expected output: Prediction: 'Apple' with 0.10% confidence.
```

## 📝 Files

*   `percetron.ipynb`: Jupyter Notebook with the full implementation.
*   `fruit.csv`: The dataset.
*   `model_weights.csv`: The saved weights of the trained model.
*   `main.py`: Placeholder file. 