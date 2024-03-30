Stock-Market-Price-Predictor

This project explores stock price prediction using a Long Short-Term Memory (LSTM) network in Python and its deployment as a web application with Streamlit.

Model Creation

The core functionality involves building an LSTM model to predict future closing prices based on historical stock data. Here's a breakdown of the process:

Data Acquisition: We use the yfinance library to download historical closing prices for a specified stock ticker symbol.
Data Preprocessing:
Moving averages (MA50, MA100, MA200) are calculated to identify trends.
The data is normalized using MinMaxScaler for better model training.
The data is split into training and testing sets.
Model Building:
A sequential LSTM model is created with multiple LSTM layers for effective pattern learning.
The model is trained on the training data, optimizing hyperparameters like epochs and batch size.
Evaluation:
The model's performance is evaluated on the testing data.
Predicted vs. actual closing prices are plotted for visualization.
Model Saving:
The trained model is saved for future use in deployment (Stock_Predictions_Model.keras).
Deployment with Streamlit

The trained model is then deployed as a user-friendly web application using Streamlit:

Web App Setup: The app.py script utilizes Streamlit to create the web interface.
User Interaction:
Users can enter a stock symbol in a text input field.
The app retrieves and displays the corresponding stock data.
Price vs. Moving Average charts are generated for visual analysis.
The model predicts future closing prices for the entered stock.
A chart comparing the original and predicted prices is displayed.
Getting Started

This section guides you through setting up and running the project:

Prerequisites

Python 3.x
Required libraries:
numpy
pandas
matplotlib.pyplot
yfinance
keras (or tensorflow.keras for TensorFlow 2.x)
streamlit
Installation

Ensure you have Python and the required libraries installed. You can install them using pip:

Bash
pip install numpy pandas matplotlib yfinance keras streamlit


 Clone this repository:

Bash
git clone https://github.com/gunjanmhjn/Stock-Market.git


 Running the Model

Train the model: Run the script stock_market_predictor.py. This script performs all the model creation steps mentioned earlier.
Running the Web App

After training the model, launch the web application:

Bash
streamlit run app.py


 This will open the app in your web browser (usually at http://localhost:8501/).

Customization

Edit stock_market_predictor.py to:
Change the default stock symbol used for model training.
Adjust hyperparameters for the LSTM model.
Edit app.py to customize the Streamlit app's layout and styling (refer to Streamlit documentation).
Disclaimer

This is an educational project. Stock price prediction is complex, and this model may not be accurate for real-world trading decisions.
