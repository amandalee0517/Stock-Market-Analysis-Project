# Stock-Market-Analysis-Project
### Instructer by Jose Portilla from Pierian Data
I'll be analyzing stock data related to a few car companies, from Jan 1 2012 to Dec 1 2020.

```python
import pandas as pd
import numpy as np
%matplotlib inline
import matplotlib.pyplot as plt
import pandas_datareader.data as web
import datetime

start = datetime.datetime(2015, 1, 1)
end = datetime.datetime(2020, 12, 1)
```

## Getting the data
Tesla Stock (Ticker: TSLA on the NASDAQ), Ford and General Motors (GM)

```python
Tesla = web.DataReader("TSLA", 'yahoo', start, end)
Ford = web.DataReader("F", 'yahoo', start, end)
GM = web.DataReader("GM", 'yahoo', start, end)
```

## Visualizing the data
```python
Tesla['Open'].plot(label='Tesla',figsize=(16,9),title='Open Price')
Ford['Open'].plot(label='Ford')
GM['Open'].plot(label='GM')
plt.legend();
```
### Open Price Trend
![Open Price Line Plot](https://github.com/amandalee0517/Stock-Market-Analysis-Project/blob/main/OpenPriceLinePlot.png)

```python
Tesla['Volume'].plot(label='Tesla',figsize=(16,9),title='Volume Trends')
Ford['Volume'].plot(label='Ford')
GM['Volume'].plot(label='GM')
plt.legend();
```
### Volume Trend
![Volume Trend](https://github.com/amandalee0517/Stock-Market-Analysis-Project/blob/main/VolumeTrend.png)


**What happened on the maximun trading volumne for Tesla?**

