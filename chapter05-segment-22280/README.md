# Problem

* READ VALUES FROM IN.A AND IN.B
* READ A VALUE FROM IN.S
* WRITE IN.A WHEN IN.S = -1
* WRITE IN.B WHEN IN.S = 1
* WRITE IN.A + IN.B WHEN IN.S = 0

# Solution

264 CYCLES / 5 NODES / 16 INSTR

```
@0
# 0: 15
# 1: 14
#-1: 10

@1
MOV UP, RIGHT

@2
START:
MOV UP, ACC
JEZ SUM
JLZ READ_L
MOV LEFT, NIL
MOV RIGHT, DOWN
JMP START
READ_L:
MOV LEFT, DOWN
MOV RIGHT, NIL
JMP START
SUM:
MOV LEFT, ACC
ADD RIGHT
MOV ACC, DOWN

@3
MOV UP, LEFT

@4


@5


@6
MOV UP, DOWN

@7


@8


@9
MOV UP, DOWN

@10


```

# Hint
Notice that the input data has following distribution
```
 0: 15
 1: 14
-1: 10
```

So it should check `0` first, then check `1`, then check `-1` to minimize the cycle count to 264. Otherwise the cycle count will be 272.