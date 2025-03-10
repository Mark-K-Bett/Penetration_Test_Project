# Challenge 1: SQL Injection (DVWA) 🚀  

## **1⃣ Objective**  
In this challenge, we exploited an **SQL Injection** vulnerability in **DVWA (Damn Vulnerable Web Application)** to:  
✅ Retrieve user credentials from the database.  
✅ Crack Gordon Brown’s password using **CrackStation.net**.  
✅ Use the credentials to SSH into `172.17.0.2` and retrieve the flag file.  

---

## **2⃣ Tools Used 🛠️**  
- **DVWA** (Damn Vulnerable Web Application)  
- **CrackStation.net** (Online hash cracker)  
- **Kali Linux** (Penetration testing)  
- **SSH** (Remote login)  

---

## **3⃣ Steps Taken 🔍**  

### **Step 1: Access DVWA and Set Security Level**
1. Open a browser and navigate to `http://10.6.6.100/dvwa/`.  
2. Log in   

### **Step 2: Identify SQL Injection Vulnerability**
1. Navigate to **DVWA → SQL Injection**.  
2. In the input field for `User ID`, test basic SQL injection:  
   ```sql
   ' OR 1=1 --  
   ```
3. If the database is vulnerable, it should return all user details.  

✅ Successfully extracted **Gordon Brown’s** password hash.  

📸 **Screenshots:** [Located in `screenshots/`](screenshots/)  

---

### **Step 3: Crack Gordon Brown's Password**
1. Copy the extracted hash.  
2. Use **CrackStation.net** to crack the password:  
   - CrackStation (Online):  
     - Go to [CrackStation.net](https://crackstation.net)  
     - Paste the hash and decrypt it.  

📸 **Screenshots:** [Located in `screenshots/`](screenshots/)  

---

### **Step 4: Locate and Open the Flag File**
1. SSH into `172.17.0.2` using Gordon Brown's credentials:  
   
2. Navigate to the **home directory**:  
  
3. Locate the **flag file**:  
   
4. Open the flag file to view the contents:  
   `
✅ Successfully retrieved the **flag!**  

📸 **Screenshots:** [Located in `screenshots/`](screenshots/)  

---

## **📚 Project Structure**
```
Challenge-1-SQL-Injection/
│── README.md                 # This documentation file  
│── exploit.sql               # SQL injection queries used  
│── cracked-password.txt      # Extracted hash and cracked password  
│── screenshots/              # Folder containing proof screenshots  
│   │── dvwa-login.png  
│   │── sqlmap-results.png  
│   │── crackstation-results.png  
│   │── flag-file.png  
```

---

## **🛡️ Remediation & Security Recommendations**
To prevent SQL Injection attacks:  
✅ **Use Prepared Statements & Parameterized Queries**  
✅ **Sanitize & Validate User Input**  
✅ **Apply Least Privilege Principle**  
✅ **Use Web Application Firewalls (WAF)**  
✅ **Regularly Update & Patch Software**  

---

## **📝 Conclusion**
This challenge demonstrated how **SQL Injection** can be exploited to extract user credentials, crack passwords, and gain unauthorized access to sensitive files. Organizations should implement best practices to mitigate such risks.  


