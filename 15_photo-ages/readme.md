# 15. Age Detection by Photo.
A chain supermarket introduces a computer vision system to analyze customer photos taken at the checkout area. This system enables age detection for analyzing purchases and suggesting relevant products based on customer age and for monitoring cashiers' compliance with regulations regarding alcohol sales.

[HTML](15_photo-ages.html) [ipynb](15_photo-ages.ipynb)
### Goal: 
Develop a CNN-based ML model to detect the age of customers from their photos.<br>
Target performance metric: **MAE < 8**.
### Data: 
A collection of photos of people with age indications. Data taken from [ChaLearn Looking at People](https://chalearnlap.cvc.uab.cat/dataset/26/description/).
### Framework:
-	Data overview and exploratory data analysis.
-	Model training.
-	Model testing.
-	General conclusion about trained model performance.
### Result: 
The pre-trained `ResNet50 model`, with a learning rate of 0.0002, successfully predicted a person's age from their photo, **MAE=7** years after 5 epochs.<br> 
The MAE was employed as the loss function, and ReLU served as the activation function for the last neuron. It is worth noting that the validation loss exceeded the training set, suggesting the presence of overfitting.<br> 
To improve the model prediction an error analysis may be performed. This analysis can help to uncover the age groups where the model more frequently errs. The training dataset can be augmented with additional data from those specific age ranges. 
### Stack: 
- `Pandas`, `Matplotlib`, `NumPy`, `TensorFlow.Keras` 
- *Adam, ResNet50*
