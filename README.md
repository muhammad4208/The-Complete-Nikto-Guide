# Nikto Commands for Web Vulnerability Scanning  

Nikto is a powerful web server scanner that helps identify vulnerabilities and misconfigurations. Below is a categorized list of commands for effective web vulnerability scanning.  

---

## Table of Contents  
1. Basic Commands  
2. Port and Target Management  
3. Proxy and Authentication  
4. Custom Headers and Plugins  
5. SSL/TLS and Evasion Techniques  
6. Output and Logging Options  
7. Advanced Scanning Techniques  

---

## **1. Basic Commands**  
```
nikto -h <target_url> -o scan.html -Format html - Saves the scan results in HTML format.  
```

---

## **2. Port and Target Management**  

### **Scan with Specific Port**  
```
nikto -h <target_url> -p 8080 -o scan_port_8080.txt - Saves the scan results for port 8080.  
```

### **Scan Multiple Targets**  
```
nikto -h targets.txt -o multi_scan_results.txt - Saves results for multiple targets listed in a file.  
```

### **Scan with Full Port Range**  
```
nikto -h <target_url> -port 1-65535 - Saves results for all ports (1-65535) on the target.  
```

---

## **3. Proxy and Authentication**  

### **Use a Proxy**  
```
nikto -h <target_url> -useproxy http://127.0.0.1:8080 - Saves results while routing traffic through a proxy.  
```

### **Scan with Authentication**  
```
nikto -h <target_url> -id admin:password - Saves results using basic authentication.  
```

---

## **4. Custom Headers and Plugins**  

### **Scan with Custom Headers**  
```
nikto -h <target_url> -header "Authorization: Bearer token123" - Adds a custom header to the request.  
```

### **Scan with Specific Plugins**  
```
nikto -h <target_url> -plugins @@PLUGINS - Runs specific Nikto plugins for testing.  
```

---

## **5. SSL/TLS and Evasion Techniques**  

### **Scan for SSL/TLS Issues**  
```
nikto -h <target_url> -ssl - Forces SSL/TLS scanning.  
```

### **Scan with Evasion Techniques**  
```
nikto -h <target_url> -evasion 1 - Uses evasion techniques to bypass detection.  
```

---

## **6. Output and Logging Options**  

### **Scan with Timeout and Retries**  
```
nikto -h <target_url> -timeout 5 -retry 3 - Sets a timeout of 5 seconds and retries failed requests 3 times.  
```

### **Scan with Custom User-Agent**  
```
nikto -h <target_url> -useragent "Mozilla/5.0" - Uses a custom User-Agent string.  
```

### **Scan for Specific Vulnerabilities**  
```
nikto -h <target_url> -Cgidirs all - Checks for CGI directories and common vulnerabilities.  
```

---

## **7. Advanced Scanning Techniques**  

### **Scan with Debug Mode**  
```
nikto -h <target_url> -Debug - Enables debug mode for detailed output.  
```

### **Scan with Mutations**  
```
nikto -h <target_url> -mutate 1 - Uses mutation techniques to discover hidden files or directories.  
```

### **Scan with Database Output**  
```
nikto -h <target_url> -dbcheck - Checks the Nikto database for updates or issues.  
```

### **Scan with No Interactive Prompts**  
```
nikto -h <target_url> -nointeractive - Disables interactive prompts for automated scanning.  
```

### **Scan with Custom Configuration**  
```
nikto -h <target_url> -config /path/to/nikto.conf - Uses a custom configuration file for scanning.  
```

### **Scan with Custom Root Directory**  
```
nikto -h <target_url> -root /custom/path - Sets a custom root directory for scanning.  
```

### **Scan with No Pause Between Tests**  
```
nikto -h <target_url> -nopause - Disables pauses between tests for faster scanning.  
```

### **Scan with Custom Error Detection**  
```
nikto -h <target_url> -404string "Not Found" - Uses a custom string to detect 404 errors.  
```

### **Scan with Verbose Output**  
```
nikto -h <target_url> -vhost example.com - Sets a virtual host and enables verbose output.  
```

### **Scan with All Plugins**  
```
nikto -h <target_url> -Plugins "all" - Runs all available plugins for comprehensive testing.  
```

### **Scan with Custom Time Delay**  
```
nikto -h <target_url> -maxtime 30s - Limits the scan to 30 seconds.  
```

### **Scan with No Follow Redirects**  
```
nikto -h <target_url> -nofollow - Disables following redirects during the scan.  
```

### **Scan with Custom Cookies**  
```
nikto -h <target_url> -cookie "sessionid=12345" - Adds custom cookies to the request.  
```

### **Scan with Custom Request Method**  
```
nikto -h <target_url> -method PUT - Uses a custom HTTP method (e.g., PUT) for testing.  
```

### **Scan with Custom Error Codes**  
```
nikto -h <target_url> -404code 404,500 - Treats specific HTTP codes (e.g., 404, 500) as errors.  
```

---

## **Notes**  
- Always ensure you have permission before scanning any target.  
- Combine Nikto with other tools like `nmap`, `gobuster`, or `sqlmap` for comprehensive testing.  
- For more information, visit the [Nikto GitHub repository](https://github.com/sullo/nikto).  

---
