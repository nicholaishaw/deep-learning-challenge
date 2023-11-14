# Credit Risk Report

# Overview:
Choosing which organizations to fund is a complex process that requires a thorough assessment of different variables—the organizations' financial histories, types of organizations, and affiliations to name a few. Assessing each organization can be time-consuming, particularly when dealing with a large number of applications. However, certain supervised learning models can identify historical patterns of organizational success, examining common variables that indicate whether an investment is healthy or risky. As such, our model was developed to aid in the decision-making process of identifying organizations that have the highest likelihood of success. The dataset used to create this model comprised of information on 34,000 organizations who previously received funding. The dataset contained information of the organizations' success rate, organizational traits, and previous financial history.


# Results:
The target variable we used in our model was the binary classification of whether the previous investment was successful or not successful (0 indicating if it was not successful, 1 indicating if it was successful). The features used were the application type, the affiliated sector of the industry (independent, company sponsored, family/parent, national, regional, and other), government organization classification, what the funding was going to be used for, organization type (trust, association, co-operative, corporation), orgnaization income, and the amount of money the organization is requesting. Name, identification number, special considerations (a binary column of 0-organization did not have special considerations, and 1-the organization had special considerations), and organization activity status were removed from analyses in order to enhance the accuracy of the model. We binned the applications types and government organization classifications to include an 'other' category in order to condense the data to enhance the accuracy. Infrequent types of applications and government classifications were assigned to the 'other' category.

We used a deep neural net model for analysis. Data were split into training and test sets for pattern recognition, scaled appropriately, and then passed through the deep neural net. Within the neural net, we used three layers with 80 neurons in the first layer, 30 neurons in the second layer, and 1 neuron in the final output layer. We applied the relu activation function to the first two layers and the sigmoid function to the last layer. After fitting and compiling the model, we achieved an accuracy of 72.26%. As our target is 75.0% accuracy, we optimized the model by employing various techniques. 
    
First, we decreased the number of epochs (number of times the data were processed) from 100 to 50. Second, we dropped irrelevant columns such as EIN, name, special considerations, and organization activity. Third, we increased the 'other' category to include more application types and classifications. Last, we increased the number of neurons from 80 to 100 in the first layer and 30 to 50 neurons in the second layer. As a result, we achieved an accuracy of 72.27%.



# Summary:
Our model possesses reasonable accuracy with an accuracy score of 72.38% (i.e., the model is able to predict a successful investment 72.38% of the time). Given the moderate performance of the model, it is recommended that the model be used to assist with funding decisions after careful examination of the organizations' background information and financial histories.

# Outside Assistance:
Tutor David Chao assisted with the development of the logic and syntax of the code in the jupyter notebook files and assisted with the machine learning concepts for the report.
