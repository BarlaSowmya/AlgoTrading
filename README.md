# AlgoTrading
Algo Trading System with ML & Automation – h2h_trial_2
This repository contains a Python-based automated trading system built using real-time market data, technical indicators, machine learning predictions, and seamless Google Sheets & Telegram integration.
Project Overview
Goal: To implement a complete mini-algo trading prototype that:

Fetches market data for 3 NIFTY 50 stocks (INFY.NS, TCS.NS, RELIANCE.NS)

Applies a technical trading strategy using RSI and SMA crossovers

Logs trades, profits, and performance metrics to Google Sheets

Predicts next-day stock movement using a Logistic Regression ML model

Sends real-time trade alerts to Telegram

Runs end-to-end with one function call
Strategy Logic
The core trading strategy follows:

Buy Signal: When RSI < 30 and 20-SMA crosses above 50-SMA

Sell Signal: When RSI > 70

Strategy is applied on intraday data (1-hour candles) for the past 60 days

Backtesting is performed over this period to measure trade success, win rate, and profit.
ML Integration
Model: Logistic Regression

Features used: RSI, SMA20, SMA50

Target: Predict whether price will rise in the next candle

Accuracy is computed and logged to Sheets

📊 Google Sheets Automation
The system writes results to a spreadsheet with three separate tabs:

Sheet Name	Purpose
P&L_Log	Logs total trades, win rate, profit, accuracy per stock
Trade_Log	Logs every individual BUY/SELL execution
Summary	Shows average win rate, ML accuracy, and total profit
You’ll need a service_account.json for Google Sheets API access.

💬 Telegram Alerts
The script also pushes trade execution alerts (BUY/SELL with price and time) to your Telegram account via a bot. You must set:

TELEGRAM_TOKEN → your bot token (from BotFather)

CHAT_ID → your Telegram user ID

🛠️ Installation
Clone this repo or upload the notebook to Google Colab

Upload your service_account.json

Replace your TELEGRAM_TOKEN and CHAT_ID

Run all cells
