# Hamming-Shannon_fano
# Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
# Apply the Huffman and Shannon-Fano to this source.
## AADHITHYA SV (212223060001)
# Aim
To compute the Average Codeword Length, Entropy, Efficiency, Redundancy, and Variance for a discrete memoryless source 
using Huffman and Shannon-Fano coding based on the given probabilities and codeword lengths.

## Tools required
Python: A versatile programming language used for scientific computing and signal processing.
NumPy: A powerful numerical library in Python for performing array-based operations and mathematical computations.
Matplotlib: A plotting library for generating high-quality graphs and visualizations of data, essentialfor demonstrating the sampling process.
      
## Program
```
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)

for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1

for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)

eff = hs / L
eff = round(eff,3)

red =  round(1 - eff,3) 

var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print()
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff*100} %")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```

## Output   
![WhatsApp Image 2025-03-25 at 21 59 29_4d6be46c](https://github.com/user-attachments/assets/36151593-241e-4767-998b-23340d2fc72c)


# calculations:
![WhatsApp Image 2025-03-25 at 21 30 26_3df8e4d7](https://github.com/user-attachments/assets/28ee21e3-f73e-4447-a899-47cb515a1878)

![WhatsApp Image 2025-03-25 at 21 30 27_4add0e97](https://github.com/user-attachments/assets/cc43a7b1-6433-410a-b327-5f5a627c70bb)


## Result 
For the given probabilities 
0.125,0.0625,0.25,0.0625,0.125,0.125,0.25

