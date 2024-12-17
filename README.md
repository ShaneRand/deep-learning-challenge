# deep-learning-challenge
Module 21 Challenge
Write a Report on the Neural Network Model
•	For this part of the assignment, you’ll write a report on the performance of the deep learning model you created for Alphabet Soup.
•	Overview of the analysis: Explain the purpose of this analysis.
o	The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.
o	From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. 
•	Results: Using bulleted lists and images to support your answers, address the following questions:
•	Data Preprocessing
o	What variable(s) are the target(s) for your model?
o	y = application_df['IS_SUCCESSFUL']

o	What variable(s) are the features for your model?

o	X = application_df.drop(columns=['IS_SUCCESSFUL'])
o	What variable(s) should be removed from the input data because they are neither targets nor features?
o	EIN, NAME
•	Compiling, Training, and Evaluating the Model
o	How many neurons, layers, and activation functions did you select for your neural network model, and why?
	This loop adds a variable number of hidden layers (between 1 and 5) to the model. For each layer, the number of neurons is also determined by Keras Tuner, ranging from 1 to 40.
	This adds the first hidden layer to the model. The number of neurons in this layer is determined by Keras Tuner, ranging from 1 to 80, in increments of 5.
	This allows Keras Tuner to choose between the ReLU and tanh activation functions for the hidden layers.
o	Were you able to achieve the target model performance?
	No – both models had accuracies of less than 75%.
o	What steps did you take in your attempts to increase model performance?
	Cut down classifications.
•	Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation
o	Overall – both models had about 72% accuracy.
o	While my models did not meet the desired performance goal of 75%, the optimization resulted in a lesser number of neurons.
o	 We could likely use a Random Forest algo – very well known in finance. Those models work with BIG DATA. Have to be careful not to overfit! They create random predictions from trees and then take an average of the results to create the model.
