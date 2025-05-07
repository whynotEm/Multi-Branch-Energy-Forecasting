# 📈 Multi-Branch Deep Learning Model for Energy Consumption Forecasting

This repository contains a **hybrid deep learning framework** for **energy consumption forecasting**, based on a multi-branch neural network architecture. The model integrates **convolutional**, **recurrent**, and **dense** representations to capture different aspects of temporal and local energy patterns.

---

## 🧠 Model Architecture

The model consists of **three parallel branches**:

- **Branch A (CNN)**: Extracts local temporal features using `Conv1D`.
- **Branch B (LSTM)**: Captures sequential dependencies through `LSTM`.
- **Branch C (Dense)**: Processes global context using fully connected layers.

All branches are concatenated and passed through dense layers to generate a final regression output.


---

## 🧪 Ablation Study

We conduct a thorough ablation study to assess the contribution of each branch:

- ✅ `full_model`: All three branches (CNN + LSTM + Dense)
- ❌ `model_without_A`: Without CNN
- ❌ `model_without_B`: Without LSTM
- ❌ `model_without_C`: Without Dense

Each model is trained and evaluated independently to measure its **Mean Squared Error (MSE)** on a test set.

---

## 📊 Results

Full model Test MSE: 0.2091
Model without Branch A (CNN): 0.2293
Model without Branch B (LSTM): 0.2833
Model without Branch C (Dense): 0.2725


---

## 📂 Dataset

We use the public dataset:

**📍 Renewable Energy Consumption in the U.S.**  
Available on Kaggle: https://www.kaggle.com/datasets/yuanchunhong/renewable-energy-consumption-in-the-us

