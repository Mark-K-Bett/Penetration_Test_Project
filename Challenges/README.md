Challenge 4: Analyze a PCAP File to Find Information

1️⃣ Objective

In this challenge, we analyzed a PCAP (Packet Capture) file to extract valuable information about a target computer, including its IP address, directories, and a file containing the challenge code. However, due to the server being down, we were unable to access the target directly via a web browser.

2️⃣ Tools Used 🛠️

Wireshark (Used to analyze network traffic in the PCAP file)


3️⃣ Steps Taken 🔍

Step 1: Analyze the SA.pcap File

Open Wireshark and load the file:

wireshark /home/kali/OTHER/SA.pcap

Apply a filter to analyze HTTP traffic:

http.request

Identify the IP address of the target computer and note any revealed directories.

Findings:

Target IP Address: 10.6.6.14

Revealed Directories: /data/, /logs/, /backup/

Step 2: Attempt to Access the Target

Use a web browser to check the revealed directories:

http://10.6.6.14/data/

The goal was to access the accounts.xml file at:

http://10.6.6.14/data/accounts.xml

Issue Encountered: ❌ The server was down, preventing access.

Tried curl as an alternative:

curl -v http://10.6.6.14/data/accounts.xml

Result: Connection failed due to the server being unavailable.

