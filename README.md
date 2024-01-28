CryptoSlayer: A Trading Bot via Kraken API

## Overview

We are embarking on the development of an innovative cryptocurrency trading bot, leveraging the Kraken API for real-time market data. Our approach integrates machine learning to discern market trends from historical data, enabling the identification of optimal strategies and indicators.

The trading bot will undergo simulated trading runs on a dedicated server, mimicking live market conditions. Throughout these simulated runs, machine learning algorithms will assess the appropriateness of entry and exit points, enhancing the bot's decision-making capabilities.

---

## Technologies

Our analytical work is conducted within a Jupyter notebook, seamlessly utilizing Python for data processing and analysis. Key technologies include:

* [Google Colab](https://colab.research.google.com/): An online Jupyter notebook providing an ideal environment for code execution and collaboration.

* [Support Vector Machines (SVM)](https://scikit-learn.org/stable/modules/svm.html): Leveraging SVM for effective machine learning model training.

* [Naive Bayes](https://scikit-learn.org/stable/modules/naive_bayes.html): Employing Naive Bayes algorithms for robust model training.

---

## Setup Guide

To ensure smooth execution of our trading bot, follow the installation guide by importing the necessary libraries and modules. Key imports include:

python
import base64
import fire
import hashlib
import hmac
import importlib
import json
import krakenex
import numpy as np
import pandas as pd
import questionary
import requests
import re
import Source.Bot as bot
import urllib.parse

from pykrakenapi import KrakenAPI
from API.Endpoints import KrakenEndpoints
from API import KrakenRequests
from finta import TA
from Helper import Utilities as util
from matplotlib.pyplot import plot
from pandas import DataFrame
from pandas.tseries.offsets import DateOffset
from pykrakenapi import KrakenAPI
from os import listdir
from os.path import isfile
from sklearn import svm
from sklearn import naive_bayes
from sklearn.naive_bayes import ComplementNB
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import classification_report, confusion_matrix
from Source.BaseStrategy import BaseStrategy
from Source.Kraken import Kraken


---

## Data Preparation

The foundation of our analysis involves extracting data from the Kraken Public API, specifically OHLC (Open, High, Low, Close) data. This data is organized into a DataFrame, facilitating comprehensive analysis and visualization.

---

## Machine / Deep Learning Modeling

Our trading strategy integrates Support Vector Classifiers (SVC) to forecast optimal entry and exit points. SVC is chosen for its efficiency in handling large datasets.

---

## Evaluation Report

* *Key Findings:*
  * Backtesting runs revealed suboptimal bot performance, indicating potential areas for improvement.

  * Optimization opportunities include refining training and test data to address potential overfitting or underfitting issues.

* *Conclusion:*
  * The current trading strategy encompasses the core strategy and a machine learning algorithm for entry and exit determinations. Critical to future success is the inclusion of robust risk management practices, encompassing position sizing, stop-losses, take-profits, and trade diversification.
