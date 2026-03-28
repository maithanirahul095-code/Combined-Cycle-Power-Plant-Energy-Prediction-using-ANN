# CCPP Energy Yield Prediction: A PyTorch Deep Learning Approach

This project implements an **Artificial Neural Network (ANN)** to predict the net hourly electrical energy output ($PE$) of a Combined Cycle Power Plant (CCPP). By leveraging environmental ambient variables, the model provides an automated way to forecast energy production with high precision.

## 📌 Project Overview
The goal is to model the non-linear relationship between environmental conditions and a power plant's electrical output. The dataset comprises **9,568 data points** collected over six years of plant operation.

### Dataset Features:
* **AT (Ambient Temperature):** Measured in $^\circ C$.
* **V (Exhaust Vacuum):** Measured in cm Hg.
* **AP (Ambient Pressure):** Measured in millibar.
* **RH (Relative Humidity):** Measured as a percentage.
* **PE (Energy Output):** The target variable (Net hourly electrical energy output in MW).

## 🛠️ Technical Stack
* **Framework:** PyTorch (Deep Learning)
* **Libraries:** Pandas, NumPy, Scikit-Learn
* **Visualization:** Matplotlib

## 🏗️ Model Architecture
The model is a **Feedforward Multi-Layer Perceptron (MLP)** designed specifically for regression tasks:

1.  **Input Layer:** 4 neurons (matching the environmental features).
2.  **Hidden Layer 1:** 6 neurons with **ReLU** activation to capture non-linearities.
3.  **Hidden Layer 2:** 6 neurons with **ReLU** activation.
4.  **Output Layer:** 1 neuron (Linear) to predict the continuous $PE$ value.

### Training Configuration:
* **Optimizer:** Adam
* **Loss Function:** Mean Squared Error (MSE)
* **Scaling:** Features were normalized using `StandardScaler` for faster convergence.
* **Persistence:** The training loop includes a "Best Model" save mechanism that exports the model weights (`best_model.pt`) whenever validation loss improves.

## 📊 Evaluation Results
The model's performance is measured using the **$R^2$ Score** and **Mean Squared Error (MSE)**.

* **Training MSE:** [Insert your result here]
* **Testing MSE:** [Insert your result here]
* **$R^2$ Score:** [Insert your result here]

