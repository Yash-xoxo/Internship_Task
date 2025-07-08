### **Task 1: Blogging via Terminal with Medium’s API**

_No GUI? No problem! Post directly to Medium from your terminal:_

1. **Prerequisites**:
    
    - Medium account + [Integration Token](https://medium.com/me/settings).
        
    - `curl` or Node.js installed.
        
2. **Get User ID**:
    
    bash
    
    curl -H "Authorization: Bearer YOUR_TOKEN" https://api.medium.com/v1/me  
    
3. **Post Article**:
    
    bash
    
    curl -X POST https://api.medium.com/v1/users/YOUR_USER_ID/posts \  
      -H "Authorization: Bearer YOUR_TOKEN" \  
      -H "Content-Type: application/json" \  
      -d '{  
        "title": "Linux in Enterprises: Why 90% of Fortune 500 Runs It",  
        "contentFormat": "markdown",  
        "content": "# Companies Love Linux...",  
        "publishStatus": "public"  
      }'  
    

_Pro Tip_: Use `links2` for terminal web browsing!
