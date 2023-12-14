# Project 4

## Business Case

The business case/task is to try and predict which drivers will submit a claim based on their customer data.

## Feature Engineering and Feature Selection
To better navigate the data and help models learn, feature engineering was implemented in the form of Principal Component Analysis (PCA) to reduce the number of features. Feature selection was implemented in the form of filtering, specifically selecting features that demonstrated non-collinearity.

## Explanatory Visualizations on 2 of the 10 most important features

### Driving Experience and Insurance Claims

The visualization below shows insight into the relationship between driving experience and filing an insurance claim ('OUTCOME'). By looking at the first range of driving experience (0-9), it's apparent that the highest number of drivers (about 2,200) filing claims this year had less than 10 years of driving experience.

 ![](https://github.com/EhLeeOod/project-4-part-1/blob/main/Data/experience_viz.PNG?raw=true)

### Marriage and Insurance Claims

The visualization below shows insight into the relationship between a driver's marriage (0 = not married, 1 = married) status and filing an insurance claim (0 = not filed, 1 = filed). We can see here that the number of claims filed by unmarried drivers (about 2,000) is about twice as many as those filed by married drivers.

![](https://github.com/EhLeeOod/project-4-part-1/blob/main/Data/marriage_viz.PNG?raw=true)

## Summary: Neural Network, Training Metrics, and Final Evaluation Metrics
Original KNN Model:

                precision    recall  f1-score  

           0       0.86      0.88      0.87      
           1       0.71      0.69      0.70       

         accuracy                           0.82     

 KNN with PCA Model:

                precision    recall  f1-score   
           0       0.86      0.87      0.86      
           1       0.70      0.68      0.69      

    accuracy                           0.81 

KNN with non-collinearity:

                 precision    recall  f1-score
           0       0.90      0.75      0.82 
           1       0.60      0.81      0.69      

    accuracy                           0.77 

Original Neural Network Model:

                precision    recall  f1-score

           0       0.87      0.90      0.89      
           1       0.76      0.72      0.74      

    accuracy                           0.84 

Tuned Neural Network Model:

accuracy: 0.8376 - recall: 0.6950 - precision: 0.7616

# The best model, recommended for production, is the original neural network model due to it outperforming the other models in accuracy (0.84) and precision (0.76)
