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
<img width="1570" height="1017" alt="image" src="https://github.com/user-attachments/assets/4d277a8e-7443-4335-9157-36d438e79ad6" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="1358" height="350" alt="image" src="https://github.com/user-attachments/assets/67275c15-3dbc-4ebd-8969-97c812364078" />

<img width="1112" height="507" alt="image" src="https://github.com/user-attachments/assets/fe1dc7a8-8ac1-4fa5-b0b7-0051569d60ce" />


**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="826" height="332" alt="image" src="https://github.com/user-attachments/assets/0d7df89b-8a06-4e88-919c-95a2accc929d" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="743" height="347" alt="image" src="https://github.com/user-attachments/assets/87ba188f-867c-4e90-8462-d42cdfc6b440" />


**6. Send the generated link to the victim.**
<img width="1920" height="1051" alt="Bharath6384_creating-a-backdoor-with-SET_ Ethical Hacking Lab EX-07 - Google Chrome 27-09-2025 09_34_52" src="https://github.com/user-attachments/assets/7da000b0-958a-4a92-8d55-d38942b3a0b7" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="542" height="141" alt="image" src="https://github.com/user-attachments/assets/f6bf61fa-3361-454a-a7c1-42ff9963ca68" />




## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
