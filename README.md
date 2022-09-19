# Beijing-air-quality-prediction-internship

## Project Introduction
### 1. Introduction
This project has applied  Machine Learning and Deep Learning techniques to analyse and predict the Air Quality in Beijing. Our task is to predict one hour into the future the concentration level of air pollutant **PM2.5**.

For the machine learning part we used a lag of 2 hours, which we deducted using **PACF**.
But when in came to Deep learning we opted for a 48h lag because longer sequences gives better predictions.

### 2. Data
This data set includes hourly air pollutants data from 12 nationally-controlled air-quality monitoring sites. The air-quality data are from the Beijing Municipal Environmental Monitoring Center. The meteorological data in each air-quality site are matched with the nearest weather station from the China Meteorological Administration. The time period is from March 1st, 2013 to February 28th, 2017. Missing data are denoted as NA. [Link of the dataset](https://archive.ics.uci.edu/ml/datasets/Beijing+Multi-Site+Air-Quality+Data?fbclid=IwAR0SfBi3p0RYjQBL3Vh1QCDFdAkPP5VTj_JhMqQkIteHk-O1q4bjQYw7mOQ)

  **NW :**
- We merged this data into one CSV.
- Outlier detection and removal using box plot.
- KNNImputation to impute missing values.
- The link to this preporcessed data can be found here [Link of the dataset](https://www.kaggle.com/datasets/medali1992/beijing-air-quality-preprocessed)



### 3. PACF
We used this function to determine the appropriate lags **p** in an AR **(p)** model or in an extended ARIMA **(p,d,q)** model.
We choose for example the explanatory variable `PM10` and how it is correlated in time.
We noticed that all variable verify the same plot meaning the best lag is two.
![PACF](src/Images/PACF-plot.png)


### 4. Souce Code
The main project implementation files can be seen in the directory named **'src'**. The structure and description of this directory is shown as:
- src:
    - AirQualityData:
        - The preprocessed data.
    - DataPreprocessing.ipynb
        - The notebook mainly for data cleaning and data preprocessing.
    - Deep Learning
        - Pytorch LSTM Baseline .ipynb
        - Pytorch Attention LSTM Baseline.ipynb
        - Tabnet baseline.ipynb

    - Machine Learning
        - Catboost baseline.ipynb
        - Lightgbm-baseline.ipynb
        - Linear models baseline.ipynb
        - XGBOOST-Baseline.ipynb
    
### 6. Benchmark

| Model | RMSE | Kaggle | code | 
|:---|:---|:---|:---| 
| Catboost |10.29049 | [our work](https://www.kaggle.com/code/nourhadrich/catboost-baseline) | [this repo](https://github.com/medAli-ai/Beijing-air-quality-prediction-internship/blob/main/src/MachineLearning/Catboost%20Baseline.ipynb)| 
| Lightgbm |  9.43424 | [our work](https://www.kaggle.com/code/khalil20cherif/linear-models-baseline) | [this repo](https://github.com/medAli-ai/Beijing-air-quality-prediction-internship/blob/main/src/MachineLearning/lightgbm-baseline.ipynb)| 
| XGBOOST | 9.23511 | [our work]() | [this repo](https://github.com/medAli-ai/Beijing-air-quality-prediction-internship/blob/main/src/MachineLearning/XGBOOST-Baseline.ipynb)|
| Linear models | 12.29697 | [our work](https://www.kaggle.com/code/khalil20cherif/linear-models-baseline) | [this repo](https://github.com/medAli-ai/Beijing-air-quality-prediction-internship/blob/main/src/MachineLearning/Linear%20models%20baseline.ipynb)| 
| LSTM | 15.45468 | [our work](https://www.kaggle.com/code/medali1992/beijing-pytorch-lstm-baseline) | [this repo](https://github.com/medAli-ai/Beijing-air-quality-prediction-internship/blob/main/src/Deep%20Learning/Pytorch%20LSTM%20Baseline.ipynb)| 
| Attention LSTM | 14.51535 | [our work](https://www.kaggle.com/code/medali1992/beijing-pytorch-attention-lstm-baseline) | [this repo](https://github.com/medAli-ai/Beijing-air-quality-prediction-internship/blob/main/src/Deep%20Learning/Pytorch%20Attention%20LSTM%20Baseline.ipynb)| 
| Tabnet | 10.38852 | [our work](https://www.kaggle.com/code/medali1992/aug-tps-tabnetclassifier) | [this repo](https://github.com/medAli-ai/Beijing-air-quality-prediction-internship/blob/main/src/MachineLearning/Tabnet%20baseline.ipynb)|

## Prediction plot
![Prediction](src/Images/prediction-plot.png)



### Collaborators <!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<!-- ALL-CONTRIBUTORS-BADGE:END -->

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
<table>
  <tr>
   <td align="center">
         <a href="https://github.com/medAli-ai"><img src="https://avatars.githubusercontent.com/u/42294664?v=4" width=100px alt="med ali"/> 
         <br/>
         <sub><b>Mohamed Ali Bouchhioua</b></sub></a><br /><a href="https://github.com/medAli-ai" title="Code">💻</a> 
   </td>
   <td align="center">
         <a href="https://github.com/2nour"><img src="https://avatars.githubusercontent.com/u/52534067?v=4" width=100px alt="2nour"/> 
         <br/>
         <sub><b>Nour Hadrich</b></sub></a><br /><a href="https://github.com/2nour" title="Code">💻</a> 
   </td>
   </tr>
   
   

</table>




            
