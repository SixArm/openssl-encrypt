# openssl-encrypt:<br>encrypt a file using our best settings

Syntax:

    openssl-encrypt <file>

Example:

    $ openssl-encrypt example.txt

Output is a new encrypted file:

    example.txt.aes

To decrypt the file:

    $ openssl-decrypt example.txt.aes


## Related

These commands are related:

  * `gpg-encrypt`: use GPG to encrypt a file using our best settings.
  
  * `gpg-decrypt`: use GPG to decrypt a file using our best settings.

  * `openssl-encrypt`: use OpenSLL to encrypt a file using our best settings.
  
  * `openssl-decrypt`: use OpenSSL to decrypt a file using our best settings.


## Settings

  * Symmetric encryption, i.e. we use the same password for encryption and decryption.
    We choose this because our users can understand symmetric more easily than asymmetic.

  * Encryption using the aes-256-cbc cipher algorithm.
    We choose this because it's a good balance of strong, fast, and portable.

  * Salt


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
