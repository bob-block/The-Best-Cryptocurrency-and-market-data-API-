# The-Best-Cryptocurrency-and-market-data-API-

Nowadays, more and more people pay attention to digital currency development and want to find an API that provides basic information, market data, etc. of digital currencies such as BTC and eth. In fact, you could consider trying Block.cc.
Block.cc has various types of API interfaces, is dedicated to developers, and is easy to access. Block.cc included 500+ exchanges, 10,000+ currencies, 28,000+ trading pairs, and 1000+ business users. It covers multi-dimensional data such as real-time price, currency information, K-line data, legal currency exchange rate, transaction depth, news flash, block data, and historical transactions.

Access URLs

REST API

https://data.block.cc/api/v3

Websocket Feed

wss://data.block.cc/ws/v3

Access to Block.cc

Before using Block.cc API, you need to register an account and apply for an API Key before developing.
You can provide an API key in a REST API call in the following ways:

1. Preferred method: Via a custom request header named X-API-KEY

2. Convenient method: pass a query string parameter named api_key

The API key can only be provided in the Websocket API via a query string parameter named api_key

example:

curl -X GET \-H 'X-API-KEY: [YOUR_API_KEY]' \'https://data.block.cc/api/v3/markets'

curl -X GET \'https://data.block.cc/api/v3/markets?api_key=[YOUR_API_KEY]'

wscat -c 'wss://data.block.cc/ws/v3?api_key=[YOUR_API_KEY]

Example request:

(1) Binance Exchange information can be obtained through the Block.cc  API

curl -X GET \ 
  'https://data.block.cc/api/v3/markets/binance'

return:

 [
 
  {
  
    "slug": "binance",
    
    "fullname": "Binance",
    
    "websiteUrl": "https://www.binance.com/",
    
    "volume": 2490122366.2343,
    
    "reportedVolume": 2490122366.2343,
    
    "expectedVolume": 2490122366.2343,
    
    "monthlyVisits": 19386372.159024935,
    
    "status": "enable",
    
    "kline": true,
    
    "spot": true,
    
    "futures": false
    
  },
  
  {
  
    "slug": "okex",
    
    "fullname": "OKEX",
    
    "websiteUrl": "https://www.okex.com",
    
    "volume": 2490122366.2343,
    
    "reportedVolume": 2490122366.2343,
    
    "expectedVolume": 2490122366.2343,
    
    "monthlyVisits": 19386372.159024935,
    
    "status": "enable",
    
    "kline": true,
    
    "spot": true,
    
    "futures": false
    
  }
  
]

（2）BTC Bitcoin prices can be obtained through the Block.cc  API

curl -X GET \'https://data.block.cc/api/v3/price?slug=bitcoin,filecoin'

Response:

   [
   
  {
  
    "s": "bitcoin",
    
    "S": "BTC",
    
    "T": 1564201016247,
    
    "u": 10254.613,
    
    "b": 1,
    
    "a": 66180.407,
    
    "v": 663551832.77,
    
    "ra": 68260.277,
    
    "rv": 684890110,
    
    "m": 182193710000,
    
    "c": 0.0111,
    
    "h": 10254,
    
    "l": 10254,
    
    "cw": 0.0111,
    
    "hw": 10254,
    
    "lw": 10254,
    
    "cm": 0.0111,
    
    "hm": 10254,
    
    "lm": 10254,
    
    "ha": 10254,
    
    "la": 10254
    
  }
  
]

If you want to know more about Block.cc, you can visit the website below or read the API documentation

Website：https://pro.block.cc/
API docs:https://blockcc-api-document.pages.dev/en_US/#changelog
