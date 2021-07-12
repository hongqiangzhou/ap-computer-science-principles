## Class Notes on "AP College Computer Science Principles"

#### Uint 1: Digital Information

1. A **bit** is the smallest piece of information in a computer. A bit has two possible values ("0" or "1").
2. A **byte** has 8 bits (example: 00010011). Need to know how to convert between bindary and decimal numbers (example: `00010011` represents  `16+2+1=19`). If the last bit is "0", the number must be an even number; if the last bit is "1", it must be an odd number.
3. A byte can represent 256 different decimal numbers (`2^8=256`). The highest number a byte can represent is 255 (`2^8-1`). 
4. When the computer tries to store a number that is bigger than it can handle, it will have an **overflow** error. For example if a computer has 4 bits and it uses the first bit to represent positive/negative sign, the biggest number it can handle is 7. It is fine for this computer to compute `1+6=7`, but will have "overflow" if tries to compute `1+7=8`, since 8 is bigger than 7, the highest number it can store. 
5. Computers use **floating-point representation** for non-integers. For example, 0.5 is represented as `1*2^{-1}`; 0.25 is `1*2^{-2}`. Note the base is always `2`, since computers use **binary** numbers.
6. For **floating-point** numbers, there may be **roundoff** errors. In computer, there is roundoff error for number `0.1`! There is no exact representation of 0.1 as an exponential of 2. Two computers can output slightly different results when they do "floating-point" computation on the same problem, if they have different **precision**.
7. Computers use numbers to represent other information through **encoding**. We learned three encoding systems: **HPE**, **ASCII** (American Standard Code for Information Interchange), and **UTF-8**. Note that **Unicode** is not an encoding scheme. Need to understand how UTF-8 repsent non-English characters. 
8. What is **analog** signal? A continuous stream of varying data. The real world is "analog". Computers store information as **digital numbers**, in forms of bits. 
9. Three steps to convert analog signal into digital numbers: **sampling**, **quantization**, and **binary encoding**. Need to understand concepts: sampling rate, sampling interval, quantization interval, and bit depth.
10. Reconstruction: convert digitalized signals back into analog signals.
11. We use **compression** algorithms to reduce the amount of space (bytes) needed to represent a file. Two types of compression: **loseless** (without lossing any information) and **losy** (discard less important information).
12. Loseless text compression: find repeated sequences and replace them with shorter representations. Need a table to store representations and meaning.
13. Loseless image compression. Need to understand bigmap and run-length encoding (RLE, run: sequence of bits with the same value). Fax machines use RLE. JPEG uses RLE during final stage of compression.
14. Loseless bit compression: Huffman coding. Represent the most common characters with shorter codes.
15. Losy compression. Images: keep the brightness, average the color (Chroma subsampling). Audio: drop inaudible sounds.
16. Copyright. Good to know: fair use, digital rights management (DRM), The Digital Millennium Copyright Act (DMCA), Creative Commons, open source. public domain.

#### Unit 2: The Internet

1. **Local Area Network** (LAN, for example a network at school), **Wide Area Network** (WAN, Internet is a WAN). A WAN can include many LANs, **Data Center Network** (DCN).
2. Computing devices use **protocals** to communicate with each other.
3. **Bit rate**: Number of bits sent in each second (bps: bits per second).
4. **Bandwidth**: the **maximum** bit rate of a system. For example, a network has a bandwitdh of 10 Mbps cannot send or receive 11 M bits in one second.
5. Good to know but not required. In computer, "K" ("kilo") means 1024, "M" ("Mega") means `1024 * 1024`, "G" ("Giga") means `1024 * 1024 * 1024`.
6. **Latency** how late the bits arrives. We typically mean "**round-tip**" latency: time between we send out the message and receive the reply.
7. Internet speed is measured by both **bandwidth** and **latency** (lentency, download bandwidth, upload bandwidth).
8. Internet uses **IP address** (IP: Internet Protocol) to identity a device. Two types: IPv4 and IPv6. To understand that IP address is represented by a sequence of bits.
9. IPv4 has **32** bits. Values include 4 numbers between 0 and 255, and separated by "." (for example: 69.137.34.64). The number of different IPv4 addresses in the world is `2^32`.
10. IPv6 has **128** bits. An IPv6 address has 8 **hexadecimal** numbers and each number has 4 digits. A hexadecimal digit has 16 values, 0-9 and then a-f. A 4-digit hexadecimal number looks like "0fa1" (its decimal value should be `15*16^2+10*16+1=4001`. The number of different IPv6 addresses in the world is `2^128`.
11. **IP address hierarch**: first sequence of bits identifies the network and final bits identity the individual node (computer, etc). For example, "141.213.127.13", "141.213" indicates University of Michigan, "127" Medicine Department, "13" an individual computer.
12. Note that **IP address** is nothing more than a sequence of bits. We do not have to use a whole number (8 bits, 0-255) to represent a department. Suppose UMich has 30 departments, and each department has more than 1000 computers. We can use 5 digits, instead of 8, to represent departments (`2^5=32`), and remaining 11 bits to represent individual computers (`2^11=2048`). 
13. Internet sends messages in **packets**. Big message can be split into multiple packets. A pecket includes a **header** and data. The header includes IP addresses of both sender and receiver (like a letter envolope).
14. Computer sends a packet to the nearest **router**. The router checks its **forwarding table** and forwards this packet to next router that is closer to the destination. Through multiple routers, eventually, the packet reaches its destination. Imagine this is like we send a mail trough post offices.
15. **Redundancy**: There are often many possible paths a packet can go down to reach its destination. 
16. **Fault tolerance**: The internet can experience many failures but still can deliver your message to its destination. "Fault tolerance" is because of "redundancy". No **single point of failure**.
17. **Transmission Control Protocal (TCP)**: used on top of IP to handle packets (ordering, retransmission, and data integrity). **User Datagram Protocal (UDP)** solves few problems but is faster than TPC (joked as "Unreliable Data Protocol"), used for time-sensitive applications (such as video streaming).
