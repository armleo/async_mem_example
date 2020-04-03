# Introduction
How to make async memory from block ram?
This design constructs slow sync write, async read memory using clock division and sync memory.

Essentially we divide out clock in to 4 cycles
On falling edge of internal_clk (counter == 0) we fetch data from address and put it into raddr
Now on rising edge (counter == 2) our design (which is clocked of internal_clk) has valid rdata coressponding to raddr