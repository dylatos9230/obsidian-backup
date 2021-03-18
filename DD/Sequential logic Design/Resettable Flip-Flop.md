## Introduction
- A resettable flip-flop adds another input called **RESET**.
- When **RESET** is  FALSE, the resettable flip-flop behaves lile an ordinary D flip-flop.
- When **RESET** is TRUE, the resettable flip-flop ignores D and resets the output to 0.
- Resettable flip-flops are useful when we want to force a known state into all the flip-flops in a system when we first turn it on.
- Such flip-flops may be **synchronously** or **asynchronously** resettable.
## Synchronously
- Synchronously resettable flip-flops reset themselves only on the rising edge of **CLK**
- When RESET is FALSE, the AND gate forces a 0 into the input of the flip-flop
- When RESET is TRUE, the AND gate passes D to the flip-flop
#### Schematic
![[Pasted image 20210122002452.png]]
#### Symbols
![[Pasted image 20210122002755.png]]

## Asynchronously
- Asynchronously resettable filp-flops reset themselves as soon as RESET becomes TRUE, independent of CLK.
