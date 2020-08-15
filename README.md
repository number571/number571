```asm
format ELF
public _start
section '.data' writeable
  msg db "Learning as a kind of hobby.", 0xA, 0x0
  siz = $-msg
section '.text' executable
_start:
  mov eax, 4
  mov ebx, 1
  mov ecx, msg
  mov edx, siz
  int 0x80
exit:
  mov eax, 1
  xor ebx, ebx
  int 0x80
```
