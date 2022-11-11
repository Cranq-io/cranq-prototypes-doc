# Joiner

_[binary/Joiner]_

![icon](</assets/icons/7341443a-8a0a-4a83-b302-effdb497c0f3.png>)

---

Joins differently encoded chunks into a base64-encoded string.<br>
<br>
Supports UTF-8 and Base 64 for input chunks.<br>
<br>
See `binary/Chunk builder` for generating input for `chunks`.<br>

---

__Keywords__: base64, utf8

### Input ports

* __chunks__: 
    ```
    {"encoding": ("utf8" or "base64"), "data": string}[]
    ```

    Receives the chunks to be joined.<br>

### Output ports

* __joined__: ` string `

    Sends the Base 64-encoded joined chunks.<br>

