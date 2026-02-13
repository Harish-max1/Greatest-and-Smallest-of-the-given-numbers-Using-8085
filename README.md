# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
LDA 4200H;
MOV C,A;
LXI H,4201H;
MOV A,M;
INX H;
DCR C;
LOOP:CMP M;
JNC NEXT;
MOV A,M;
NEXT:INX H;
DCR C;
JNZ LOOP;
STA 4300H;
HLT;
```
## Output:
<img width="1902" height="916" alt="image" src="https://github.com/user-attachments/assets/abe41204-e155-418b-ab37-6477d6bec821" />
<img width="291" height="807" alt="image" src="https://github.com/user-attachments/assets/ff7c2527-cd92-45fd-8ce9-99b05f58aa7c" />


## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
LDA 4200H;
MOV C,A;
LXI H,4201H;
MOV A,M;
INX H;
DCR C;
LOOP:CMP M;
JC NEXT;
MOV A,M;
NEXT:INX H;
DCR C;
JNZ LOOP;
STA 4301H;
HLT;
```

## Output:
<img width="1920" height="966" alt="image" src="https://github.com/user-attachments/assets/e9a67611-20e3-4328-8127-1ddda4d64380" />
<img width="301" height="782" alt="image" src="https://github.com/user-attachments/assets/f6aff22b-cff1-4861-b8be-0ef924d4295f" />


## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
