# Neural_Network_Charity_Analysis
## Overview
Provided a dataset of over 34,000 organizations that have received funding from Alphabet Soup over the years, I must attempt to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results
For all attempts:
* Dropped the 'EIN' column
* Used OneHotEncoder to encode categorical variables

**Attempt #1**
* Dropped 'NAME' column
* Replaced 'Application_Type' with 'Other' if there were less than 700 
* Replaced 'Classification' with 'Other' if there were less than 1800
* 2 Hidden Layers
	* 80 Neurons
	* 30 Neurons
* Used Relu and Sigmoid Activations Functions
* Epochs: 100
* Accuracy: 72.54%

![Attempt 1](https://github.com/BlazeMedina/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt%201.png)
 

**Attempt #2**
* Replaced 'Application_Type' with 'Other' if there were less than 700 
* Replaced 'Classification' with 'Other' if there were less than 1800
* Replaced 'Name' with 'Other' if there were lass than 5 occurrences
	* This bins charities that have instances of less than 5 
* 2 Hidden Layers
	* 80 Neurons
	* 30 Neurons
* Used Relu and Sigmoid Activations Functions
* Epochs: 100
* Accuracy: 79.14%

![Attempt 2](https://github.com/BlazeMedina/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt%202.png)

**Attempt #3**
* Replaced 'Application_Type' with 'Other' if there were less than 700 
* Replaced 'Classification' with 'Other' if there were less than 1800
* Replaced 'Name' with 'Other' if there were lass than 5 occurrences
	* This bins charities that have instances of less than 5 
* 3 Hidden Layers
	* 80 Neurons
	* 50 Neurons
	* 30 Neurons
* Used Relu and Sigmoid Activations Functions
* Epochs: 100
* Accuracy: 79.02%

![Attempt 3](https://github.com/BlazeMedina/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt%203.png)

## Summary
The first attempt resulted in an accuracy of 72.54%.  I then decided to bin the charity names that had less than 5 occurrences.  Alphabet Soup's relationship with those charities is newer and not as well established.  After binning the 'NAME' column, the accuracy of the model was 79.14%.  I then attempted to add another layer to determine if it would improve the accuracy.  It did not.  The accuracy of the third attempt was 79.02%.  Therefore, the second attempt to predict whether applicants will be successful if funded by Alphabet Soup had the highest accuracy of the models tested.
