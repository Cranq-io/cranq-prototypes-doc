# Tag incrementer

_[flow/Tag incrementer]_

---

Increments the iterable (colon-separated) part of the received signal's tag.<br>
<br>
Bounces when tag is not iterable.<br>
<br>
Used for lining up signals with iterations. (See eg. `data/array/Iterator`.)<br>
<br>
Example A (success):<br>
1. "A"@"x:1" received via `data`<br>
2. "A"@"x:2" is sent via `data` (output)<br>
<br>
Example B (invalid input):<br>
1. "A"@"x" received via `data`<br>
2. "A"@"x" is sent via `bounced`<br>
<br>
See also:<br>
* `flow/Tag nester`<br>
* `flow/Tag trimer`<br>

---

__Keywords__: simulated iteration, fake iteration, synchronization, syncing

### Input ports

* __data__: ` any `


    Receives signal with iterable tag.<br>
    <br>
    When the tag is not iterable, the signal will be bounced.<br>

### Output ports

* __data__: ` any `


    Sends signal with data identical to the one received via `data`, but with incremented tag.<br>


* __bounced__: ` any `


    Forwards the signal received through `data` when its tag was not iterable.<br>

