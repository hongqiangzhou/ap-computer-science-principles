## Class Notes on "AP College Computer Science Principles"

#### Uint 1: Digital Information
__Bits and Bytes:__ 
1. A bit is the smallest piece of information in a computer. A bit has two possible values ("0" or "1").
2. A byte has 8 bits (example: 00010011). Need to know how to convert between bindary and decimal numbers (example: `00010011` represents  `16+2+1=19`). If the last bit is "0", the number must be an even number; if the last bit is "1", it must be an odd number.
3. A byte can represent 256 different decimal numbers (`2^8=256`). The highest number a byte can represent is 255 (`2^8-1`). 
4. When the computer tries to store a number that is bigger than it can handle, it will have an **overflow** error. For example if a computer has 4 bits and it uses the first bit to represent positive/negative sign, the biggest number it can handle is 7. It is fine for this computer to compute `1+6=7`, but will have "overflow" if tries to compute `1+7=8`, since 8 is bigger than 7, the highest number it can store. 
5. Computers use **floating-point representation** for non-integers. For example, 0.5 is represented as `1*2^{-1}`; 0.25 is `1*2^{-2}`. Note the base is always `2`, since computers use **binary** numbers.
6. For **floating-point** numbers, there may be **roundoff** errors. In computer, there is roundoff error for number `0.1`! There is no exact representation of 0.1 as an exponential of 2. Two computers can output slightly different results when they do "floating-point" computation on the same problem, if they have different **precision**.
7. Computers use numbers to represent other information through **encoding**. We learned three encoding systems: **HPE**, **ASCII** (American Standard Code for Information Interchange), and **UTF-8**. Note that **Unicode** is not an encoding scheme. Need to understand how UTF-8 repsent non-English characters. 
8. What is **analog** signal? A continuous stream of varying data. The real world is "analog". Computers store information as **digital numbers**, in forms of bits. 
9. Three steps to convert analog signal into digital numbers: **sampling**, **quantization**, and **binary encoding**. Need to understand concepts: sampling rate, sampling interval, quantization interval, and bit depth.
10. Reconstruction: convert digitalized signals back into analog signals.
11. We use **compression** algorithms to reduce the amount of space (bytes) needed to represent a file. Two types of compression: **loseless** (without lossing any information) and **losy** (discard less important information).
