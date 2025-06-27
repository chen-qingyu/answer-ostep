## 5 Interlude: Process API

### Simulation

1. Result:

   ![img](./images/1.png)

2. While fork percentage is higher, the final process tree is bigger.

3. Result:

   ![img](./images/2.png)

   a forks b; b exits; a forks c; a forks d; d forks e.

4. When 'c' exits, orphaned process re-parent to 'a'. When use -R flag, orphaned process re-parent to 'b' (re-parent to local parent).

5. Result:

   ![img](./images/3.png)

   ```
   a
   |-b
   | |-f
   |-c
   |-d
       |-e
   ```

6. Result:

   ![img](./images/4.png)

   - a forks b; b forks c; c exits; b forks d; b forks e.
   - a forks b; b forks c; b forks d; c exits; b forks e.
   - a forks b; b forks c; b forks d; b forks e; c exits.
   - a forks b; a forks c; c exits; b forks d; b forks e.
   - a forks b; a forks c; b forks d; c exits; b forks e.
   - a forks b; a forks c; b forks d; b forks e; c exits.

### Code

1. `x = 100`, the variable in the child process is 100 too. `x` is independent.![img](./images/5.png) ![img](./images/6.png)
2. Yes, both child and parent can access the file descriptor. When they write at the same time, they all write successfully.![img](./images/7.png)

3. Yes, just use `sleep()`.![img](./images/8.png)

4. Because system have to meet different needs.![img](./images/9.png)

5. `wait()` return the PID of child process. In the child, `wait()` return -1.![img](./images/10.png)

6. When know the exact PID, use `waitpid()`.![img](./images/11.png)

7. After close standard output, there are no outputs.![img](./images/12.png)

8. Result:

   ![img](./images/13.png)
