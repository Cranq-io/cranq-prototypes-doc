# Command runner

_[system/Command runner]_

---

Runs the received command string with the received options.<br>
<br>
Sends stdout, stderr and optionally error message when the process finished.<br>
<br>
Bounces command and options when the node is already in the state of executing a command.<br>

---

### Input ports

* __command__: ` string `


* __options__: ` {"cwd" :string, "env" :{string: string}} `

### Output ports

* __stdout__: ` string `


* __stderr__: ` string `


* __error__: ` (string or null) `


    Null on success.<br>


* __on busy__: 
    ```
    {"command" :string, "options" :{"cwd" :string, "env" :{string: string}}}
    ```


    The received command and options when the node is still executing another command.<br>


* __bounced__: ` any `

