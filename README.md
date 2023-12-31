# Olivia's Deep Learning Assignment
## UofT Data Analytics Bootcamp Module 21 Challenge

### Table Of Contents
1. [Preprocessing](#preprocessing)
2. [Neural Network Model](#neural-network-model)
3. [Usage](#usage)

## Preprocessing
The preprocessing steps performed on the dataset are as follows:
1. The dataset is read from the `charity_data.csv` file using Pandas.
2. The non-beneficial ID columns, 'EIN' and 'NAME', are dropped.
3. The number of unique values in each column is determined.
4. The `APPLICATION_TYPE` column is analyzed, and a cutoff value is chosen to bin "rare" categorical variables together as "Other". The corresponding rows in the dataframe are replaced accordingly.
5. The success counts for each application type are checked to ensure successful binning.
6. The `CLASSIFICATION` column is analyzed, and a cutoff value is chosen to bin "rare" classifications together as "Other". The corresponding rows in the dataframe are replaced accordingly.
7. The success counts for each classification are checked to ensure successful binning.
8. Categorical variables in the dataframe are encoded using one-hot encoding with `pd.get_dummies`.
9. The preprocessed data is split into features (`X`) and target (`y`) arrays.
10. The preprocessed data is further split into training and testing datasets using `train_test_split`.
11. The features datasets (`X_train` and `X_test`) are scaled using `StandardScaler` to normalize the data.

## Neural Network Model
The neural network model is built and trained using TensorFlow:
1. The model is defined as a sequential model with multiple layers.
2. The first hidden layer has 80 units and uses the ReLU activation function.
3. The second hidden layer has 30 units and uses the ReLU activation function.
4. The output layer has 1 unit and uses the sigmoid activation function.
5. The model is compiled with the binary cross-entropy loss function, the Adam optimizer, and accuracy as the evaluation metric.
6. The model is trained for 100 epochs using the training data.
7. The model is evaluated using the testing data to calculate the loss and accuracy.
8. The trained model is saved as an HDF5 file named "trained_application.h5" for future use.

## Usage
To use this code:
1. Ensure you have the necessary dependencies installed, including scikit-learn, pandas, and TensorFlow.
2. Clone this repository to your local machine.
3. Place the `charity_data.csv` file in the same directory as the Jupyter Notebook or Python script.
4. Open the Jupyter Notebook or Python script and run the code.
5. The preprocessing steps will be performed on the dataset, and the neural network model will be trained and evaluated.
6. The trained model will be saved as "trained_application.h5" for future use.

[Back To Top](#olivias-deep-learning-assignment)