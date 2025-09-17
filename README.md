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
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200                   |     32                   |
|  1201                   |     67                   |
|  1202                   |     15                   |
|  1203                   |     27                   |
|  1204                   |     47                   |
|  1205                   |     8E                   |
|1206|00|
#### Manual Calculations

![WhatsApp Image 2025-09-17 at 21 44 47_8b642030](https://github.com/user-attachments/assets/16e45eb1-233f-4952-bb5e-915ffb1a7043)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

![WhatsApp Image 2025-09-17 at 21 49 47_b1c91e9c](https://github.com/user-attachments/assets/93224a87-cc0c-47f2-aa0b-ffa64660c2f8)


![WhatsApp Image 2025-09-17 at 21 49 34_3f5298e1](https://github.com/user-attachments/assets/2d274294-24dd-4037-b32d-313466632cda)


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
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200                   |  45                      |
|  1201                    |67|
| 1202|31|
|1203|23|
|1204|14|
|1205|44|
|1206|00|

#### Manual Calculations

![WhatsApp Image 2025-09-17 at 21 49 48_70216624](https://github.com/user-attachments/assets/941ac0f8-9568-4e9c-ab52-8c61ef3f2cb7)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-17 at 21 49 45_69aaec38](https://github.com/user-attachments/assets/e4ecad02-b880-4675-8c3d-e738374d544e)

![WhatsApp Image 2025-09-17 at 21 49 38_43725ee4](https://github.com/user-attachments/assets/b753afeb-533c-4e97-b65c-ff1d239d1a6d)


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
|    1200                     |    12                      |
|1201|34|
|1202|12|
|1203|34|
|1204|44|
|1205|51|
|1206|97|
|1207|0A|

#### Manual Calculations

![WhatsApp Image 2025-09-17 at 22 07 20_c7059d49](https://github.com/user-attachments/assets/102f7bc5-5447-4e91-9fe0-c0bbfd5e078f)



---

## OUTPUT SCREEN FROM MASM SOFTWARE

![WhatsApp Image 2025-09-17 at 21 49 28_27f5cade](https://github.com/user-attachments/assets/99db6d3d-cbef-4b57-a6da-ae78c16308d0)

![WhatsApp Image 2025-09-17 at 21 49 39_573a3923](https://github.com/user-attachments/assets/fb909008-2b65-49a5-b9f3-bb0d6353ca76)



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
|   1200                      |              12            |
|1201|34|
|1202|12|
|1203|34|
|1204|01|
|1205|00|
|1206|00|
|1207|00|
#### Manual Calculations

![WhatsApp Image 2025-09-17 at 22 12 57_8dbbe35f](https://github.com/user-attachments/assets/660bdc37-179d-47a5-ae0b-37973f0eae6d)


---
## OUTPUT FROM MASM SOFTWARE

![WhatsApp Image 2025-09-17 at 21 49 37_f31dbdc0](https://github.com/user-attachments/assets/75074cfe-1c34-4711-8059-2aa8f699ad7d)

![WhatsApp Image 2025-09-17 at 21 49 49_ee92aa8e](https://github.com/user-attachments/assets/9defdc7d-e653-4780-86fc-eb3a0e157be3)

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

