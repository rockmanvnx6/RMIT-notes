# Ciphertext

**Q1:** 

> Ciphertext : **ZLJBYPAF**



| Z    | L    | J    | B    | Y    | P    | A    | F    |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| b    | n    | l    |      |      |      |      |      |

> Ciphertext: **FDHVDU**

| F    | D    | H    | V    | D    | U    |
| ---- | ---- | ---- | ---- | ---- | ---- |
| G    | E    | I    | W    | E    | V    |
| H    | F    |      |      |      |      |
| I    | G    |      |      |      |      |
| J    | H    |      |      |      |      |
| K    | I    | M    |      |      |      |
|      |      |      |      |      |      |
|      |      |      |      |      |      |

shift 23 => CAESAR. From C to F, shift 3 chracters to the right. 

---

**Solution**

create something like

a) if the cipher text. start from Z, => Z = 0

| Z    | A    | B    | C    | D    | E    | F    | G    | H    | I    | J    | K    | L    | M    | N    | O    | P    | Q    | R    | S    | T    | U    | V    | W    | X    | Y    |      |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 0    | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   | 11   | 12   | 13   | 14   | 15   | 16   | 17   | 18   | 19   | 20   | 21   | 22   | 23   | 24   | 25   |      |



Shift 1

Z => A, L=> M, J => K..

=> result: AMKCZQBG

shift 2...



shift 19… => SECURITY (plaintext).

from S to Z will be 7 characters



**Q3:**

**String: SECURITY IN COMPUTING** — replace blank with X.

|      | 1    | 2    | 3    | 4    | 5     |
| ---- | ---- | ---- | ---- | ---- | ----- |
| 4    | T    | I    | N    | G    | **X** |
| 2    | I    | T    | Y    | I    | N     |
| 3    | C    | O    | M    | P    | U     |
| 1    | S    | E    | C    | U    | R     |

result: TINGXITYINCOMPUSECUR. — correct

|      | 5     | 3    | 1    | 4    | 2    |
| ---- | ----- | ---- | ---- | ---- | ---- |
| 4    | **X** | N    | T    | G    | I    |
| 2    | N     | Y    | I    | I    | T    |
| 3    | U     | M    | C    | P    | O    |
| 1    | R     | C    | S    | U    | E    |

result: XNTGINYIITUMCPORCSUE — correct



**String: WE ARE ALL TOGETHER**

row:

| 0    | 1    | 2    | 3    | 4    |
| ---- | ---- | ---- | ---- | ---- |
| 2    | E    | A    | L    | L    |
| 4    | T    | H    | E    | R    |
| 1    | W    | E    | A    | R    |
| 3    | T    | O    | G    | E    |

result: EALLTHERWEARTOGE — correct



column:
| 0    | 3    | 1    | 2    | 4    |
| ---- | ---- | ---- | ---- | ---- |
| 2    | L    | E    | A    | L    |
| 4    | E    | T    | H    | R    |
| 1    | A    | W    | E    | R    |
| 3    | G    | T    | O    | E    |

result: LEALETHRAWERGTOE — correct



