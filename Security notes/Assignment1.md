# Assignment 1

Student ID: s3619352

Student name: Thang Pham

### Q1. a)

>  Given: 
>
> **SOGIUNBCNUODLMIXOTSINCRHINPEHNWRTOAROSATNPHAIITSSOB OFEDUOOTSPIIELMXNAPESATLRN**
>
> Known: The first word is 'THIS'

- First, we need to generate a matrix of 11 rows and 7 columns

|        | 1    | 2    | 3    | 4    | 5    | 6    | 7    |
| ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| **1**  | S    | O    | G    | I    | U    | N    | B    |
| **2**  | C    | N    | U    | O    | D    | L    | M    |
| **3**  | I    | X    | O    | T    | S    | I    | N    |
| **4**  | C    | R    | H    | I    | N    | P    | E    |
| **5**  | H    | N    | W    | R    | T    | O    | A    |
| **6**  | R    | O    | S    | A    | T    | N    | P    |
| **7**  | H    | A    | I    | I    | T    | S    | S    |
| **8**  | O    | B    | O    | F    | E    | D    | U    |
| **9**  | O    | O    | T    | S    | P    | I    | I    |
| **10** | E    | L    | M    | X    | N    | A    | P    |
| **11** | E    | S    | A    | T    | L    | R    | N    |

As know the first word is 'THIS'. So first 4 columns in row 1 will be ‘THIS'. Which means within a row, there must be characters T,H,I,S. Based on that conclusion we have the result:

|        | 5    | 1    | 4    | 6    | 3    | 7    | 2    |
| ------ | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| **7**  | T    | H    | I    | S    | I    | S    | A    |
| **10** | N    | E    | X    | A    | M    | P    | L    |
| **8**  | E    | O    | F    | D    | O    | U    | B    |
| **11** | L    | E    | T    | R    | A    | N    | S    |
| **9**  | P    | O    | S    | I    | T    | I    | O    |
| **4**  | N    | C    | I    | P    | H    | E    | R    |
| **1**  | U    | S    | I    | N    | G    | B    | O    |
| **5**  | T    | H    | R    | O    | W    | A    | N    |
| **2**  | D    | C    | O    | L    | U    | M    | N    |
| **6**  | T    | R    | A    | N    | S    | P    | O    |
| **3**  | S    | I    | T    | I    | O    | N    | X    |

>  **<u>Message:</u>**
>  
THIS IS AN EXAMPLE OF DOUBLE TRANSPOSITION CIPHER USING BOTH ROW AND COLUMN TRANSPOSITION.

###b)

> Original: **UMYTMHUZSRGZ**
>
> **BruteForce**

 UMYTMHUZSRGZ --- n: 0 <br />
 TLXSLGTYRQFY --- n: 1 <br />
 SKWRKFSXQPEX --- n: 2 <br />
 RJVQJERWPODW --- n: 3 <br />
 QIUPIDQVONCV --- n: 4 <br />
 PHTOHCPUNMBU --- n: 5 <br />
 OGSNGBOTMLAT --- n: 6 <br />
 NFRMFANSLKZS --- n: 7 <br />
 MEQLEZMRKJYR --- n: 8 <br />
 LDPKDYLQJIXQ --- n: 9 <br />
 KCOJCXKPIHWP --- n: 10 <br />
 JBNIBWJOHGVO --- n: 11 <br />
 IAMHAVINGFUN --- n: 12 <br />

> <u>**Message**</u> 
>
> IAMHAVINGFUN --- n: 12

Shift n = 12.

**Python code written: https://pastebin.com/mB5GD1fz**

## c)

- First, we generate the frequency of all the character in the text:

  ```python
  ('L', 1)
  ("'", 1)
  ('A', 2)
  ('P', 2)
  ('"', 4)
  ('M', 6)
  ('E', 6)
  ('.', 6)
  ('F', 7)
  ('I', 7)
  ('Z', 8)
  (',', 11)
  ('R', 11)
  ('V', 14)
  ('S', 15)
  ('K', 17)
  ('O', 18)
  ('T', 20)
  ('C', 21)
  ('Q', 25)
  ('B', 30)
  ('H', 31)
  ('W', 31)
  ('G', 34)
  ('D', 36)
  ('N', 39)
  ('U', 54)
  ('X', 60)
  ('J', 80)
  (' ', 129)
  ```

