# Neural_Network_Charity_Analysis

## Project overview

The purpose of this project is to use machine learning and neural networks to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. The CSV file contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are several columns that capture metadata about each organization, such as the following:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Resources

- Data Source: `charity_data.csv`
- Data Tools: `Pandas`, `tensorflow`, `scikit-learn`
- Software: `Jupyter Notebook`

## Results

### Data Preprocessing

- Column removed from the input data as it wasn't a target nor feature variable.

![image](https://user-images.githubusercontent.com/91766276/157544838-6d0ba2f0-d981-4b66-873c-b75582a6a1ad.png)

- Determined which variables needed binning.

![image](https://user-images.githubusercontent.com/91766276/157545077-8950aedb-7ff2-457d-b766-b08092ecf45d.png)

- Binning `APPLICATION_TYPE`, `CLASSIFICATION` and `NAME` variables.

![image](https://user-images.githubusercontent.com/91766276/157545395-9d9e6fc8-9cb5-491c-a1b7-284b0d9be12c.png)
![image](https://user-images.githubusercontent.com/91766276/157545473-c02162b4-f7a5-436b-9001-46b4e8c41460.png)
![image](https://user-images.githubusercontent.com/91766276/157545528-379327e4-8629-4e0d-a523-ad999cd43ac1.png)

- Generated categorical variables and encoded them using OneHotEncoder.

![image](https://user-images.githubusercontent.com/91766276/157546269-891c30c6-6afa-46cf-ba8e-f2bf6dfff1f2.png)

### Compiling, Training, and Evaluating the Model

- Merged the encoded variables with the initial DataFrame, dropping the original categorical variables.

![image](https://user-images.githubusercontent.com/91766276/157548648-6b933820-c8f8-4c31-8a6d-8869b481770c.png)

- Splited processed the data leaving `IS_SUCCESSFUL` as the target array, then scaled the data.

![image](https://user-images.githubusercontent.com/91766276/157549230-5aba0846-6ee0-46b4-a77a-9ad7ba4e7ca1.png)

- Defined the model with three `Hidden_Layers`, increased the number of nodes to achieve a target predictive accuracy higher than 75%.

![image](https://user-images.githubusercontent.com/91766276/157549685-d4cf252a-c67c-40f4-bd68-94af128a3487.png)

- Used `100` epochs and saved the model's weights every 5 epochs.

![image](https://user-images.githubusercontent.com/91766276/157549925-e38c6acc-9288-4ac1-962e-4cbb77872ac9.png)

- Evaluated the model and exported to HDF5 file.

![image](https://user-images.githubusercontent.com/91766276/157550150-683cb3fb-05c6-48fb-af16-38160b6a9aae.png)

## Summary

The original model achieved a predictive accuracy of `0.72`, the optimized model was able to achieve a predictive accuracy of `0.76` exceeding the `0.75` target by doing the following: dropped less columns than the original model, created an additional bin for `NAME` variable, decreased the number of values for all the created bins, increased the number of hidden layers to `3` and added more neurons to the hidden layers. Finally, I would recommend using `Random Forest` model to solve this project because this model only handles tabular and is able to achieve comparable predictive accuracy on tabular data which is the case for the provided dataset. 

- Here is an example of the predictive accuracy that the `Random Forest` model achieved.

![image](https://user-images.githubusercontent.com/91766276/157553292-4bbf4045-9c77-4deb-91b0-d9a3c633e08e.png)




