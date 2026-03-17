# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
```
MOV A,30H;
ADD A,31H;
MOV 40H,A;
JNC NEXT;
MOV 41H,#01H;
SJMP END_PROGRAM;
NEXT:MOV 41H,#00H;
END_PROGRAM:NOP;
END
```

## Output:
<img width="1920" height="1200" alt="Screenshot 2026-03-12 141912" src="https://github.com/user-attachments/assets/56302c50-37ee-4239-8696-26d7bc530411" />
<img width="957" height="217" alt="Screenshot 2026-03-12 142122" src="https://github.com/user-attachments/assets/5ea68bfc-fa39-4d91-915c-f4bbf11147b5" />
<img width="959" height="215" alt="Screenshot 2026-03-12 142058" src="https://github.com/user-attachments/assets/e8037d41-6b60-4516-a53d-21c8d0cecaea" />

## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
  ORG 0000H
  MOV A,30H
  SUBB A,31H
  MOV 40H,A
  JNC NEXT 
  MOV 41H,#01H;
  SJMP END_PROGRAM;
  NEXT:MOV 41H,#00H;
  END_PROGRAM:NOP;
  END
```

## Output:
<img width="1920" height="1200" alt="Screenshot 2026-03-13 153323" src="https://github.com/user-attachments/assets/22a4191e-5d64-49a9-889f-ea07aaaa74b6" />
<img width="956" height="215" alt="Screenshot 2026-03-13 153345" src="https://github.com/user-attachments/assets/faa83694-6088-4229-adfd-251e60e0d01d" />
<img width="958" height="167" alt="Screenshot 2026-03-13 153358" src="https://github.com/user-attachments/assets/696f8eda-f041-4044-9531-582571cb6ba9" />

## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
ORG 0000H
MOV A, 30H 
MOV B, 31H
MUL AB
MOV 40H, A 
MOV 41H, B
END
```

## Output:
<img width="1920" height="1200" alt="Screenshot 2026-03-13 154422" src="https://github.com/user-attachments/assets/1c0964e7-ffdb-4450-afb4-6a922f2583d0" />
<img width="955" height="188" alt="Screenshot 2026-03-13 154445" src="https://github.com/user-attachments/assets/60555a75-6921-4148-b2a6-a37b3da33665" />
<img width="959" height="198" alt="Screenshot 2026-03-13 154456" src="https://github.com/user-attachments/assets/3ed34228-ac08-4b50-8030-f81bfbce21bc" />

## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
ORG 0000H
MOV A, 30H
MOV B, 31H
DIV AB
MOV 40H, A
MOV 41H, B 
END
```

## Output:
<img width="1920" height="1200" alt="Screenshot 2026-03-13 154815" src="https://github.com/user-attachments/assets/8f6e52f2-b9e9-4146-954d-3610dba0df71" />
<img width="960" height="197" alt="Screenshot 2026-03-13 154738" src="https://github.com/user-attachments/assets/d0950626-0e47-4fb2-ba0f-b19591fa2492" />


## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

