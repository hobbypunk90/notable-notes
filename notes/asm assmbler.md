---
title: asm assmbler
created: '2019-07-30T06:19:48.988Z'
modified: '2019-12-30T07:38:12.341Z'
---

# asm assmbler

## usage
```
EAX,EBX,ECX,EDX - "general purpose", more or less interchangeable

lea  rbx, qword [..]

```

```c
unsigned long a1, r;
void junk( void )
{
   asm(
        "pushl %eax \n"
        "pushl %ebx \n"
        "movl $100,%eax \n"
        "movl a1,%ebx \n"
        "int $69 \n"
        "movl %eax,r \n"
        "popl %ebx \n"
        "popl %eax \n"
   );
}
```

## see also
- 

