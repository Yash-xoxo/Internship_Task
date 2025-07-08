### **Task 2: Reverse-Engineering GUI Programs**

_Ever wondered what commands your GUI apps run?_

- **Tool**: `strace` (trace system calls).
    
- **Example**: Tracking `gnome-disks`:
    
    bash
    
    ```strace -f -e execve gnome-disks 2>&1 | grep udisksctl```
    

_Discovery_: Gnome Disks silently runs `udisksctl` commands!
