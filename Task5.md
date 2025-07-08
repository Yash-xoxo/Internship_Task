### **Task 5: Send Messages from the Terminal**

_Email/WhatsApp/Tweet/SMS without leaving CLI:_

- **Email** → `mutt`/`mail`:
    
    bash
    
    ```echo "Body" | mail -s "Subject" user@example.com```
    
- **WhatsApp** → `yowsup` (Python library).
    
- **Tweet** → `t` (Ruby CLI):
    
    bash
    
    ```t update "Linux is awesome! #TerminalPower"```
    
- **SMS** → Twilio API + `curl`.
