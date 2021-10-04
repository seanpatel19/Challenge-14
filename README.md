# Challenge-14

## Venture Funding with Deep Learning

The business team has given you a CSV file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. The CSV file contains a variety of information about each business, including whether or not it ultimately became successful. With your knowledge of machine learning and neural networks, you decide to use the features in the provided dataset to create a binary classifier model that will predict whether an applicant will become a successful business.

Step 1: Read the applicants_data.csv file into a Pandas DataFrame. Review the DataFrame, looking for categorical variables that will need to be encoded, as well as columns that could eventually define your features and target variables. 

Step 2: Drop the “EIN” (Employer Identification Number) and “NAME” columns from the DataFrame, because they are not relevant to the binary classification model.

Step 3: Encode the dataset’s categorical variables using OneHotEncoder, and then place the encoded variables into a new DataFrame.

Step 4: Add the original DataFrame’s numerical variables to the DataFrame containing the encoded variables.

Step 5: Using the preprocessed data, create the features (X) and target (y) datasets. The target dataset should be defined by the preprocessed DataFrame column “IS_SUCCESSFUL”. The remaining columns should define the features dataset.

Step 6: Split the features and target sets into training and testing datasets.

Step 7: Use scikit-learn's StandardScaler to scale the features data.

Step 8: Create a deep neural network by assigning the number of input features, the number of layers, and the number of neurons on each layer using Tensorflow’s Keras.

Step 9: Compile and fit the model using the binary_crossentropy loss function, the adam optimizer, and the accuracy evaluation metric.

Step 10: Evaluate the model using the test data to determine the model’s loss and accuracy.

Step 11: Save and export your model to an HDF5 file, and name the file AlphabetSoup.h5.
 
Step 12: Repeat the above with different imputs to make the model better 




---

## Technologies
This application is written in Python 3.7  

this application uses the following packages:

Pandas 

Pathlib

Tensorflow

Sklearn

---

## Installation Guide

Before running the application first install the following dependencies.
See the associated Screenshot for what to Install 

![imports](https://github.com/seanpatel19/Challenge-13/blob/74b2e77213ce6b0059e8969e7c92c9712360d38a/Images/installs.jpg)




---

## Examples

Please see the following images of the code 

This is the code for compiling the model

![target balance](https://github.com/seanpatel19/Challenge-13/blob/74b2e77213ce6b0059e8969e7c92c9712360d38a/Images/nn%20code%20.jpg)



The results of the 3 models as it can be seen this is not a very successful model
![target balance](https://github.com/seanpatel19/Challenge-13/blob/74b2e77213ce6b0059e8969e7c92c9712360d38a/Images/model%20results.jpg)



---

## Usage

To use the data simply clone the repository. This can also be used via Google Collab but I chose jupyter notebook 

Different layers could be added as well ad different values of the layers 
```
---

## Contributors

Sean Patel (myself) seanpatel076@gmail.com
---

## License

License is public anyone can use or make changes to this application
