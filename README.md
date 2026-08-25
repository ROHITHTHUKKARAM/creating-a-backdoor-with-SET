# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="955" height="1079" alt="Screenshot 2026-08-25 141039" src="https://github.com/user-attachments/assets/0a2e9730-ee82-4988-9bbf-d6f7d9b6385d" />



**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="958" height="1079" alt="Screenshot 2026-08-25 134048" src="https://github.com/user-attachments/assets/67fbc883-de1e-4c07-927e-51f8e2d92dea" />
<img width="956" height="1079" alt="Screenshot 2026-08-25 134201" src="https://github.com/user-attachments/assets/cc67da71-4886-4cc9-9fad-abf164194388" />
<img width="958" height="1079" alt="Screenshot 2026-08-25 134308" src="https://github.com/user-attachments/assets/c4379a3a-7055-4fbc-b288-86e9a7049f8a" />


**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="959" height="1079" alt="Screenshot 2026-08-25 134443" src="https://github.com/user-attachments/assets/74e76cdc-9424-47cb-b539-23658b6b223b" />


**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="958" height="1079" alt="Screenshot 2026-08-25 141425" src="https://github.com/user-attachments/assets/75879666-0547-4a5e-a844-89544a029f20" />




**6. Send the generated link to the victim.**
<img width="957" height="1079" alt="Screenshot 2026-08-25 140359" src="https://github.com/user-attachments/assets/c8c80540-774b-4310-94da-a132c47cd742" />




**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="958" height="1079" alt="Screenshot 2026-08-25 140422" src="https://github.com/user-attachments/assets/63f10f00-bfd6-466c-9d5e-1aa6d15bd92a" />





## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