- Next, based on the frequency table, we can substitute by following:

  ```python
  'J': 'e', // based on the frequency 
  'X': 't', // based on the frequency. 
  'U': 'a', 
  'D': 'h',
  'T': 'c',
  'O': 'f',
  'I': 'v',
  'K': 'y',
  'G': 'o',
  'C': 'u',
  'B': 'r',
  'N': 'n',
  'Q': 'l',
  'R': 'w',
  'H': 'i',
  'W': 's',
  'M': 'm',
  'E': 'q',
  'Z': 'p',
  'F': 'b',
  'V': 'g',
  'S': 'd',
  'P': 'k',
  'A': 'x',
  'L': 'z'	
  ```

> **Message**: 
> 
the methodology behind frequency analysis relies on the fact that in any language, each letter has its own personality. the most obvious trait that letters have is the frequency with which they appear in a language. clearly in english the letter 'z' appears far less frequently than, say, 'a'. in times gone by, if you wanted to find out the frequencies of letters within a language, you had to find a large piece of text and count each frequency. now, however, we have computers that can do the hard work for us. but in fact, we don't even need to do this step, as for most languages there are databases of the letter frequencies, which have been calculated by looking at millions of texts, and are thus very highly accurate.

**Python code written:**

- Count letter frequency: https://pastebin.com/diNTCwAw
- Replace word: https://pastebin.com/7ggLLWZv

### Q2

**i.**

- Step1. Trudy knows the range value is from \$95 to \$103
- Step2. He generate a brute force `rainbow table` which contains all of the possible **SHA-256** hashing value from **95 - 103**

Result:

```python
95 ad48ff99415b2f007dc35b7eb553fd1eb35ebfa2f2f308acd9488eeb86f71fa8
96 7b1a278f5abe8e9da907fc9c29dfd432d60dc76e17b0fabab659d2a508bc65c4
97 d6d824abba4afde81129c71dea75b8100e96338da5f416d2f69088f1960cb091
98 29db0c6782dbd5000559ef4d9e953e300e2b479eed26d887ef3f92b921c06a67
99 8c1f1046219ddd216a023f792356ddf127fce372a72ec9b4cdac989ee5b0b455
100 ad57366865126e55649ecb23ae1d48887544976efea46a48eb5d85a6eeb4d306
101 16dc368a89b428b2485484313ba67a3912ca03f2b2b42429174a4f8b3dc84e44
102 37834f2f25762f23e1f74a531cbe445db73d6765ebe60878a7dfbecd7d4af6e1
103 454f63ac30c8322997ef025edff6abd23e0dbe7b8a3d5126a894e4a168c1b59b
```

- Step 3. Based on the `rainbow table` above, we will find the Hash value of Alice and Bob, which is 

`8C1F1046219DDD216A023F792356DDF127FCE372A72EC9B4CDAC989EE5B0B455` and `454F63AC30C8322997EF025EDFF6ABD23E0DBE7B8A3D5126A894E4A168C1B59B ` respectively.

Result:

```python
95 ad48ff99415b2f007dc35b7eb553fd1eb35ebfa2f2f308acd9488eeb86f71fa8
96 7b1a278f5abe8e9da907fc9c29dfd432d60dc76e17b0fabab659d2a508bc65c4
97 d6d824abba4afde81129c71dea75b8100e96338da5f416d2f69088f1960cb091
98 29db0c6782dbd5000559ef4d9e953e300e2b479eed26d887ef3f92b921c06a67
99 8c1f1046219ddd216a023f792356ddf127fce372a72ec9b4cdac989ee5b0b455 ------ ALICE
100 ad57366865126e55649ecb23ae1d48887544976efea46a48eb5d85a6eeb4d306
101 16dc368a89b428b2485484313ba67a3912ca03f2b2b42429174a4f8b3dc84e44
102 37834f2f25762f23e1f74a531cbe445db73d6765ebe60878a7dfbecd7d4af6e1
103 454f63ac30c8322997ef025edff6abd23e0dbe7b8a3d5126a894e4a168c1b59b ------ BOB
```

