# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**
---
## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />
---
## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END
```
OUTPUT
<img width="1919" height="1077" alt="Screenshot 2025-09-22 233738" src="https://github.com/user-attachments/assets/f89683a5-e057-4339-b4a1-0eef9b17fb37" />
<img width="818" height="493" alt="Screenshot 2025-09-22 233806" src="https://github.com/user-attachments/assets/a9aa5da9-8159-4683-b385-d28af44ac568" />
---
MANUAL CALCULATIONS
![MPMC MANUAL FACTORIAL CAL](https://github.com/user-attachments/assets/d0f28959-a8a7-4a67-8262-49239eb222c9)
---
RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.
---


