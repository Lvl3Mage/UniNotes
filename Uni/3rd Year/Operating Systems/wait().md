### **`wait()` and `waitpid()`**

- **`wait()`**: Suspends the calling process until one of its child processes terminates. It returns the PID of the terminated child or `-1` if an error occurs.
- **`waitpid()`**: Similar to `wait()`, but provides more control. It can wait for a specific child process or modify its behavior using options.

### **Methods**
- **`wait(int *status)`**: Waits for any child process to terminate and stores its exit status.
- **`waitpid(pid_t pid, int *status, int options)`**: Waits for a specific child process (`pid`) to terminate. You can specify:
  - `pid > 0`: Wait for the specific child.
  - `pid = -1`: Wait for any child (same as `wait()`).
  - `options`: Special flags (e.g., `WNOHANG` to return immediately if no child has exited).

### **Example in C**
```c
#include <stdio.h>
#include <sys/wait.h>
#include <unistd.h>

int main() {
    pid_t child_pid = fork();

    if (child_pid == 0) {
        // Child process
        printf("Child process with PID: %d\n", getpid());
        return 42; // Exit with status 42
    } else {
        // Parent process
        int status;
        waitpid(child_pid, &status, 0); // Wait for the child process to terminate

        if (WIFEXITED(status)) {
            printf("Child exited with status: %d\n", WEXITSTATUS(status));
        }
    }
    return 0;
}
```

### **Key Points**
- **`wait()`**: Waits for any child, returns when one exits.
- **`waitpid()`**: Wait for a specific child (or any child if `pid=-1`) with optional flags for finer control.