# deep-learning-challenge

# Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.
From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.
# Instructions
Step 1: Preprocess the Data

Step 2: Compile, Train, and Evaluate the Model

Step 3: Optimize the Model

Step 4: Write a Report on the Neural Network Model

Step 5: Copy Files Into Your Repository

# Neural Network Model Report
### 1. Overview of the analysis: Explain the purpose of this analysis
This assignment aims to develop a deep learning binary classifier that can predict the success rate of funding applicants for Alphabet Soup, a nonprofit organization. The dataset I have contains information on over 34,000 organizations, including detailed application information, affiliations, government classification, funding use cases, income classification, funding amount requested, and fund utilization.
The analysis involves, first, preprocessing the data by removing unnecessary columns, encoding categorical variables, and splitting the dataset into training and testing sets. Next, a neural network model is designed, trained, and evaluated for its loss and accuracy. Optimization techniques, such as adjusting input data, modifying network architecture, activation functions, and training epochs, are applied to improve the model's performance.
The ultimate goal is to achieve a predictive accuracy of over 75%. Once optimized, the model is saved as an HDF5 file for future use.

### 2. Results: 

#### Data Preprocessing

* What variable(s) are the target(s) for your model?
 
ANS: The model's target variable is “IS_SUCCESSFUL,” indicating the success of a charity donation.

* What variable(s) are the features for your model?
  
ANS: The model's feature variables consist of all columns in the DataFrame except for “IS_SUCCESSFUL.”
  
* What variable(s) should be removed from the input data because they are neither targets nor features
  
ANS: I omitted the Employee Identification Number (EIN) from the feature and target selection as it does not contain relevant information for our predictive model. 
  
#### Compiling, Training, and Evaluating the Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why? 

ANS: In the "AlphabetSoupCharity_Optimization_3.ipynb" file, I configured a neural network model with three hidden layers containing 50, 80, and 50 neurons, respectively. After conducting multiple iterations and tests with different neuron numbers and layer configurations, I found that this specific combination yielded the best results in terms of accuracy and loss. I utilized the "relu" activation function for all three hidden layers to introduce non-linearity and enhance the model's performance. Lastly, I employed the sigmoid activation function for the final output layer to ensure the output remains within the 0 to 1 range, which is crucial for binary classification.

<img width="1072" alt="Screenshot 2024-05-23 at 6 19 40 PM" src="https://github.com/hatkiet/deep-learning-challenge/assets/154276115/c50fe918-28c6-4a83-8db4-22bb7fa43286">

Additionally, I experimented with a neural network model with all three hidden layers containing 80 neurons, but using the "tanh" activation function for the third layer in an attempt to improve accuracy and reduce loss in the "AlphabetSoupCharity_Optimization_4.ipynb" file.

<img width="1063" alt="Screenshot 2024-05-23 at 6 21 27 PM" src="https://github.com/hatkiet/deep-learning-challenge/assets/154276115/50fb0d03-75c7-4097-9347-4ddb0d5d6501">


* Were you able to achieve the target model performance?

ANS: I have managed to create an effective deep neural network model to forecast the success of organizations funded by Alphabet Soup. After refining the model through several optimizations, I attained a predictive accuracy exceeding 75%, ultimately achieving a final accuracy score of 79.58%. This model could serve as a valuable tool for Alphabet Soup in identifying applicants with the highest likelihood of success in their endeavors.

<img width="731" alt="Screenshot 2024-05-23 at 6 25 12 PM" src="https://github.com/hatkiet/deep-learning-challenge/assets/154276115/f639821d-fc4a-4dc7-8d64-5761033c2f9d">


* What steps did you take in your attempts to increase model performance?

ANS: The EIN column was excluded during the optimization process as it was deemed irrelevant. Retaining the NAME column improved model accuracy. To enhance the data, a threshold value was selected, and names occurring less than 5 times were substituted with "Other." A similar methodology was applied to the CLASSIFICATION column, where categories with fewer than 1000 occurrences were replaced with "Other." The resulting grouping was validated for accuracy.

<img width="735" alt="Screenshot 2024-05-23 at 6 26 39 PM" src="https://github.com/hatkiet/deep-learning-challenge/assets/154276115/3c5eb166-a214-4469-a759-3dfa2e908d65">

<img width="710" alt="Screenshot 2024-05-23 at 6 31 13 PM" src="https://github.com/hatkiet/deep-learning-challenge/assets/154276115/b1efd943-ac63-4e3c-845e-3d6cea73c45e">

<img width="856" alt="Screenshot 2024-05-23 at 6 31 25 PM" src="https://github.com/hatkiet/deep-learning-challenge/assets/154276115/d9bd04d1-2ea4-4834-a67c-b6426e977ce0">


### 3. Summary: 

The deep learning model used TensorFlow and Keras to achieve a predictive accuracy of 79.58% in classifying the success of Alphabet Soup-funded organizations. The model underwent several optimization attempts, including dropping columns, binning categorical variables, and adjusting layers and activation functions. Although the target accuracy of 75% was successfully achieved, it required significant optimization efforts to enhance loss and accuracy.

Consider exploring alternative models such as the Random Forest Classifier or Support Vector Machine (SVM) to improve classification. These models can effectively handle numerical and categorical variables, outliers, and imbalanced datasets, potentially enhancing classification performance.

[Note]: I have used our knowledge of Python and Neural Network Modeling (activities of Days 1 and 2 in class) to finish this challenge. 

