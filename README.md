EasyShadowcash-PHP
===============

A simple class for making calls to Shadowcash/Shadowcoin's daemon JSON-RPC API using PHP.

Getting Started
---------------
1. Include easyshadowcash.php into your PHP script:

    ```php
    require_once('easyshadowcash.php');
    ```
2. Initialize shadowcashd connection/object:

    ```php
    $shadowcash = new Shadowcash('rpcuser','rpcpassword');
    ```

    Optionally, you can specify a host and port. Defaults are 127.0.0.1 and port 51736.

    ```php
    $shadowcash = new Shadowcash('rpcuser','rpcpassword','12.34.56.78','9999');
    ```

3. Make calls to shadowcoind as methods for your object. Examples:

    ```php
    $shadowcash->getinfo();
    
    $shadowcash->getblockcount();
    
    $shadowcash->getrawtransaction('9e79d2201393286e1ada3f0fbbe24b996a6cbcdabaa91b6701a8501e36fbf1e4',1);

    $shadowcash->getblock('0000002372e70c3e4113a41364acd0ad1b7e51b9a9d3014f7b1e1e11a4cc0256');
    ```
