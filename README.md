# freqtrade-trading-strategies
contains strategies for using freqtrade. Please be aware they are supposed to show off some of the indicators and concepts you can use with freqtrade and might not be great for investing purposes. So please use them on your own risk.

A lot of these also helped me just to understand the api and play with some ideas. The only onces I considered worth it to further work on are the ones listed below.

If you really like them, or think I lost enough money testing them, please feel free to shoot me a donation in btc at:

1AoyvVpGSg9TatyCNZbTgkQveFHZXssutW


## Backtesting Results

These are just backtesting results. Nobody know's how this will perform in a bull/bear/sideways market.

### Simple:

2018-05-01 21:37:18,094 - freqtrade.optimize.backtesting - INFO - Measuring data from 2018-04-12T04:40:00+00:00 up to 2018-05-02T04:30:00+00:00 (19 days)..

```
==================================== BACKTESTING REPORT ====================================
pair        buy count    avg profit %    total profit BTC    avg duration    profit    loss
--------  -----------  --------------  ------------------  --------------  --------  ------
BTC_ETH            13            1.16          0.00150821           600.0        13       0
BTC_LTC             2            1.24          0.00024830           685.0         2       0
BTC_ETC             2            1.26          0.00025439           515.0         2       0
BTC_POWR            3            2.94          0.00091145           433.3         3       0
BTC_XMR             2            1.37          0.00027446           357.5         2       0
TOTAL              22            1.44          0.00319681           555.2        22       0

```

``` javascript
  "max_open_trades": 1,
  "stake_currency": "BTC",
  "stake_amount": 0.01,

  "experimental": {
    "use_sell_signal": true,
    "sell_profit_only": true
  }
```

### Quickie:

```
2018-05-01 21:41:24,313 - freqtrade.optimize.backtesting - INFO - Measuring data from 2018-04-12T04:40:00+00:00 up to 2018-05-02T04:35:00+00:00 (19 days)..
2018-05-01 21:41:24,927 - freqtrade.optimize.backtesting - INFO -
==================================== BACKTESTING REPORT ====================================
pair        buy count    avg profit %    total profit BTC    avg duration    profit    loss
--------  -----------  --------------  ------------------  --------------  --------  ------
BTC_ETH            17            0.64          0.00109456           510.3        17       0
BTC_LTC             7            0.68          0.00048056           489.3         7       0
BTC_ETC             4            0.99          0.00039919           187.5         4       0
BTC_DASH            4            0.92          0.00037095           178.8         4       0
BTC_ZEC             3            0.72          0.00021597           278.3         3       0
BTC_XLM             2            0.89          0.00017956           350.0         2       0
BTC_NXT             4            0.83          0.00033445           160.0         4       0
BTC_POWR            4            1.54          0.00062234           250.0         4       0
BTC_ADA             5            0.75          0.00037910           641.0         5       0
BTC_XMR             3            0.71          0.00021304           483.3         3       0
TOTAL              53            0.81          0.00428972           403.7        53       0

```

``` javascript
  "max_open_trades": 1,
  "stake_currency": "BTC",
  "stake_amount": 0.01,

  "experimental": {
    "use_sell_signal": true,
    "sell_profit_only": true
  }
```

### ReinforcedQuickie

```
2018-05-07 16:25:13,675 - freqtrade.optimize.backtesting - INFO - Measuring data from 2018-01-10T04:55:00+00:00 up to 2018-05-07T20:55:00+00:00 (117 days)..
2018-05-07 16:25:15,955 - freqtrade.optimize.backtesting - INFO -
==================================== BACKTESTING REPORT ====================================
pair        buy count    avg profit %    total profit BTC    avg duration    profit    loss
--------  -----------  --------------  ------------------  --------------  --------  ------
ETH/BTC            94           -0.03         -0.00031933           461.2        81      13
LTC/BTC            45            0.05          0.00020906           375.1        38       7
ETC/BTC            39            0.45          0.00175444           244.1        35       4
DASH/BTC           22           -1.20         -0.00263321           337.7        14       8
XLM/BTC            24            0.46          0.00108829           173.5        21       3
POWR/BTC           10            0.42          0.00042175           165.5         9       1
XMR/BTC            20            0.93          0.00184997           268.0        19       1
TOTAL             254            0.09          0.00237097           347.9       217      37
           37            0.58          0.00209264            76.2        32       5

```

``` javascript
  "max_open_trades": 1,
  "stake_currency": "BTC",
  "stake_amount": 0.01,

  "experimental": {
    "use_sell_signal": true,
    "sell_profit_only": true
  }
```

### ClucMay72018

```
2018-05-07 16:26:20,833 - freqtrade.optimize.backtesting - INFO - Using local backtesting data (using whitelist in given config) ...
2018-05-07 16:26:22,997 - freqtrade.optimize.backtesting - INFO - Measuring data from 2018-01-10T04:55:00+00:00 up to 2018-05-07T20:55:00+00:00 (117 days)..
2018-05-07 16:26:24,085 - freqtrade.optimize.backtesting - INFO -
==================================== BACKTESTING REPORT ====================================
pair        buy count    avg profit %    total profit BTC    avg duration    profit    loss
--------  -----------  --------------  ------------------  --------------  --------  ------
ETH/BTC             1            2.03          0.00019834            10.0         1       0
LTC/BTC             1            2.53          0.00024453            15.0         1       0
ETC/BTC             6            0.24          0.00013575           130.8         5       1
DASH/BTC            2            2.50          0.00048673           480.0         2       0
XLM/BTC            14            1.45          0.00198838            35.0        14       0
POWR/BTC           12           -0.34         -0.00039685            43.8         9       3
XMR/BTC             1           -5.67         -0.00056424            35.0         0       1
TOTAL              37            0.58          0.00209264            76.2        32       5
```

``` javascript
  "max_open_trades": 1,
  "stake_currency": "BTC",
  "stake_amount": 0.01,

  "experimental": {
    "use_sell_signal": true,
    "sell_profit_only": true
  }
```
