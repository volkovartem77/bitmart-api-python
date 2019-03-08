# bitmart-api-python
This is a simple Python wrapper for Bitmart REST API
> Full docs https://github.com/bitmartexchange/bitmart-official-api-docs

### Usage

```python
from bitmart_api import *

api_key = '<your api key>'
secret_key = '<your secret key>'

title = '<title>'
```

> title is a name of your API key that you set when registered your key.
```python
bitmart = Bitmart(api_key, secret_key, title)
```

##### Public Endpoints

```python
print(bitmart.ping())
print(bitmart.time())
print(bitmart.steps())
print(bitmart.currencies())
print(bitmart.symbols())
print(bitmart.symbols_details())
print(bitmart.ticker('ETH_BTC'))
print(bitmart.kline('ETH_BTC', 15, 1525760116000, 1525769116000))
print(bitmart.orderbook('ETH_BTC', 6))
print(bitmart.trades('ETH_BTC'))
```

##### Authenticated Endpoints

```python
print(bitmart.wallet())
print(bitmart.place_order('ETH_BTC', 1, 1, 'buy'))
print(bitmart.cancel_order(564654))
print(bitmart.cancel_all_order('ETH_BTC', 'buy'))
print(bitmart.list_orders('ETH_BTC', 0, 0, 100))
print(bitmart.order_details(123232))
```

##### Service

```python
print(bitmart.precision)
```
