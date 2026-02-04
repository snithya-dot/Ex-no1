# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) 
| ----------------------- | ------------------------ |
|       1200              |             58
|                         |
|       1201              |              13

#### Manual Calculations

<img width="1541" height="969" alt="image" src="https://github.com/user-attachments/assets/1f081c74-7550-4382-9e99-c687e5ed7dca" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="639" height="186" alt="image" src="https://github.com/user-attachments/assets/a68f56c7-5d71-498f-bec3-4975981efd6a" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
SUB AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200            |         10               |
|         1201            |         11               |
|         1202            |         00               |
|
#### Manual Calculations

<img width="1600" height="1075" alt="image" src="https://github.com/user-attachments/assets/bd2a1553-db61-4a49-86d3-abc42a182d05" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="635" height="148" alt="image" src="https://github.com/user-attachments/assets/c9773f8c-f928-4668-941f-681b0e993589" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1201:34          |          68:1205
|        1202:12          |          00:1206
|        1203:34          |          c4:1207

#### Manual Calculations
<img width="1005" height="557" alt="image" src="https://github.com/user-attachments/assets/6c95ac88-1598-4ad6-926d-f4f72f861914" />






---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="639" height="176" alt="image" src="https://github.com/user-attachments/assets/2442636e-f8b1-4f44-a08a-fc9992788452" />





## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1201:34          |          68:1205
|        1202:12          |          00:1206
|        1203:34          |          c4:1207

#### Manual Calculations
<img width="1009" height="523" alt="image" src="https://github.com/user-attachments/assets/e6a9d955-94b3-4a8b-9646-bfa090567a12" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="635" height="172" alt="image" src="https://github.com/user-attachments/assets/06d26d1c-59e7-47d6-a2b0-a0a15e2dae7a" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

