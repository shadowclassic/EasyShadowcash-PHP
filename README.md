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
    $shadowcash = new Shadowcash();
    ```

    Optionally, you can specify a host and port. Defaults are 127.0.0.1 and port 51736.

    ```php
    $shadowcash = new Shadowcash('12.34.56.78','9999');
    ```

3. Make calls to shadowcoind as methods for your object. Examples:

    ```php
    $shadowcash->is_ready();
    
    $shadowcash->getblockcount();
    
    $shadowcash->get_block_header_by_height(1);
    ```
