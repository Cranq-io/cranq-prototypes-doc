# Burst tester

_[flow/utils/Burst tester]_

---

Sends true on the last signal in bursts of `length` length.<br>
<br>
Example:<br>
1. `length` set to 3<br>
2. "A"@0 received via `data`<br>
3. false@0 sent via `is last`<br>
4. "B"@1 received via `data`<br>
5. false@1 sent via `is last`<br>
6. "C"@2 received via `data`<br>
7. true@2 sent via `is last` <br>

---

__Keywords__: series, modulo, detect, test

### Input ports

* __data__: ` any `

    Receives the burst signals.<br>


* __length__: ` number `

    Burst length to be detected.<br>
    <br>
    Can be parameter.<br>

### Output ports

* __is last__: ` boolean `

    Sends true on the last signal in the burst, false otherwise.<br>

