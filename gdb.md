# Focus Area: Process Debugging with `gdb`

## Problem  
You need to debug a running process on your Linux system:  
- Identify a process to debug using `ps` or `top`.  
- Attach to the process using `gdb`.  
- List the backtrace of the running threads.  
- Detach from the process safely without terminating it.

## Commands to Learn and Practice  
- `ps aux | grep <process>`  
- `sudo gdb -p <PID>`  
- Inside `gdb`:  
  - `bt` (to get the backtrace)  
  - `detach` (to safely detach)  
  - `quit` (to exit `gdb`)  

## Interview Quiz  
1. What is `gdb`, and when would you use it?  
2. How can you debug a core dump using `gdb`?  
3. What is the difference between attaching `gdb` to a running process and starting a program inside `gdb`?
