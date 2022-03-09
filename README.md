# Neural_Network_Charity_Analysis

## Project overview

The purpose of this project is to use machine learning and neural networks to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The CSV file contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

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

- Column removed from the input data as it wasn't a target nor feauture variable.

![image](https://user-images.githubusercontent.com/91766276/157544838-6d0ba2f0-d981-4b66-873c-b75582a6a1ad.png)

- Determined which variables needed binning.

![image](https://user-images.githubusercontent.com/91766276/157545077-8950aedb-7ff2-457d-b766-b08092ecf45d.png)

- Binning `APPLICATION_TYPE`, `CLASSIFICATION` and `NAME` variables.

![image](https://user-images.githubusercontent.com/91766276/157545395-9d9e6fc8-9cb5-491c-a1b7-284b0d9be12c.png)
![image](https://user-images.githubusercontent.com/91766276/157545473-c02162b4-f7a5-436b-9001-46b4e8c41460.png)
![image](https://user-images.githubusercontent.com/91766276/157545528-379327e4-8629-4e0d-a523-ad999cd43ac1.png)

- Generated categorical variables and encoded them using OneHotEncoder.

![image](https://user-images.githubusercontent.com/91766276/157546269-891c30c6-6afa-46cf-ba8e-f2bf6dfff1f2.png)

