# Focus Area: Understanding `strace` for Debugging

## Problem  
You need to troubleshoot a misbehaving application using `strace`:  
- Use `strace` to monitor the system calls of a simple command like `ls`.  
- Redirect the output of `strace` to a file named `strace_ls.log`.  
- Identify which files are being accessed by the `ls` command.  
- Use `strace` to troubleshoot a program that fails to start due to a missing file or permission issue.

## Commands to Learn and Practice  
- `strace ls`  
- `strace -o strace_ls.log ls`  
- `grep open strace_ls.log`  
- `strace -e trace=open ./my_program`

## Interview Quiz  

1. What is `strace`, and how does it help in debugging?  
<details>
  <summary>Show Answer</summary>
  `strace` is a debugging tool that traces system calls made by a program. It helps identify what the program is attempting to do—such as opening files, reading data, or interacting with the network—and is particularly useful for diagnosing errors like missing files, permission issues, or unexpected behavior in system interactions.
</details>

2. How can you filter `strace` output to focus on specific system calls?  
<details>
  <summary>Show Answer</summary>
  Use the `-e trace=` option followed by the system calls you’re interested in. For example, `strace -e trace=open,read,write ./my_program` will show only calls related to file opening and I/O operations.
</details>

3. How would you use `strace` to debug a network-related issue?  
<details>
  <summary>Show Answer</summary>
  You can trace network-related system calls, such as `connect`, `accept`, `send`, and `recv`. By filtering on these calls (`-e trace=connect,accept,send,recv`), you can see exactly how your application is interacting with the network, identify connection failures, or pinpoint unexpected latency.
</details>
