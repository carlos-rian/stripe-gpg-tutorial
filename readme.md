# Encrypt file using GPG - Linux WSL Ubuntu

## Step 1
1.	Create Folder
    ```sh
    mkdir help
    ```

2.	Check gpg version.

    **command**
    ```sh
    gpg --version
    ```
    **output**
    ```
    gpg (GnuPG) 2.2.19
    libgcrypt 1.8.5
    Copyright (C) 2019 Free Software Foundation, Inc.
    License GPLv3+: GNU GPL version 3 or later <https://gnu.org/licenses/gpl.html>
    This is free software: you are free to change and redistribute it.
    There is NO WARRANTY, to the extent permitted by law.

    Home: /home/carlos-rian/.gnupg
    Supported algorithms:
    Pubkey: RSA, ELG, DSA, ECDH, ECDSA, EDDSA
    Cipher: IDEA, 3DES, CAST5, BLOWFISH, AES, AES192, AES256, TWOFISH,
            CAMELLIA128, CAMELLIA192, CAMELLIA256
    Hash: SHA1, RIPEMD160, SHA256, SHA384, SHA512, SHA224
    Compression: Uncompressed, ZIP, ZLIB, BZIP2
    ```



3.	Enter the Folder.
    ```sh
    cd help
    ```

## Step 2
1. Create file **key.pub** with values of the **PGP PUBLIC KEY Sidecar**.
    ```sh
    echo "-----BEGIN PGP PUBLIC KEY BLOCK-----

    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
    =3PPa
    -----END PGP PUBLIC KEY BLOCK-----" > key.pub
    ```

2. Check if it was created.

    **command**
    ```sh
    ls -l
    ```
    **output**
    ```
    total 7
    -rwxrwxrwx 1 carlos-rian carlos-rian 6648 Jul  7 12:42 key.pub
    ```

3. Import public key to **gpg**.

    **command**
    ```sh
    gpg --import key.pub
    ```
    **output**
    ```
    gpg: key 9C78B7620C1E99AD: public key "Stripe Import Key (PCI) <support-migrations@stripe.com>" imported
    gpg: Total number processed: 1
    gpg:               imported: 1
    ```

4. Check **gpg** keys, list all public keys.

    **command**
    ```sh
    gpg -k
    ```
    **output**
    ```
    /home/carlos-rian/.gnupg/pubring.kbx
    ------------------------------------
    pub   rsa4096 2019-07-03 [SC] [expires: 2023-06-22]
        AEBF7C4838C44D2FDC99A3F99C78B7620C1E99AD
    uid           [ unknown] Stripe Import Key (PCI) <support-migrations@stripe.com>
    sub   rsa4096 2022-03-29 [E] [expires: 2023-06-22]
    sub   rsa4096 2022-03-29 [S] [expires: 2023-06-22]
    ```

## Step 3
1. **Add the file you need to encrypt** in the folder you created.


2. List files.

    **command**
    ```sh
    ls -l
    ```
    **output**
    ```sh
    total 8
    -rwxrwxrwx 1 carlos-rian carlos-rian 6250 Jul  7 12:52 key.pub
    -rwxrwxrwx 1 carlos-rian carlos-rian    3 Jul  7 13:15 sidecar.txt
    ```

3. Create encrypt file, confirm using **y** and enter. Arg **--armor** transforms the encrypted output to text instead of binary. 

    **command**
    ```sh
    gpg --encrypt --armor --recipient 9C78B7620C1E99AD sidecar.txt
    ```

    **output**
    ```
    gpg: 35AE1E63A401015C: There is no assurance this key belongs to the named user

    sub  rsa4096/35AE1E63A401015C 2022-03-29 Stripe Import Key (PCI) <support-migrations@stripe.com>
    Primary key fingerprint: AEBF 7C48 38C4 4D2F DC99  A3F9 9C78 B762 0C1E 99AD
        Subkey fingerprint: B354 01FA B05F 51DB E5AB  A14C 35AE 1E63 A401 015C

    It is NOT certain that the key belongs to the person named
    in the user ID.  If you *really* know what you are doing,
    you may answer the next question with yes.

    Use this key anyway? (y/N) y
    ```

4. List files, **note** that a new file with .asc (without --armor is .gpg) extension was created. This file can be sent to the owner of the Private Key and he will be able to decrypt the message.

    **command**
    ```sh
    ls -l
    ```
    **output**
    ```sh
    total 12
    -rwxrwxrwx 1 carlos-rian carlos-rian 6250 Jul  7 12:52 key.pub
    -rwxrwxrwx 1 carlos-rian carlos-rian    3 Jul  7 13:15 sidecar.txt
    -rwxrwxrwx 1 carlos-rian carlos-rian  878 Jul  7 13:20 sidecar.txt.asc
    ```