### **Task 6: Demystify Ctrl+C / Ctrl+Z**

_Keyboard shortcuts = Linux signals!_

- **Ctrl+C** → `SIGINT` (Signal 2):
    
    bash
    
    ```kill -2 PID  # Forcefully terminate```
    
- **Ctrl+Z** → `SIGTSTP` (Signal 20):
    
    bash
    
    ```kill -20 PID  # Pause (background)```
    

_Handle signals in scripts_:

bash

```trap 'echo SIGINT caught!' SIGINT ``` 
