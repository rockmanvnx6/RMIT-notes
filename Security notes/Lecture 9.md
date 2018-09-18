# Digital Authentication & Security Prototcols

Two access controls, you need:

- **Authentication**:
  - Are you who you say you are?

- **Authorization**
  - Are you allowed to do that?

## Protocols

- Networking protocoles - rules followed in netowrked communication systems
  - Examples: HTTP, FTP, etc

- Security protocol - the (communication) rules followed in a security application
  - Examples: SSL, IPSec, Kerberos, etc.

>  Protocols still have flaws.



## Authentication

Simply passwords, fingerprints, etc.

### Challenge-Response

Challenge so that fake is not possible.

And only Alice can provide the correct response.

- **Nonce** (**n**umber used **once**)

![image-20180917130726089](image-20180917130726089.png)

### Generic Challenge-Response

![image-20180917131131085](image-20180917131131085.png)

### Symmetric key notation

Encrypt plaintext **P** with key **K**

$C = E(P,K)$

Decrypt cipher text **C** with **K**

$P = D(C,K)$

Alice and Bob share symmetric key K.

K known only to Alice and Bob

## Authentication with symmetric key notation

![image-20180917131418955](image-20180917131418955.png)

R is nonce, challenge.

# Mutual authentication

![image-20180917131826442](image-20180917131826442.png)

![image-20180917131900714](image-20180917131900714.png)

![image-20180917131941225](image-20180917131941225.png)

RA and RB are nonces