# Deploy script creator

_[blockchain/ethereum/actions/Deploy script creator]_

---

Creates the deploy script to deploy the contract using Hardhat.<br>

---

### Input ports

* __params__: 
    ```
    {
        "cwd": string,
        "path": string,
        "contract-name": string,
        "result-path": string,
        "message": string
    }
    ```

    {<br>
      "cwd": string, // the working directory<br>
      "path": string, // the path to write the deploy script to<br>
      "contract-name": string, // the name of the contract to deploy<br>
      "result-path": string, // the path in the state to write the result to<br>
      "message": string // the message to print on the console<br>
    }<br>


* __state__: ` any `

    Receives script state.<br>

### Output ports

* __state__: ` any `

    Sends updated script state.<br>

