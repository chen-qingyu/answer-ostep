## 4 The Abstraction: The Process

### Simulation

1. the CPU utilization is 100%. Because there is no IO request.![img](./images/1.png)

2. 4+1+5+1=11 ticks.![img](./images/2.png)

3. Shorter time (11 => 7). Yes, switching the order matter. Because when IO run, CPU also run.![img](./images/3.png)

4. Longer time (7 => 11).![img](./images/4.png)

5. Shorter time (11 => 7).![img](./images/5.png)

6. System resources not being effectively utilized.![img](./images/6.png)

7. Short time (31 => 21). Because both CPU and IO is used.![img](./images/7.png)

8. IO_RUN_IMMEDIATE vs. IO_RUN_LATER: almost equal. Sometimes IO_RUN_IMMEDIATE better.

   SWITCH_ON_IO better than SWITCH_ON_END.
