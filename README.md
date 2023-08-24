## Module 21 Challenge
# deep_learning_challenge

Overview of Analysis: 
- The purpose of this analysis was to build a model that will successfully identify applicants that will be successful if funded by non-profit foundation Alphabet Soup.
- Using neural network technology, the model will be a binary classifier which uses metadata on organisations that that received funding from Alphabet Soup in the past.

Data Pre-processing:
- Target variable: 'IS_SUCCESSFUL'
- Feature variables: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION' 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', ASK_AMT'
- Removed variables (neither targets nor features): 'EIN', 'NAME'

Results:
- In the optimised model ('alphabet_soup_classifier_v2') the total number of nodes actually decreased (from a total of 110 to 90), although the optimised model included three hidden layers, as opposed to two in the original model.
- A sigmiod function was used as the output layer, given its effectiveness with binary classification datasets (the model we are building is a binary classifier). However, a variety of different activation functions for the hidden layers were tested, with a combination of ReLU and LeakyReLU producing the best results.
- The number of hidden layers increased from 2 to 3 between the original and optimmised model (as the additional hidden layer yielded better accuracy scores).
- Model testing also showed that a reduction in the number of epochs, from 50 in the original model to 25 in the optimised model, resulted in an improvement in the accuracy of the model. Higher model accuracy as a result of a reduction in epochs can be a result of model over-fitting (with the higher number of epochs).
- Unfortunately, despite many testing iterations, the target model performance of 75% was not able to be achieved. The optimised model had an accuracy score of 72.96%.
- In summary, whilst the model was not able to produce the target accuracy score of 75%, it came close and therefore still has reasonable explanatory insight when it comes to assisting Alphabet Soup to select successful venture applicants. Being able to select successful ventures with ~73% accuracy is impressive, especially given the typically high failure rates of new ventures.
- Random forest machine learning could also be used to build a classification model to help Alphabet Soup select applicants with the best chance of success. The neural network model that we built for this project produced higher accuracy scores with a relatively small number of epochs (25). This indicates that the model was likely at risk of over-fitting the data. One strength of random forest machine learning models is their ability to handle complex datasets whilst mitigating overfitting, which is likely to be useful for the dataset in question.