Step 4. He found out that **Alice bid 99** and **Bob bid 103**. He can then bid \$103.1 to win the auction

**ii.**

To prevent bruteforce attack. It's better to add a random character before or after the actual value:

For example. If Alice wants to bet 99, instead of hashing 99. She can add `SALT_` in the front. Thus, it will be:

`SALT_99` 

$sha256(`SALT\_99`) = 771fd4b3a65555993d18188500b0be4b908791758bfb69e6547f549f6865c2a2 $

As a result, it's impossible for Trudy to guess what string Alice added to the front and thus he can't bruteforce. 

**Python code written: https://pastebin.com/E24J4HhU**

### Q3

- **How would Alice encrypt message `M=7415`**
  - First, she will choose $n = p*q = 443 * 503 = 222829$
  - Next, she calculates $φ(n) = (p-1)*(q-1) = 442*502 = 221884$
  - Next, she pick a prime number $e$ such that $gcd(e,221884) = 1$
    - As a result, in this case, choosing $e = 3$ since it's the smallest.
  - Thus, the public key will be $(222829,3)$
  - Encrypted message $C = M^emodn = 7415^3mod(222829) = 134908$
  - Private key $d = mod inverse(e,φ(n)) = 147923$
- **How would Bob decrypt `C=134908` with `d=147923`**
  - $M = C^dmodn = 134908^{147923} mod(222829) = 7415 $

**Python code written: https://pastebin.com/fS9f14PT**

### Q4

- Trudy has the following information: `n = 3901`, `e=11`, `C=1602`
- First, she will prepare a list of prime number. And then find the first $p$ and $q$ so that $p*q = 3901$

  - She obtains: `p = 83`, `q = 47`
- Thus, she has: $φ(n) = (p-1)*(q-1) = 82*46 = 3772$
- Then she can calculate $d = modinverse(e,φ(n)) = modinverse(11,3772) = 343$
- Thus, the message is $M = C^dmodn = 1602^{343}mod(3901) = 3$

**Python code written: https://pastebin.com/fS9f14PT**



### Q5

- We have: `M = 59`, `p = 8467`, `g = 7919`, `x=91`, `r=51`

<u>Key generation</u>:

First, Bob will calculate the value of y

$y = g^xmod(p) = 7919^{91} mod (8467) = 3249$

<u>Sender encryption</u>

Sender Alice will receive `y` from Bob and calculate k:

$k = y^rmod(p) = 3249^{51}mod(8467) = 2145$

Then she will calculate 2 different Cipher text

$C_1 = g^rmod(p) = 7919^{51}mod(8467) = 6276$

$C_2 = M*kmod(p) = 59*2145mod(8467) = 8017$

<u>Receiver decryption</u>

Bob receive `C1` and `C2` from Alice. First, he finds k by:

$k = C_1^xmod(p) = 6276^{91}mod(8467) = 2145$

Next, he finds

$k^{-1} = modinverse(k,p) = 2145^{-1}mod(8467) = 4271$

Thus:

$M = k^{-1}*C_2mod(p) = 4271*8017mod(8467) = 59$

**Python code written: https://pastebin.com/fS9f14PT**

### Q6

- We have `M = 1234`, `p=61`,`q=97`,`g=119`,`r=67`

<u>Key generation:</u>

Bob will calculate $n=p*q = 61*97 = 5917$

So we have the public key $(n,g) = (5917,119)$

<u>Private key generation</u>

First, Bob calculates lambda $λ = lcm(p-1,q-1) = lcm(60,96) = 480$

Next, he calculates $k = L(g^λmodn^2) $ with $L(u) = \frac{u-1}{n}$

So $k = L(119^{480}mod(5917^2)) = 4142 $

Then he calculates $μ = k^{-1}mod(n) = 4142^{-1}mod(5917) = 10$

<u>Sender side encryption</u>

Alice selects `r=67`. She then calculates 

$c = g^mr^nmod(n^2) = 119^{1234}67^{5917}mod(5917^2) = 31145362 $

<u>Receiver decryption</u>

Bob receive the cypher message, he then decrypt using

$m = L(c^λmod(n^2))*μmod(n) = L(31145362^{480}mod(5917^2))*10mod(5917) = 1234$

**Python code written: https://pastebin.com/fS9f14PT**



