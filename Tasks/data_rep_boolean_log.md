# Task 1
## Boolean Logic
Draw the circuit for the boolean equations provided.

### AB + not(A + B)
![image](https://user-images.githubusercontent.com/111758436/198275640-107a3877-480c-4137-92be-1ee1d755ae17.png)
### not(A(A + B)) + B
![image](https://user-images.githubusercontent.com/111758436/198277158-4d078160-86da-40b2-a4b3-eaab7371e96a.png)
### ((not A) and B) or (A and B)
![image](https://user-images.githubusercontent.com/111758436/198278594-315a01ce-c353-40c9-a5ef-52dd132c00b7.png)
### not(ACB) + not((A + C)B)
![image](https://user-images.githubusercontent.com/111758436/198280295-a50d299f-441b-402d-a594-41bcd9a720e3.png)
### [HL] not(b1b2b3) + not((b1 + b3))(b1 + b2)
![image](https://user-images.githubusercontent.com/111758436/198281801-2ab38b14-8b01-427b-b1da-a07183c77907.png)
## Get the equation
Write the boolean equation for the circuit shown.

### Circuit 1
![image](https://user-images.githubusercontent.com/111758436/198283683-36664d2e-c75c-44c7-8014-481d09c5910f.png)

### Circuit 2
![image](https://user-images.githubusercontent.com/111758436/198285303-f6ca1b85-f50c-4628-a99a-39943a45ff58.png)

### Circuit 3
![image](https://user-images.githubusercontent.com/111758436/198324472-51f00cf3-270f-437c-813b-7dba1197c1e2.png)

## Truth table
Write the truth table for the equations below.

### X = A and B
| **a** | **b** | **x** |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

### Out = input1 or input2
| **input1** | **input2** | **Out** |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

### Light = not(S1) + not(S2 + S3) + S1S2not(S3)
| **S1** | **S2** | **S3** | **not S1** | **S2 or S3** | **not (S2 or S3)** | **not S3** | **S1 and S2** | **not S3 and (S1 and S2)** | **not S1 or not (S2 or S3)** | **(not S1 or not (S2 or S3)) or (not S3 and (S1 and S2))** |
|----|----|----|--------|----------|----------------|--------|-----------|------------------------|--------------------------|--------------------------------------------------------|
| 0  | 0  | 0  | 1      | 0        | 1              | 1      | 0         | 0                      | 1                        | 1                                                      |
| 0  | 0  | 1  | 1      | 1        | 0              | 0      | 0         | 0                      | 1                        | 1                                                      |
| 0  | 1  | 0  | 1      | 1        | 0              | 1      | 0         | 0                      | 1                        | 1                                                      |
| 0  | 1  | 1  | 1      | 1        | 0              | 0      | 0         | 0                      | 1                        | 1                                                      |
| 1  | 0  | 0  | 0      | 0        | 1              | 1      | 0         | 0                      | 1                        | 1                                                      |
| 1  | 0  | 1  | 0      | 1        | 0              | 0      | 0         | 0                      | 0                        | 0                                                      |
| 1  | 1  | 0  | 0      | 1        | 0              | 1      | 1         | 1                      | 0                        | 1                                                      |
| 1  | 1  | 1  | 0      | 1        | 0              | 0      | 1         | 0                      | 0                        | 0                                                      |

### [HL] Login = not(P1P2P3) + not((P3not(P2P1))) + not(P1 + P3)
| P1 | P2 | P3 | P1 and P2 | (P1 and P2) and P3 | not ((P1 and P2) and P3) | not (P1 and P2) | not (P1 and P2) and P3 | not(not (P1 and P2) and P3) | P1 or P3 | not (P1 or P3) | not ((P1 and P2) and P3) or not(not (P1 and P2) and P3) | (not ((P1 and P2) and P3) or not(not (P1 and P2) and P3)) or not (P1 or P3)) |
|----|----|----|-----------|--------------------|--------------------------|-----------------|------------------------|-----------------------------|----------|----------------|---------------------------------------------------------|------------------------------------------------------------------------------|
| 0  | 0  | 0  | 0         | 0                  | 1                        | 1               | 0                      | 1                           | 0        | 1              | 1                                                       | 1                                                                            |
| 0  | 0  | 1  | 0         | 0                  | 1                        | 1               | 0                      | 1                           | 1        | 0              | 1                                                       | 1                                                                            |
| 0  | 1  | 0  | 0         | 0                  | 1                        | 1               | 0                      | 1                           | 0        | 1              | 1                                                       | 1                                                                            |
| 0  | 1  | 1  | 0         | 0                  | 1                        | 1               | 0                      | 1                           | 1        | 0              | 1                                                       | 1                                                                            |
| 1  | 0  | 0  | 0         | 0                  | 1                        | 1               | 0                      | 1                           | 1        | 0              | 1                                                       | 1                                                                            |
| 1  | 0  | 1  | 0         | 0                  | 1                        | 1               | 0                      | 1                           | 1        | 0              | 1                                                       | 1                                                                            |
| 1  | 1  | 0  | 1         | 0                  | 1                        | 0               | 0                      | 1                           | 1        | 0              | 1                                                       | 1                                                                            |
| 1  | 1  | 1  | 1         | 1                  | 0                        | 0               | 0                      | 1                           | 1        | 0              | 1                                                       | 1                                                                            |

## Data conversation
Information can be represented in different systems, for example the number 10  in decimal (system base 10) can be represented in binary (system base 2) as 1010 or 12 in base 8. 

It is critical for you to understand how to represent information in different ways, this will help you visualize how the computer processes data.

### 256 (Decimal)
**Base 2 (Binary):** 100000000

**Base 4:** 10000

**Base 6:** 1104

### 433 (Base 5)
**Base 10 (Decimal):** 118

**Base 8 (Octal):** 166

**Base 16 (Hexadecimal):** 76

### FA32 (Base 16)
**Base 10 (Decimal):** 64050

**Base 8 (Octal):** 175062

**Base 2 (Binary):** 1111101000110010
