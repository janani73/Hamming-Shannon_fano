# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.4,0.19,0.16,0.15,0.15} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
personal computer with colab
# Program:

# HUFFMAN:
```
import math
p = [0.4,0.19,0.16,0.15,0.15]
lk = [1,3,3,3,3]
n = len(p)
L = sum(p[k] * lk[k]
for k in range(n))
hs = sum(p[k] * math.log(1 / p[k], 2)
 for k in range(n))
hs = round(hs, 3)
eff = round(hs / L, 3)
red = round(1 - eff, 3)
var = sum(p[k] * (lk[k] - L) ** 2
for k in range(n))
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```

# SHANNON - FANO:
```
import math
p = [0.4,0.19,0.16,0.15,0.15]
lk = [2,2,3,3,2]
n = len(p)
L = sum(p[k] * lk[k]
for k in range(n))
hs = sum(p[k] * math.log(1 / p[k], 2)
 for k in range(n))
hs = round(hs, 3)
eff = round(hs / L, 3)
red = round(1 - eff, 3)
var = sum(p[k] * (lk[k] - L) ** 2
for k in range(n))
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
# Output:

# HUFFMAN:
``` 
Average Codeword Length is : 2.35
Entropy is : 2.228
Efficiency is : 94.8%
Redundancy is : 0.052
Variance is : 1.004
```
# SHANNON - FANO:
```
Average Codeword Length is : 2.41
Entropy is : 2.228
Efficiency is : 92.4%
Redundancy is : 0.076
Variance is : 0.232

```
# Result:
```
The values are calculated successfully.
