# Time-based moving buffer

_[streaming/Time-based moving buffer]_

---

Stores the "value" property of samples received in the last `length` seconds and sends them via `buffer`.<br>
<br>
Errors on invalid `size`.<br>
<br>
Expects samples to be received in ascending order of "timestamp".<br>
<br>
Data sent via `buffer` is immutable.<br>
<br>
Example:<br>
1. `size` set to 2 (seconds)<br>
2. {value: "A", timestamp: 0}@0 received via `sample`<br>
3. [{value: "A", timestamp: 0}]@0 sent via `buffer`<br>
4. {value: "B", timestamp: 1}@1 received via `sample`<br>
5. [{value: "A", timestamp: 0}, {value: "B", timestamp: 1}]@1 sent via `buffer`<br>
6. {value: "C", timestamp: 3}@2 received via `sample`<br>
7. [{value: "B", timestamp: 1}, {value: "C", timestamp: 3}]@1 sent via `buffer`<br>

---

__Keywords__: buffer, overflow, stream, rotate, window, seconds

### Input ports

* __sample__: ` {"value" :any, "timestamp" :number} `


    Receives individual samples to be buffered.<br>


* __size__: ` number `


    Size of the buffer in seconds.<br>

### Output ports

* __buffer__: ` {"value" :any, "timestamp" :number}["value"][] `


    Sends current contents of moving buffer.<br>


* __error__: ` {"message" :string} `


    Sends error when:<br>
    * size is equal or less than 0 or not set<br>


* __bounced__: ` {"value" :any, "timestamp" :number} `


    Forwards input received via `sample` on error.<br>

