# Multi params builder

_[io/http/utils/Multi params builder]_

---

Builds an array of single query parameters as key-value pairs based on the key received via `key` and the values received via `values`.<br>
<br>
Example:<br>
1. ["Norah", "Smith"]@1 received via `values`<br>
2. "name"@1 received via `key`<br>
3. [{"key": "name", "value": "Norah"}, {"key": "name", "value": "Smith"}]@1 sent via `params`<br>

---

__Keywords__: construct, create, key-value pairs

### Input ports

* __values__: ` string[] `

    Receives an array of query parameter values associated with the same key.<br>


* __key__: ` string `

    Receives the key part of a key-value pair.<br>

### Output ports

* __params__: ` {"key" :string, "value" :string}[] `

    Sends an array of single query params as key-value pairs.<br>

