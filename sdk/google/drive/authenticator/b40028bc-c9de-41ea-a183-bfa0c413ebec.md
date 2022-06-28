# Authenticator

_[sdk/google/drive/Authenticator]_

---

Authenticates the service user to use google drive.<br>
<br>
Example:<br>
1. `session Id` receives "drive_session"@0 <br>
2. `email` receives  "email@email.com"@0<br>
3. `key` receives "TopSecretKey"@0<br>
4. `done` sends null@0 <br>

---

__Keywords__: google, drive, authentication, sdk, file

### Input ports

* __session Id__: ` string `

    Receives the session id of the drive action.<br>
    <br>
    Example: <br>
    "drive_session"<br>


* __email__: ` string `

    Receives the email address of the service account.<br>
    <br>
    Example: <br>
    "email@email.com"<br>


* __key__: ` string `

    Receives the private key of the service account.<br>
    <br>
    Example: <br>
    "TopSecretKey!"<br>

### Output ports

* __done__: ` null `

    Sends null if the action was successful.<br>
    <br>
    Example:<br>
    null<br>


* __error__: ` {"error" :string} `

    Sends the error which happened during the execution of the action.<br>
    <br>
    Example:.<br>
    {error: "Something went wrong!"}<br>

