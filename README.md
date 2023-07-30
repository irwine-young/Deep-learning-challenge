# Deep-learning-challenge

## Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the bestchance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use thefeatures in the provided dataset to create a binary classifi er that can predict whether applicants will be successful iffunded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organisations thathave received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capturemetadata about each organisation, such as:
1. EIN and NAME — Identification columns
2. APPLICATION_TYPE — Alphabet Soup application type
3. AFFILIATION — Affiliated sector of industry
4. CLASSIFICATION — Government organisation classification
5. USE_CASE — Use case for funding
6. ORGANIZATION — Organisation type
7. STATUS — Active status
8. INCOME_AMT — Income classification
9. SPECIAL_CONSIDERATIONS — Special considerations for application
10. ASK_AMT — Funding amount requested
11. IS_SUCCESSFUL — Was the money used effectively

## Steps
1. Preprocess the data by identifying required columns, dropping columns, understanding the column features
2. Split the preprocessed data into features array X, and target array y with train_test_split function
3. Create a binary classification model for prediction of success based on the datasets
4. Create Neural Network Model through assigning the number of features, number of nodes in each layer, and number of layers required.
5. Compile and train the model through set number of epochs.
6. Evaluate (accuary and loss) the mode using the test data
7. Save and export results to an HDF5.

## Optimisation of the Model. 
The model accuracy and loss for main and optimisation 1-3 were the following:

# Optimisation Main:
268/268 - 1s - loss: 0.5634 - accuracy: 0.7282 - 509ms/epoch - 2ms/step
Loss: 0.5634280443191528, Accuracy: 0.7281632423400879

# Optimisation 1:
268/268 - 0s - loss: 0.5686 - accuracy: 0.7248 - 464ms/epoch - 2ms/step
Loss: 0.5685680508613586, Accuracy: 0.724781334400177

# Optimisation 2: 
268/268 - 0s - loss: 0.5606 - accuracy: 0.7289 - 460ms/epoch - 2ms/step
Loss: 0.5605754852294922, Accuracy: 0.728863000869751

# Optimisation 3: 
268/268 - 1s - loss: 0.5941 - accuracy: 0.7292 - 510ms/epoch - 2ms/step
Loss: 0.5940616726875305, Accuracy: 0.7292128205299377

These optimisation were made by altering the number of hidden layers and number of nodes for the model, which still yield a lower accuracy. (<0.75)

However, for optimisation 4, instead of dropping the "Name" feature in the initial dataset, we've include the "Name" into the neural network model, replace all the bin count of < 50 as others to simplify the "Names" feature column. This model yields better accuracy than the initial 4 models with only nodes and layers modifications.

# Optimisation 4:
268/268 - 1s - loss: 0.5677 - accuracy: 0.7620 - 541ms/epoch - 2ms/step
Loss: 0.5676767826080322, Accuracy: 0.7619825005531311

## Conclusion:
Overall, it is necessary to include the "Names" feature into the neural network as it increases the accuracy. A further RandomForestClassifier model can be used to give an idea of feature importance, to fully optimise the dataset prior to Neural Network model, removing features that has lower importance. 
