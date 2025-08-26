# OWASP Top 10 Web Application Attacks
---

## 1. Directory Traversal Attack (`../`) 
Imagine you’re in a hotel and you’re only supposed to access your own room. But you find a way to sneak into the manager’s office by walking through unlocked doors.  
**In Web:**  
A hacker tricks a website into letting them access secret files on the server by using special paths like `../../secret.txt`.

---

## 2. RC4 Nomore Attack
You’re using a lock that everyone once thought was safe, but now thieves have learned an easy trick to open it.  
**In Web:**  
RC4 was a popular way to scramble data, but attackers found weaknesses, so it’s no longer safe to use.

---

## 3. LDAP Injection Attack  
You call a company and the receptionist asks, “Who do you want to speak with?” If you say something clever, you trick the receptionist into giving you a list of all employees instead.  
**In Web:**  
Hackers inject special characters into search boxes to trick the website into revealing or changing sensitive information stored in directories (like address books).

---

## 4. SQL Injection 
You’re at a restaurant and instead of ordering food, you shout, “Give me the keys to the cash register!”  
**In Web:**  
Hackers type sneaky commands into input fields to make the website share, change, or delete data from its database.

---

## 5. Cross Site Scripting (XSS) vs. CSRF Attack

### Cross Site Scripting (XSS) 
You write a sneaky note and trick someone into reading it aloud, causing trouble for them.  
**In Web:**  
Attackers inject harmful scripts into websites so that when other users visit, their browsers run the attacker’s code.

### Cross Site Request Forgery (CSRF)
You trick someone into sending a letter on your behalf without them knowing what’s inside.  
**In Web:**  
Attackers trick logged-in users into performing actions they didn’t intend (like changing their password) by making their browser send requests without their consent.

---

## 6. XML External Entity Attack (XXE)
You mail a form to a company, but you secretly include a note asking them to send you their private files.  
**In Web:**  
Attackers send special XML data to a website, tricking it into giving up files or secret information.

---

## 7. Magecart Attack
Hackers sneak a credit card skimmer into a shop’s checkout counter to steal your card info.  
**In Web:**  
Hackers inject malicious code into e-commerce sites to capture customers' credit card details during checkout.

---

## 8. SSRF Payload (Server Side Request Forgery)
You ask a librarian to fetch a book from a locked staff room for you when you shouldn’t have access.  
**In Web:**  
Attackers trick a server into fetching or interacting with resources it shouldn’t have access to, sometimes leaking sensitive data.

---

## 9. H2C Smuggling Attack
You send a message in a secret language the guards don’t understand, smuggling forbidden items past them.  
**In Web:**  
Attackers exploit differences in how web servers handle certain HTTP message formats (like HTTP/2 to HTTP/1.1 downgrades), sneaking malicious requests past security checks.

---

## 10. MarioNet Attack
Someone secretly puts a remote control in your toy, and later they can make it do whatever they want—even when you’re not looking.  
**In Web:**  
Hackers run hidden scripts in your browser, turning your computer into a “zombie” that can be controlled remotely for attacks or mining cryptocurrency.

---
# Various Terminologies
**Shell Injection**  
Shell Injection lets hackers trick your program into running harmful commands by sneaking them into input.
Functions like system(), startprocess(), Runtime.exec(), and Process.start() can be dangerous if you use user input without checks.
Always validate input and use safer alternatives when possible.

---
**CRLF injection Attack**  

Imagine you’re writing a letter, and you end each line by pressing “Enter” (that’s a line break). Computers use special characters for this: CR (Carriage Return, \r) and LF (Line Feed, \n). Together, they make a new line: CRLF.

---
## XML
XML (eXtensible Markup Language) is a way for computers to store and share data using special tags (like <name>John</name>). It’s designed to be readable by both humans and machines.
**WSDL, UDDI, and SOAP**  
**SOAP (Simple Object Access Protocol)**
A protocol (set of rules) for sending messages between computers over the Internet, using XML.Used for Sending requests and getting responses between web services.

**WSDL (Web Services Description Language)**
An XML file that describes what a web service can do, how to talk to it, and where it lives.Tells computers how to interact with a web service.


**UDDI (Universal Description, Discovery, and Integration)**
A big, searchable phonebook for web services, describing what they do, where to find them, and how to use them.Finding and registering web services.

---
## Websockets

a way for your computer (like a web browser) and a server to talk to each other in real time, like a phone call, instead of sending letters back and forth.
Used for:Live chat apps (like WhatsApp Web)
Online games
Real-time dashboards

---
## CORS (Cross-Origin Resource Sharing)

CORS is the browser’s way of checking if it’s safe to get data from other websites.

---
## SAML-based SSO
SAML-based SSO stands for “Security Assertion Markup Language – Single Sign-On.”
Log in once (at the trusted “security office”)
Access many websites or apps without logging in again
The websites trust the “pass” you got from the security office

---
## LFI (Local File Inclusion) 
LFI (Local File Inclusion) is a web security vulnerability that allows an attacker to trick a web application into including files on the server. This can lead to the attacker viewing sensitive files, executing code, or even taking full control of the server under some conditions.

---
## Webhooks 
Webhooks are automatic messages sent from one app to another when something happens.

---
## RBAC stands for Role-Based Access Control.
It’s a way for organizations to control who can do what in a system by assigning “roles” (like Admin, Editor, Viewer) to users.
Each role has specific permissions.

---
## No (Attribute-Based Access Control) ABAC Validation
The system doesn’t check “who, what, when, where, or why” before letting someone do something.

---
## WebFinger
WebFinger lets you find public info about someone using an email-like address.
In CEHV13, you “get” this info by sending a GET request to the right URL and reading the JSON response.

---
## IDOR Insecure Direct Object Reference.
IDOR means users can access things just by changing IDs, without checks.
