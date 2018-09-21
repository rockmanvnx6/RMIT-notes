# Q6

##**Alice:**

- Make a file

```bash 
touch afile.txt
```
## Bob:
- Generate private key

```bash
openssl genrsa -out key.pem 1024
```

- Generate public key

```bash
openssl rsa -in key.pem -out pub-key.pem -pubout
```

## Alice:
**Encrypt with AES symmetric key**

```bash
openssl aes-256-cbc -a -salt -in afile.txt -out cipher.txt
```

Set the secret-key is `123`



<u>Sign using Bob's public key</u>

```bash
openssl rsautl -in cipher.txt -out cipher-signed.txt -pubin -inkey pub-key.pem -encrypt
```

- init ipfs system

- ```bash
  ipfs init
  ```

- Start daemon

- ```bash
  ipfs daemon
  ```

- open another prompt

- ```bash
  ipfs add cipher-signed.txt
  ```

- Receive unique hash: `QmaeTGkcco6yJzJ2ssVDUG6Y9HZe21b45L6ajtdP3YatNR`

  Send **Bob**
  - QmaeTGkcco6yJzJ2ssVDUG6Y9HZe21b45L6ajtdP3YatNR
  - Secret-key: 123

## Bob:

- First bob checks if the file in ipfs database

  ```bash
  ipfs pin ls
  ```

- Then he can 

- ```bash
  ipfs get QmaeTGkcco6yJzJ2ssVDUG6Y9HZe21b45L6ajtdP3YatNR
  ```

- He decrypt using his private key:

  ```bash
  openssl rsautl -in QmaeTGkcco6yJzJ2ssVDUG6Y9HZe21b45L6ajtdP3YatNR -out to-decipher.txt -inkey key.pem -decrypt
  ```

- He decrypt the cipher message

  - **Decrypt**

    ```bash
    openssl aes-256-cbc -d -a -in to-decipher.txt -out result.txt
    ```

    Put in secret-key: `123`