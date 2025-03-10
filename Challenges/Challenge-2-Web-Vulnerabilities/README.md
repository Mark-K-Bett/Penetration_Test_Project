Challenge 2: Web Server Vulnerabilities 🌍🚀

1️⃣ Objective

In this challenge, we discovered vulnerable directories due to improper web server configurations and retrieved the flag file.

2️⃣ Tools Used 🛠️

DVWA (Damn Vulnerable Web Application for security testing)

Nikto (Web server vulnerability scanner used for reconnaissance)

3️⃣ Steps Taken 🔍

Step 1: Access the Web Server

Open a browser and navigate to http://10.6.6.100/dvwa/.

In the DVWA browser, set DVWA Security to low.

Step 2: Perform Reconnaissance

Use Nikto to scan the web server and identify directories where indexing is enabled:

nikto -h 10.6.6.100

Identify the directory /docs as a vulnerable directory.

Step 3: Locate the Flag File

Enter http://10.6.6.100/docs in the browser.

Locate and open user_form.html to reveal the flag value.

