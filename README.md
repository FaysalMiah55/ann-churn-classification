# ANN Churn Classification

This project aims to predict customer churn whether a person leave or not leave from the bank, using an Artificial Neural Network (ANN). The dataset used for this project is the "Churn_Modelling.csv" file, which contains information about customers of a bank.

## Project Structure


- `app.py`: Streamlit app for deploying the model.
- `Churn_Modelling.csv`: Dataset used for training and testing.
- `implementation.ipynb`: Jupyter notebook for model implementation and training.
- `label_en_gender.pkl`: Pickle file for label encoding gender.
- `logs/fit/`: Directory for storing training logs.
- `model.h5` and `model.keras`: Saved models.
- `onehot_en_geo.pkl`: Pickle file for one-hot encoding geography.
- `prediction.ipynb`: Jupyter notebook for making predictions.
- `requirements.txt`: List of dependencies.
- `scaler.pkl`: Pickle file for data scaling.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/ann-churn-classification.git
    cd ann-churn-classification
    ```

2. Create and activate a virtual environment:
     ```
    python -m venv myenv
    source myenv/bin/activate 
    ```

3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## Usage
Run the Streamlit app:
    ```
    streamlit run app.py
    ```

## Dataset
The dataset includes the following features:
- **RowNumber**: Index of the row.
- **CustomerId**: Unique identifier for the customer.
- **Surname**: Customer's surname.
- **CreditScore**: Customer's credit score.
- **Geography**: Customer's country.
- **Gender**: Customer's gender.
- **Age**: Customer's age.
- **Tenure**: Number of years the customer has been with the bank.
- **Balance**: Customer's account balance.
- **NumOfProducts**: Number of products the customer has with the bank.
- **HasCrCard**: Whether the customer has a credit card.
- **IsActiveMember**: Whether the customer is an active member.
- **EstimatedSalary**: Customer's estimated salary.
- **Exited**: Whether the customer has exited (target variable).

## Data Preprocessing
In data preprocessing section, droped some unnecessary features and dealing with categorical variables using label encoder(applied in Gender feature) and one hot encoder (applied in Geography feature) and save those in pkl file for furtur uses. Then split the dataset in training and testing set, applied feature scaling with standard Scaler also save it in pkl file.

## Model Building
The model is an Artificial Neural Network (ANN) implemented using TensorFlow and Keras. It predicts whether a customer will churn based on the provided features.

## Deploy in Streamlit
deploy this app in streamlit: https://ann-churn-classification-n9i8zoga4maz8xu78undcz.streamlit.app/

## License

This project is licensed under the MIT License.
