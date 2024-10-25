# RL4Trading

In this project, we are implementing a Reinforcement Learning algorithm for financial data analysis.

Acces to report : 
- [Report](RL4Trading_Final.pdf)

## Data Structure

* We source our data from Yahoo Finance via their API, specifically focusing on the closing prices for our modeling purposes.

## Model Architecture

### Environment

* Our environment comprises:
  - A dataframe containing stock price data,
  - A specified time range for action consideration,
  - A balance representing investable funds,
  - A record of the number of shares held at each time step.

### Actions

* Our action space encompasses three distinct types:
  1. Buying a certain proportion of stocks based on the model's confidence in a buy strategy.
  2. Selling a certain proportion of stocks based on the model's confidence in a sell strategy.
  3. Taking no action.

<p align="center">
  <img src="images/scatter.png" alt="First model with LSTM layer" width="400"/>
  <img src="images/bars.png" alt="Second model with Transformer layer" width="400"/>
</p>
<p align="center"><b>Representation of the actions taken and their proportion</b></p>


### Deep Q-Network (DQN)

* Our DQN architecture is a blend of various layers, notably incorporating LSTM due to the sequential nature of trading data. Additionally, it considers other relevant factors such as the number of stocks held and the current account balance.

<p align="center">
  <img src="images/model1.png" alt="First model with LSTM layer" width="400"/>
  <img src="images/model2.png" alt="Second model with Transformer layer" width="400"/>
</p>
<p align="center"><b>Two models using combination of RNN and Transformers to predict the next price value</b></p>

## Results

<p align="center">
  <img src="images/triangle.png" alt="Action taken during the time" width="400"/>
  <img src="images/wealth.png" alt="Evolution of the wealth" width="400"/>
</p>
<p align="center"><b>Action taken over time and evolution of the value of the account</b></p>

## How to Use the Notebook

To utilize this notebook effectively, follow these steps:

1. Locate the Classes:
   - The classes required for this notebook are located in the "utils" folder. Ensure that you have access to this folder and its contents.

2. Fetch Financial Data:
   - Run the "get_financial_data.ipynb" notebook to understand how to fetch financial data. This step is crucial for gathering the necessary data for analysis.

3. Understand Reinforcement Learning Process:
   - After fetching financial data, run the "start.ipynb" notebook to comprehend the reinforcement learning process. This notebook will guide you through the steps involved in reinforcement learning for financial analysis.

By following these steps, you can effectively utilize the notebook and gain insights into financial data using reinforcement learning techniques.
