# Order book fetcher

_[apis/poloniex/public/Order book fetcher]_

![icon](</assets/icons/33d6ca66-d216-4c2b-b2ae-87685c291a6f.png>)

---

Returns the order book for a given market, as well as a sequence number used by websockets for synchronization of book updates and an indicator specifying whether the market is frozen. You may set currencyPair to "all" to get the order books of all markets.<br>
<br>
https://docs.poloniex.com/#returnorderbook<br>

---

__Keywords__: order book, asks, bids, price, token, currency, pair, sample, fetch, retrieve

### Input ports

* __query__: ` {"currencyPair": string, optional "depth": number} `

### Output ports

* __data__: 
    ```
    {
      "asks": [string, number][],
      "bids": [string, number][],
      "isFrozen": string,
      "postOnly": string,
      "seq": number
    }
    ```


* __response__: 
    ```
    {"status": number, "headers": {string: any}, "body": string}
    ```


* __error__: ` {"error": string} `

