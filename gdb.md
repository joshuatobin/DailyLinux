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

<details>
  <summary>Show Answer</summary>
  `gdb` is a debugger that allows you to inspect running processes, analyze core dumps, and step through code to identify bugs.
</details>

2. How can you debug a core dump using `gdb`?

<details>
  <summary>Show Answer</summary>
  Use `gdb <program> <core>` to load the program’s binary and core file. Once inside `gdb`, you can use commands like `bt` (backtrace) to see where the program crashed.
</details>

3. What is the difference between attaching `gdb` to a running process and starting a program inside `gdb`?

<details>
  <summary>Show Answer</summary>
  Attaching `gdb` to a running process lets you inspect it as-is, preserving its current state. Starting a program inside `gdb` runs it from the beginning, allowing you to step through its initialization and early execution.
</details>
