
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**
![WhatsApp Image 2025-11-13 at 17 02 45_edacdd2e](https://github.com/user-attachments/assets/46dfad97-7446-4b30-b681-b58b5e5478fd)

**MEMORY WINDOW:**

Before execution: D:0x40H:

![WhatsApp Image 2025-11-11 at 21 09 30_14ae2c90](https://github.com/user-attachments/assets/721d16ee-4770-45c5-9dec-76cf096a5d38)

After execution: D:0x40H:

![WhatsApp Image 2025-11-11 at 21 09 30_9c5308e7](https://github.com/user-attachments/assets/b3781dfe-129b-4a36-b308-cafc2d98989c)



**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**
![WhatsApp Image 2025-11-13 at 17 02 46_d9bf867d](https://github.com/user-attachments/assets/4aad2863-85a8-40c0-95a3-3e31a3ba29b3)

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:

![WhatsApp Image 2025-11-11 at 21 30 53_8fdbbb68](https://github.com/user-attachments/assets/e7ba2150-a8f5-4bff-a7e9-c4ff327e001e)

After execution:
D:0x40H:

![WhatsApp Image 2025-11-11 at 21 29 59_612ae07c](https://github.com/user-attachments/assets/985e73fa-beeb-44be-96af-02a085b5a11d)

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

