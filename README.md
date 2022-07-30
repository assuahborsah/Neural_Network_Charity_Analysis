# Neural_Network_Charity_Analysis

# Overview of the analysis


A foundation, Alphabet Soup, wants to predict where to make investments. The goal is to use machine learning and neural networks to apply features on a provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. The initial file has 34,000 organizations and several columns that capture metadata about each organization from past successful fundings.

 Within this dataset are several columns that capture metadata about each organization, such as the following:
 
•	EIN and NAME—Identification columns
•	APPLICATION_TYPE—Alphabet Soup application type
•	AFFILIATION—Affiliated sector of industry
•	CLASSIFICATION—Government organization classification
•	USE_CASE—Use case for funding
•	ORGANIZATION—Organization type
•	STATUS—Active status
•	INCOME_AMT—Income classification
•	SPECIAL_CONSIDERATIONS—Special consideration for application
•	ASK_AMT—Funding amount requested
•	IS_SUCCESSFUL—Was the money used effectively


# Resources
Python, Visual Studio Code, Anaconda, Jupyter Notebook and Pandas.


# Results/Deliverables


## Data Preprocessing

•	What variable(s) are considered the target(s) for your model?

Checking to see if the target is marked as successful in the DataFrame, indicating that it has been successfully funded by AlphabetSoup.


•	What variable(s) are considered to be the features for your model?

The IS_SUCCESSFUL column is the feature chosen for this dataset.


•	What variable(s) are neither targets nor features, and should be removed from the input data?

The EIN and NAME columns will not increase the accuracy of the model and can be removed to improve code efficiency.

 
 ![image](https://user-images.githubusercontent.com/96086671/181934042-1c7a0a5b-37ae-4e72-bf93-874da953ab47.png)

 
## Compiling, Training, and Evaluating the Model


•	How many neurons, layers, and activation functions did you select for your neural network model, and why?

In the optimized model, layer 1 started with 110 neurons with a relu activation. For layer 2, it dropped to 80 neurons and continued with the relu activation. From there, the sigmoid activation seemed to be the better fit for layers 3 (40 neurons) and layer 4 (20 neurons).



![image](https://user-images.githubusercontent.com/96086671/181934060-1f71a412-f146-4dd1-bb76-81898cea318f.png)

 
•	Were you able to achieve the target model performance?
The target for the model was 75%, but the model produced 72.7%.

•	What steps did you take to try and increase model performance?

Columns were reviewed and the STATUS and SPECIAL_CONSIDERATIONS columns were dropped as well as increasing the number of neurons and layers. Other activations were tried such as tanh, but the range that model produced went from 40% to 68% accuracy. The linear activation produced the worst accuracy, around 28%. The relu activation at the early layers and sigmoid activation at the latter layers gave the best results.


![image](https://user-images.githubusercontent.com/96086671/181934071-6afd6916-cf9d-4372-9f13-0eb1eb186b59.png)

 
# Summary:

The relu and sigmoid activations yielded a 72.7% accuracy, which is the best the model could produce using various number of neurons and layers.
