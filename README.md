# authrw
* [authrw](https://github.com/Ajay-Aj-00/Test/tree/master/authrw) is a **Crypto Challenge** given in InCTF-2018 Finals Attack and Defence
* It uses the `AES 128-bit CBC mode Encrytion`.`IV(16 bytes)` is given in iv.txt but we have to **generate the key** using [generate_key.py](https://github.com/Ajay-Aj-00/Test/tree/master/authrw/generate_key.py) which takes the Team password as input.The generated Key is `md5 hash of Team password`.
* **It Runs a Crypto Service in which it has `Login` and `Register` services**
![Login,Register](https://raw.githubusercontent.com/Ajay-Aj-00/Test/master/Images/1.png "Service")
### 2 - Register
* For the Register it will Asks the user for **username** (username != 'admin')
* Then It Encrypts the `pad("username=input():role=ordinary")` with AES CBC 128-bit Encryption
* After that It returns a cookie which is `"IV+Cipher_text".encode('hex')`
* [Register](https://raw.githubusercontent.com/Ajay-Aj-00/Test/master/Images/3.png "Register")
