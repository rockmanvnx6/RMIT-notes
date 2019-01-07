

# Public key cryptography - Elgamal and Paillier and Practical PKC



# Elgamal

![image-20180806125807923](image-20180806125807923.png)

So server side:

- Choose a random number, call it `r`

- Calculate `k` $k = y^rmod (p)$

- Calculate 2 Cipher text, `C1` and `C2`

- $C1 = g^r mod(p)$

- $C2 = m * k mod p$

  `m = message`

Client side:

- if there is no `y`, $y = g^xmod(p)$

- Calculate $k = C1^x mod(p)$
- Calculate mod_inverse(k) = $k^{-1} = k * mod (p)$
- Decrypt: $m = k^{-1} * C_2mod(p)$



### So how do we generate y,g,p,x

![image-20180806130222590](image-20180806130222590.png)

![image-20180806130254947](image-20180806130254947.png)

![image-20180806130307630](image-20180806130307630.png)

# Exponential Elgamal Cryptosystem

![image-20180806131820471](image-20180806131820471.png)

![image-20180806131833202](image-20180806131833202.png)



## Limitations of Elgamal

- It becomes double size of the plain text.



# Paillier 

![image-20180806132042525](image-20180806132042525.png)

<u>Encryption</u>

$c = g^mr^nmod(n^2)$

<u>Decryption</u>

![image-20180806132314464](image-20180806132314464.png)

![image-20180806132425094](image-20180806132425094.png)

p & q has to satisfy the condition. $gcd(pq,(p-1)(q-1)) == 1$

![image-20180806132645385](image-20180806132645385.png)

![image-20180806132600534](image-20180806132600534.png)

![image-20180806133016919](image-20180806133016919.png)

# Open ssl

**Generate private public key:**

```console
openssl genrsa -out key.pem 1024
```

// 1024 bit.

![image-20180806134408843](image-20180806134408843.png)

in hex format.

**Generate public key**

```
openssl rsa -in key.pem -out pub-key.pem -pubout
```



**Encrypt**

```
openssl rsautl -in plain-text.txt -out cipher.txt -pubin -inkey pub-key.pem -encrypt
```

**Decrypt**

```
openssl rsautl -in cipher.txt -out result.txt -inkey key.pem -decrypt
```

