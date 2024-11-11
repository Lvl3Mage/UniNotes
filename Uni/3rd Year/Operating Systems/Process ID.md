### **PID and PPID**

- **PID (Process ID)**: A unique identifier assigned by the operating system to each running process.
- **PPID (Parent Process ID)**: The process ID of the parent process, i.e., the process that spawned the current process.

### **Methods**
- **`getpid()`**: Returns the process ID of the calling process.
- **`getppid()`**: Returns the parent process ID of the calling process.

### **Example in C**
```c
#include <stdio.h>
#include <unistd.h>

int main() {
    pid_t pid = getpid();   // Get current process ID
    pid_t ppid = getppid(); // Get parent process ID

    printf("PID: %d\n", pid);
    printf("PPID: %d\n", ppid);

    return 0;
}
```

### **Key Points**
- Use `getpid()` to retrieve the current process ID.
- Use `getppid()` to retrieve the parent process ID.
