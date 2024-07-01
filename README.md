# preco_do_d-lar
Dados do Dólar ao longo do tempo frente ao real, verificação da desvalorização da moeda brasileira frente a moeda americana.

## Importando Bibliotecas

!pip install yfinance --upgrade --no-cache-dir
import yfinance as yf
yf.pdr_override()

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import pandas_datareader.data as web

## Obtendo Dados

tickers = ["USDBRL=X"]
carteira = web.get_data_yahoo(tickers)['Close']
start_date = '2000-01-01'

## Visualizando Dados

carteira.plot(subplots=True, figsize=(22,8))
plt.grid()
plt.show()
