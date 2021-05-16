# Charity Analysis Using Neural Networks

## Overview
The purpose of this analysis was to use deep learning models to determine if a non-profit recipient of grant funds from AlphabetSoupCharity, was going to be successful in using those funds.  

- **Programs:** Jupyter Notebook, Python Tensor Flow

## Results
The analysis was grouped into 3 main groupings: Data Preprocessing; Compiling, Training, and Evaluating the Model; and Model Optimization.

#### Data Preprocessing
The data was split into target and features to feed into the deep learning model. Several columns were unused because they did not contribute to the analysis and therefore those columns were dropped from the analysis. 
- Target Data: IS_SUCCESSFUL
- Feature Data: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT
- Unused Data: EIN, and NAME

#### Compiling, Training, and Evaluating the Model
The deep learning model was set up with 2 hidden layers which yielded a total of 5,981 parameters. I chose the “3 or 2” times method when determining the number of neurons and with 44 columns of data chose the round number of 80 for the first layer and 30 for the second. 
- Neurons in Layer 1: 80
- Neurons in Layer 2: 30

#### Optimization
In order to improve model performance a series of 3 attempts were made at optimization. None of the optimizations had a material impact on the results which can be seen in the next section below.
- Optimization 1: Add additional neurons to the original layers (neurons per layer: 132 and 66)
- Optimization 2: Change activation function from ReLU to Tanh
- Optimization 3: Add a third and fourth hidden layer with 132,66,33, and 12 neurons.

### Overall Results
The final results are listed below.
![ Results](https://github.com/Brooks2210/Neural_Network_Charity_Analysis/blob/main/Results.png)
From this table we can see that the original model had a loss of 0.55 and accuracy of 0.73. The additional optimization attempts did not have any greater success than the original model. 

## Summary
The results of the model were less than optimal, and I would not suggest using a deep learning model on this type of data. The data was very categorical and even though in pre-processing we were able to convert it, I believe that the conversion to numerical data did not have the effect that we wanted. Deep learning could still be used to determine the success potential for grant recipients, but I would gather different types of data, such as years in operation, number of staff, number of people serviced by the non-profit, and credit scores of the organization. With the current type of data collected, a random forest learning model might work better.
