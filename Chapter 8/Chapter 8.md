## 8 Scheduling: The Multi-Level Feedback Queue

### Simulation

1. Result:

   ![img](./images/1.png)

   ![img](./images/2.png)

   I had a question at the beginning: why is ALLOT only 1, but after running 1 ticks, it's priority is not reduced? Think about it, because ALLOT is based on a time slice.

   ![img](./images/3.png)

   ![img](./images/4.png)

   So, there is an error in README: ALLOT is measured in time slices, not milliseconds.![img](./images/5.png)

2. Example 1:

   ![img](./images/6.png) ![img](./images/7.png)

   Example 2:

   ![img](./images/8.png) ![img](./images/9.png)

   Example 3:

   ![img](./images/10.png) ![img](./images/11.png)

3. Result:

   ![img](./images/12.png) ![img](./images/13.png)

4. Result:

   ![img](./images/14.png)

5. Boost = 10 ms / 0.05 = 200 ms.

6. With the `-I` flag:

   ![img](./images/15.png)

   Without the `-I` flag:

   ![img](./images/16.png)
