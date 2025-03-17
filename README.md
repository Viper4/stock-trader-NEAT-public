# stock-trader-NEAT-public
Public repo for my AI stock trader personal project.

The code is in a private repository. 
You can request access to view the code via email at vpr1618@gmail.com.

## Description
This is an implementation of the NEAT (Neuroevolution of Augmenting Topologies) genetic algorithm for stock trading.
The NEAT-python library (https://neat-python.readthedocs.io/en/latest/) was used for this project.

A recurrent neural network is trained using the NEAT genetic algorithm over historical stock data for a single stock ticker. 
I am not trying to create a god stock trader that can pick out its own stocks to trade and magically perform well on those newly found stocks. 
Instead, I choose the stock tickers I want the AI to train for, and individual networks are created to "specialize" in those specific stocks by training only for that stock.
The inputs provided to the AI are the stock's technical bar data (OHLCV), momentum indicators, and news sentiment on that stock. 
Additionally, the close price, volume, and news sentiment of the S&P 500 and the NASDAQ are also fed as inputs.
The news sentiment is calculated using an external NLP model called finBERT (https://huggingface.co/ProsusAI/finbert).

The outputs of the AI consist of a Buy/Sell indicator and a quantity value.

I am currently working on rewriting the code to use the tensorneat library so the training can run faster with GPU acceleration.

---
