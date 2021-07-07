## Class Notes on "AP College Computer Science Principles"

#### Uint 1: Digital Information
__Bits and Bytes:__ 
1. A bit is the smallest piece of information in a computer. A bit has two possible values ("0" or "1").
2. A byte has 8 bits (example: 00010011). Need to know how to convert between bindary and decimal numbers (example: `00010011` represents  `16+2+1=19`). If the last bit is "0", the number must be an even number; if the last bit is "1", it must be an odd number.
3. A byte can represent 256 different decimal numbers (`2^8=256`). The highest number a byte can represent is 255 (`2^8-1`). 
4. __Overflow__: When the computer tries to store a number that is bigger than it can handle. For example if a computer has 4 bits and it uses the first bit to represent positive/negative sign, the biggest number it can handle is 7. It is fine for this computer to compute `1+6=7`, but will have __overflow__ if tries to compute `1+7=8`, since 8 is bigger than 7, the highest number it can store.
5. Computers use __floating-point representation__ for non-integers. For example, 0.25 is represented in computer by `1*2^{-2}`. Note the base is always `2`, since computers use **binary** numbers.
6.  
