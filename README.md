# Gradient-Descent-for-NN
# 📉 Gradient Descent: From Scratch vs. TensorFlow

How does a Neural Network actually learn? This repository explores the mathematical core of Machine Learning by implementing **Gradient Descent** from scratch using Python and NumPy, then validating the results against a professional **TensorFlow/Keras** implementation.

---

## 🛠️ The Tech Stack
* **Language:** Python
* **Deep Learning Framework:** TensorFlow & Keras
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib

---

## 🧠 Key Concepts Implemented

### 1. The Math of Learning
Gradient Descent is an optimization algorithm used to find the minimum of a cost function. In this project, I implemented:
* **Log Loss (Binary Cross-Entropy):** The cost function used to measure the error for binary classification.
* **Partial Derivatives:** Calculating the gradients for Weights ($w$) and Bias ($b$) to determine the direction of the "steepest descent."
* **Learning Rate ($\eta$):** Controlling the size of the steps taken toward the minimum.



### 2. Implementation from Scratch
I wrote a custom `gradient_descent` function that:
* Initializes weights to $1$ and bias to $0$.
* Iteratively updates parameters using the formula: 
  $$w_{new} = w_{old} - \eta \cdot \frac{\partial Loss}{\partial w}$$
* Prints the loss at every 50th epoch to track the model's convergence.

### 3. TensorFlow Comparison
To verify the scratch implementation, I built a single-layer Neural Network in Keras:
* **Optimizer:** Adam/SGD.
* **Loss:** binary_crossentropy.
* **Validation:** Compared the final weights and bias from TensorFlow with my custom function. **Result:** Both yielded nearly identical parameters!

---

## 📊 Dataset: Insurance Data
The model uses `insurance_data.csv` to predict if a person will buy insurance based on two features:
* **Age**
* **Affordability**

This simple binary classification task provides a clear way to visualize how the decision boundary shifts as the weights are optimized.

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git](https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git)

2. **Install Dependencies:**  pip install tensorflow pandas numpy matplotlib
   
3. **Execute:** Open GradientDescent.ipynb in Jupyter or VS Code to see the side-by-side comparison of the two approaches.
