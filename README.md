# Neural Network Charity Analysis

## Overview
The purpose of this week's challenge was to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. To do this I created a neural network model to determine the success rate, and a second model with a target accuracy of 75%.

## Results
### Data Preprocessing
During the preprocessing stage, there were several variables to keep in mind:
- The target of the analysis was to determine "would an applicant would be successful if we invest in them?". This was detailed in the "IS_SUCCESSFUL" column of the dataframe
- The features for my model was the data in the following columns
  - APPLICATION_TYPE
  - AFFILIATION 
  - CLASSIFICATION
  - USE_CASE
  - ORGANIZATION
  - STATUS
  - INCOME_AMT
  - SPECIAL_CONSIDERATIONS
  - ASK_AMT
- The "EIN" and "NAME" columns were neither targets nor features, so they were removed from the input data.

![application_df](https://user-images.githubusercontent.com/88118759/148706467-df0f8d16-73ba-4295-8df6-38bc2e310b78.PNG)

### Compiling, Training, and Evaluating the Model
For my neural network model, I used 2 hidden layers with "ReLU" activation functions consisting of 80 and 30 neurons, and the "Sigmoid" activation function for the output layer. I chose to use the "ReLU" activations due to their advantages in analyzing large, nonlinear data, and will be more efficient computational load. I used the "Sigmoid" activation in the output layer again due to the large, nonlinear data and it will produce a 0 or 1 value which is what I need.
![neural_network_model](https://user-images.githubusercontent.com/88118759/148706923-9dc4c608-7dbe-4694-9224-e8cfc4939d70.PNG)

I did not achieve the target performance of 75% accuracy but I was fairly close with a 72.9% result.

![neural_network_accuracy](https://user-images.githubusercontent.com/88118759/148706957-b17ec7fc-0fb7-4ed7-81c4-714ea506f9c0.PNG)

I attempted to increase this accuracy by changing the model activation functions to "tanh" on attempt 1, and this yielded an accuracy of 73%.

![attempt1](https://user-images.githubusercontent.com/88118759/148707179-e905730c-2e07-46ff-b824-1acc85259531.PNG)

I changed the number of neurons used in the hidden layers and used a combination of "tanh" and "ReLU" activations for attempt 2, yielding an accuracy of 73%.

![attempt2](https://user-images.githubusercontent.com/88118759/148707181-070cdb5d-db17-43f9-b519-b34086f4e801.PNG)

And for the 3rd attempt, I used a combination of "ReLU" and "tanh" activations for the first and second hidden layers, respectively and I increased the number of epochs back to 50. This resulted in an accuracy of 72.9%.

![attempt3](https://user-images.githubusercontent.com/88118759/148707184-81019a39-9614-43d7-be06-91b7349ace00.PNG)

## Summary
To summarize, the results did not meet the target of 75% although were very close. I believe that using the ReLU function is the right way to go, but I would test with different layer and neuron configurations to reach the desired accuracy.
