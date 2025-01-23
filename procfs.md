# Focus Area: Exploring `/proc` Filesystem

## Problem  
You need to gather system and process information using the `/proc` virtual filesystem:  
- List the contents of the `/proc` directory and explore its structure.  
- Inspect `/proc/cpuinfo` and `/proc/meminfo` to gather details about the CPU and memory of the system.  
- Choose an active process (using its PID) and examine the contents of `/proc/<PID>/status` and `/proc/<PID>/fd/` to understand its state and open file descriptors.  
- Summarize what you learned from the `/proc` filesystem and its practical use cases.

## Commands to Learn and Practice  
- `ls /proc`  
- `cat /proc/cpuinfo`  
- `cat /proc/meminfo`  
- `ls /proc/<PID>/fd/`  
- `cat /proc/<PID>/status`

## Interview Quiz  

1. What is the `/proc` filesystem, and how does it differ from regular filesystems?  
<details>
  <summary>Show Answer</summary>
  The `/proc` filesystem is a virtual filesystem that provides a window into the kernel and system state. Unlike regular filesystems that store persistent data, `/proc` dynamically generates its content, reflecting the current state of the kernel, processes, and system hardware in real-time.
</details>

2. How can you use `/proc` to monitor system performance in real time?  
<details>
  <summary>Show Answer</summary>
  You can examine files such as `/proc/stat` for CPU statistics, `/proc/meminfo` for memory usage, and `/proc/loadavg` for system load averages. By reading these files periodically, you get a live view of how the system is performing.
</details>

3. What kind of information can you retrieve from `/proc/<PID>/cmdline`?  
<details>
  <summary>Show Answer</summary>
  `/proc/<PID>/cmdline` contains the exact command-line arguments used to start the process. This can help you understand how the process was invoked, what parameters were passed, and its configuration at launch.
</details>
