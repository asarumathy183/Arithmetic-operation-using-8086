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
| 1200:12                 | 1204:24                  |
| 1201:34                 | 1205:68                  |
| 1203:12                 | 1206:00                  |
| 1204:34                 |                          |

#### Manual Calculations

![add](https://github.com/user-attachments/assets/8880dc02-323f-4db9-9c69-5a876302b40b)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

![add code](https://github.com/user-attachments/assets/50f44adb-19f9-47d1-9b52-1899cb065869)
![add output](https://github.com/user-attachments/assets/781d739f-0126-4c74-b464-dedaed6f8dd0)

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
| 1200:12                 | 1204:00                  |
| 1201:34                 | 1205:22                  |
| 1203:12                 | 1206:00                  |
| 1204:12                 |                          |

#### Manual Calculations

![sub](https://github.com/user-attachments/assets/6486561b-c634-4e30-82d1-5be8bb4366bc)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

![sub code](https://github.com/user-attachments/assets/4153958a-bbb6-436f-b310-c71507b30106)
![sub output](https://github.com/user-attachments/assets/c802c321-b1b5-4f28-9ccf-d67cc7c4ab73)


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
| 1200:12                 | 1204:44                  |
| 1201:34                 | 1205:51                  |
| 1203:12                 |                          |
| 1204:34                 |                          |

#### Manual Calculations

![mul](https://github.com/user-attachments/assets/898d067d-a029-4de6-ba65-8732d5f514ba)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

![mul code](https://github.com/user-attachments/assets/5ba06986-eba3-45c1-aba4-628c19adc8c9)
![mul output](https://github.com/user-attachments/assets/872c3f4d-a56d-40ab-8563-d8ec821c1939)

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
| 1200:12                 | 1204:01                  |
| 1201:34                 | 1205:00                  |
| 1203:12                 | 1206:00                  |
| 1204:34                 |                          |

#### Manual Calculations

![div](https://github.com/user-attachments/assets/7e51837f-80e1-4530-98fe-fc7e7bec6deb)

---
## OUTPUT FROM MASM SOFTWARE

![div code](https://github.com/user-attachments/assets/5003180b-5f2b-4007-8de6-b42be1fd1842)
![div output](https://github.com/user-attachments/assets/3b80380c-e69c-4e1f-823f-616bf9ab88e9)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
