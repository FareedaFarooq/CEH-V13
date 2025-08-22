# Web Server Architectures and Attacks — Easy Guide

---

## 1. Apache Web Server Architecture

**Apache** is an open-source, modular, and process-based web server.

### Key Points:
- **Modular:** Features can be added/removed using modules (like mod_ssl for HTTPS).
- **Process-based:** Each client request is handled by a separate process or thread.
- **Configurable:** Uses `httpd.conf` & `.htaccess` files for configuration.

### Diagram (Simple)
```
Client ---> Apache Listener ---> Request Handler ---> Response ---> Client
                 |                        |
            [Modules]                [Static/Dynamic Content]
```

### Advantages
- **Flexible:** Add only needed modules.
- **Cross-platform:** Works on Linux, Windows, Mac.
- **Widely supported:** Huge community, lots of tutorials.
- **Secure:** Regular updates & security patches.

---

## 2. IIS Web Server Architecture

**IIS (Internet Information Services)** is Microsoft’s web server for Windows.

### Key Points:
- **Integrated with Windows:** Uses Windows authentication and management tools.
- **Component-based:** Uses services (WWW, FTP, SMTP).
- **Worker process model:** Uses `w3wp.exe` to handle requests.

### Diagram
```
Client ---> HTTP.SYS (Kernel) ---> IIS Worker Process (w3wp.exe) ---> Application Pool ---> Response
```

---

## 3. Web Server Attacks

### a) DNS Server Hijacking
- **What:** Attackers change your DNS server settings.
- **Result:** Visitors are sent to fake/malicious sites.

### b) Directory Traversal Attack (Important)
- **What:** Attackers access files/folders outside the web root by manipulating URL paths.
- **Example:**
  ```
  http://example.com/index.php?page=../../../../etc/passwd
  ```
- **Risk:** Can read sensitive files like passwords.

### c) Web Server Misconfigurations
- **What:** Weak/default settings (e.g., default passwords, directory listing enabled).
- **Risk:** Attackers exploit these for unauthorized access.

### d) HTTP-Response-Splitting Attack (Important)
- **What:** Malicious input splits HTTP response into two parts.
- **Risk:** Used for stealing data or injecting content.

### e) Web Cache Poisoning Attack
- **What:** Attackers trick web cache into storing harmful responses.
- **Result:** Future visitors get malicious content from cache.

### f) SSH Brute Force Attack
- **What:** Attackers try many username/password combos to access SSH.
- **Risk:** Unauthorized shell access.

### g) FTP Brute Force
- **What:** Similar to SSH, but targets FTP login.

### h) HTTP/2 Continuation Flood Attack
- **What:** Abuses HTTP/2 protocol, sends endless continuation frames to exhaust server resources.

### i) FrontJacking Attack
- **What:** Abuses front-end frameworks to hijack browser sessions or user actions.

---

## 4. Webserver Attack Methodology

```
1. Info Gathering (What server, what version, open ports)
2. Vulnerability Scanning (Look for misconfigurations, outdated software)
3. Exploitation (Try attacks: brute force, directory traversal, etc.)
4. Privilege Escalation (Gain higher access)
5. Covering Tracks (Delete logs, hide presence)
```

---

## 5. Terminologies

### WebDAV
- **Web Distributed Authoring and Versioning**
- Extension of HTTP that lets users edit and manage files on remote web servers.

### NTFS
- **New Technology File System**
- File system used by Windows, supports permissions, encryption, and large files.

---
