# Problem

* READ A VALUE FROM IN.A
* DOUBLE THE VALUE
* WRITE THE VALUE TO OUT.A

# Solution

84 CYCLES / 6 NODES / 12 INSTR

```
@0


@1
MOV UP, RIGHT
MOV UP, DOWN

@2
MOV LEFT, DOWN

@3


@4
MOV UP, ACC
ADD ACC
MOV ACC, DOWN

@5
MOV UP, ACC
ADD ACC
MOV ACC, DOWN

@6


@7
MOV UP, RIGHT

@8
MOV UP, DOWN
MOV LEFT, DOWN

@9

```