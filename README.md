# openssl-encrypt:<br>encrypt a file using our best settings

Syntax:

    openssl-encrypt <file>

Example:

    $ openssl-encrypt example.txt

Output is a new encrypted file:

    example.txt.aes

To decrypt the file:

    $ openssl-decrypt example.txt.aes


## Settings

  * Symmetric encryption, i.e. we use the same password for encryption and decryption.
    We choose this because our users can understand symmetric more easily than asymmetic.

  * Encryption using the aes-256-cbc cipher algorithm.
    We choose this because it's a good balance of strong, fast, and portable.

  * Salt


## See also

These commands are similar:

  * [`gpg-encrypt`](https://github.com/SixArm/gpg-encrypt): 
    use GPG to encrypt a file using our best settings.
  
  * [`gpg-decrypt`](https://github.com/SixArm/gpg-decrypt): 
    use GPG to decrypt a file using our best settings.

  * [`openssl-encrypt`](https://github.com/SixArm/openssl-encrypt): 
    use OpenSLL to encrypt a file using our best settings.
  
  * [`openssl-decrypt`](https://github.com/SixArm/openssl-decrypt): 
    use OpenSSL to decrypt a file using our best settings.


## Command

The command is:

    openssl \
    aes-256-cbc \
    -salt 
    -in "$1" \
    -out "$1.aes"


## Tracking

  * Command: openssl-encrypt
  * Version: 1.0.0
  * Created: 2017-09-14
  * Updated: 2017-09-14
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
