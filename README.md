8 bit = 1 byte  
16 bit = 2 byte = 1 word  
32 bit = 4 byte = 2 word = 1 dword (double-word)  
64 bit = 8 byte = 4 word = 1 qword (quad-word)  

```asm
%include "io64.inc"

section .text
global CMAIN
CMAIN:
    mov rbp, rsp; for correct debugging


    mov eax, 0x1234
    mov rbx, 0x12345678
    mov cl, 0xff
    
    mov al, 0x00 ; 0x1234 -> 0x1200
    mov rax, rdx
    
    xor rax, rax
    ret
    
section .data
    msg db  'Hello World', 0x00
```
