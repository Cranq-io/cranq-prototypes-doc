# JSON listener

_[io/http/express/JSON listener]_

---

Starts an express server set up for handling requests and also responding with JSON bodies.<br>

---

__Keywords__: express, server, start, json

### Input ports

* __app ID__: ` string `

    The id of the express instance.<br>
    <br>
    Example: <br>
    "my-express-server"<br>


* __port__: ` number `

    The port number express should listen to.<br>
    <br>
    Example: <br>
    3000<br>

### Output ports

* __done__: ` any `


* __error__: ` {"error" :string} `

    Sends error information in case the server could not be started or a middleware could not be applied.<br>

