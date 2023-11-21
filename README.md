# Finance: Stock Portfolio Management Web App
<h2>CS50 Project - Week 9</h2>

Check out the complete assignment details [here](https://cs50.harvard.edu/x/2023/psets/9/finance/).

<img width="819" alt="screenshot" src="https://github.com/andreiii14/CS50-Finance/assets/128039153/4b5cdea6-08a6-4a08-8361-529c198833e2">

## Technologies Used
- Python
- Flask with session authentication
- SQL
- HTML
- CSS
- Bootstrap

## Project Overview
Finance is a web application that enables authenticated users to simulate buying and selling stocks using virtual currency. It also provides real-time stock quotes fetched from the IEX API and allows users to track their stock portfolio transaction history.

## Features:
- **User Registration**: Users can easily register for an account by providing their name, email address, and password.
- **Stock Quotes**: Access real-time stock quotes by entering the stock symbol.
- **Buying and Selling**: Trade stocks by specifying the number of shares to buy or sell and the stock symbol.
- **Portfolio Management**: View your current holdings, including the number of shares owned, purchase price, and current market value of each stock.

## How to Run
1. Clone this repository.

2. Navigate to the project directory and execute the following commands:

    - Activate a virtual environment: `python3 -m venv .venv` and select the virtual environment as the active workspace.
    - Install dependencies: `pip install -r requirements.txt`.
    - Set Flask environment variable: `export FLASK_APP=application.py`.
    - Configure and export your API key following the provided instructions.
    - Run the command: `flask run` to launch the app on localhost.

Upon opening the finance site in your browser, register for a new account (upper right corner) to create your personalized stock portfolio.

## Views
- **Register**: Allows new users to register for an account, displaying an apology view if the form data is incomplete or if the chosen username already exists in the database.
- **Index**: The homepage displays a table summarizing the logged-in user's owned stocks, including the number of shares, current stock price, and the value of each holding. This view also shows the user's virtual "cash" balance and the total value of their "cash" plus stock holdings.
- **Quote**: Enables users to look up a stock's current price by submitting a form, retrieving real-time data from the IEX API. An error message is rendered if the stock symbol is invalid.
- **Buy**: Allows users to "buy" stocks by submitting a form with the stock's symbol and the desired number of shares. The system checks the validity of the stock symbol and ensures the user can afford the purchase at the current market price with their available balance. Transaction history is stored in the database.
- **Sell**: Enables users to "sell" shares of any stock currently owned in their portfolio.
- **History**: Displays a table summarizing the user's past transactions, listing whether the stock was bought or sold, the stock's symbol, buy/sell price, the number of shares, and the transaction date/time.

---

Please note that the Login and Logout functions, along with all functions in helpers.py, were part of the assignment's starter code and are not my original work. Starter code ©2020 David J. Malan/Harvard.
