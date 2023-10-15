# Wap to convert 10 ASCII characters to their lowercase equivalents if there are any uppercase from memory location 9050h in 8085.
LXI H,9650
MVI C,0AH
LOOP:
  MOV A,M
  CPI 97h
  JNC L:
  ADD 20H
L:
  INX H
  DCR C
  JNZ LOOP
HLT
