---
tags: [encoding/ascii]
title: ascii
created: '2019-07-30T06:19:48.987Z'
modified: '2019-07-30T09:06:14.044Z'
---

# ascii

> `ASCII - American Standard Code for Infromation Interchange` is a character `encoding`standard for electronic communication


## ascii character set

```sh
man ascii
```

### print all avail. characters
```sh
for ((i=32;i<127;i++)) do
  printf "\\$(printf %03o "$i")"; 
done
printf "\n"
```
    
| char | oct | hex |dec |
| :--  | :-- | :-- |:-- |
| `"`  | 042 | 22  | 34 |
| `J`  | 112 | 4a  | 74 |


```sh
printf '\112' # or 
echo $'\112'  # octal 
 
printf '\x4a' # hex
 
printf "\\$(printf %o 74)" # or 
xxd -r <<<'0 4a'           # decimal
```


## get decimal-set
```sh
echo '"' | tr -d "\n" | od -An -t uC
#          |            └────────────────  Use od (octal dump) to print:
#          |                                   -An    means Address none
#    remove "newline" char                     -t     select a type
#                                              u      type is unsigned decimal.
#                                              C      of size (one) char


```

## hexdump file
```sh
xxd docker-compose.yml    # hexdump of file
```
[Jafrog's dev blog](http://jafrog.com/2013/11/23/colors-in-terminal.html)


## table hexadecimal

```text
#     _0    _1    _2    _3    _4    _5    _6    _7    _8    _9    _A    _B    _C    _D    _E    _F

# 0_  NUL   SOH   STX   ETX   EOT   ENQ   ACK   BEL   BS    HT    LF    VT    FF    CR    SO    SI
# 0   0000  0001  0002  0003  0004  0005  0006  0007  0008  0009  000A  000B  000C  000D  000E  000F

# 1_  DLE   DC1   DC2   DC3   DC4   NAK   SYN   ETB   CAN   EM    SUB   ESC   FS    GS    RS    US
# 16  0010  0011  0012  0013  0014  0015  0016  0017  0018  0019  001A  001B  001C  001D  001E  001F

# 2_  SP     !    "     #     $     %     &     '     (     )     *     +     ,     -     .     /
# 32  0020  0021  0022  0023  0024  0025  0026  0027  0028  0029  002A  002B  002C  002D  002E  002F 

# 3_  0     1     2     3     4     5     6     7     8     9     :     ;     <     =     >     ?
# 48  0030  0031  0032  0033  0034  0035  0036  0037  0038  0039  003A  003B  003C  003D  003E  003F 

# 4_  @     A     B     C     D     E     F     G     H     I     J     K     L     M     N     O
# 64  0040  0041  0042  0043  0044  0045  0046  0047  0048  0049  004A  004B  004C  004D  004E  004F 

# 5_  P     Q     R     S     T     U     V     W     X     Y     Z     [     \     ]     ^     _
# 80  0050  0051  0052  0053  0054  0055  0056  0057  0058  0059  005A  005B  005C  005D  005E  005F

# 6_  `     a     b     c     d     e     f     g     h     i     j     k     l     m     n     o
# 96  0060  0061  0062  0063  0064  0065  0066  0067  0068  0069  006A  006B  006C  006D  006E  006F

# 7_   p     q     r     s    t      u     v     w     x     y     z     {     |     }     ~     DEL
# 112  0070  0071  0072  0073  0074  0075  0076  0077  0078  0079  007A  007B  007C  007D  007E  007F
```