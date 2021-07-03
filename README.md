# Neural_Network_Charity_Analysis

# Overview of the Analysis 
The goal of this project is to deliver a binary classifier that can help a nonprofit predict where it should invest int resources. The non profit is tasked with sorting though several application for grants and wants to understand is a model can help predict what application will be successful based on historical data that it has collected. The model chosen for the project is Keras which is a deep learning models running on the tenserFlow platform. 

# Results 

##Data Processing 
Date was sourced into Jupiter notebooks for cleaning and model training. 2 column EDI and Nam were dropped from the data set as they would not contribute to anything in the final out put. In addition to dropping columns the data was reviewed for binning. Application type and classification had more than 10 unique variables. Both sets of data were plated for density and to aid in the binning (Add image)

The date was then created to a list and the categorical data was converted to numerics using skylark one hot encoder. A new data frame with the converted data was merged back onto the original data frame and the existing data (that was converted) dropped leaving a clean numerical data.  The data was then split into Test and Train with the Y being defined as Is_Successful and the Is_unsucessful column being dropped. 
		
##Compiling, Training and Evaluating the model
		
Layer and neurons - after the data was scaled the models designed with two hidden Relu layers and out signed out put layer. The nodes within the rely layers were 80 and 30 
(Inset model table) 
 
target model performance - The model was then compiled for loss to use binary crossentrophy, it was optimized with Adam and the metric was loss. 100 epoch were selected with saving after every 5 epochs. He model yielded an accuracy score of 72% 

Several passed at optimizing the model were performed including the following 
	Additional nodes and a hidden relu layer  resulting in accuracy 47% 
	changed out put layer from Sigmoid to Tanh which also resulted in similar accuracy.
	Changed a hidden layer from relu to Sigmoid resulting in 69% accuracy. 
			
# Summary Additional scenarios testing of different model structures should be performed if accuracy great than 72% is required. The data should also be compared again randome forest to see if a with in models help increase accuracy. Lastly the data should also be scenario tested to determine what column can be removed to increase accuracy. 
