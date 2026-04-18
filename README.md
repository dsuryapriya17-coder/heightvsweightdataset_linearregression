# heightvsweightdataset_linearregression
📊 Height vs Weight Dataset – Linear Regression
📌 Overview

This project demonstrates Simple Linear Regression using a dataset that contains Height and Weight values. The goal is to understand the relationship between a person's height and weight and to predict weight based on height.

📁 Dataset Description

The dataset contains two main features:

Height (X) → Independent variable (input)
Weight (Y) → Dependent variable (output)
Example Data:
Height (cm)	Weight (kg)
150	50
155	55
160	60
165	65
170	70
🎯 Objective
To build a linear regression model
To find the relationship between height and weight
To predict weight for a given height
📐 Model Used

We use the Simple Linear Regression equation:

Y=b
0
	​

+b
1
	​

X

Where:

Y = Predicted Weight
X = Height
b₀ = Intercept
b₁ = Slope
⚙️ Steps Involved
Load the dataset
Separate input (Height) and output (Weight)
Train the linear regression model
Predict weight values
Visualize the results
🧪 Sample Python Code
import numpy as np
import matplotlib.pyplot as plt

# Dataset
height = np.array([150, 155, 160, 165, 170])
weight = np.array([50, 55, 60, 65, 70])

# Calculate mean
mean_x = np.mean(height)
mean_y = np.mean(weight)

# Calculate slope (b1)
num = np.sum((height - mean_x) * (weight - mean_y))
den = np.sum((height - mean_x)**2)
b1 = num / den

# Calculate intercept (b0)
b0 = mean_y - b1 * mean_x

print("Slope:", b1)
print("Intercept:", b0)

# Prediction
y_pred = b0 + b1 * height

# Plot
plt.scatter(height, weight, color='blue')
plt.plot(height, y_pred, color='red')
plt.xlabel("Height")
plt.ylabel("Weight")
plt.title("Height vs Weight Linear Regression")
plt.show()
📊 Output
A straight line showing the relationship between height and weight
Predicted values for weight based on height
📈 Applications
Health and fitness analysis
BMI estimation
Basic machine learning learning example
✅ Conclusion

This project shows how linear regression can model the relationship between two variables. It is one of the simplest and most important concepts in machine learning.
