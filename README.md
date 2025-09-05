 Cowrie Honeypot Project

This project documents the setup and use of Cowrie, a medium-interaction SSH and Telnet honeypot.  
The goal is to capture and analyze attacker behavior in a safe environment, while gaining hands-on experience with cybersecurity monitoring and attack simulation.


What is Cowrie?
Cowrie is a honeypot designed to emulate an SSH/Telnet server.  
It provides a fake filesystem and shell, records all login attempts, executed commands, and even file downloads/uploads, without ever exposing the real system.


Project Overview
This project includes:
- Installing and configuring Cowrie in a Python virtual environment  
- Editing the `cowrie.cfg` configuration file  
- Starting, stopping, and monitoring the honeypot  
- Running brute-force attacks using Hydra  with the `rockyou.txt` wordlist  
- Capturing and analyzing attacker logs  
- Testing reverse shell interactions with Netcat  


 Key Features
- Logs all authentication attempts (usernames & passwords)  
- Records attacker commands and file transfer attempts  
- Provides a fake Linux-like filesystem  
- Supports integration with ELK Stack for log visualization  


Installation Steps (Summary)
1. Update and upgrade the system  
2. Install dependencies (`git`, `python3-venv`, `pip`, `libssl-dev`, `libffi-dev`, `build-essential`)  
3. Clone Cowrie into `/opt/cowrie`  
4. Create a Python virtual environment and install requirements  
5. Configure `cowrie.cfg`  
6. Start Cowrie with `bin/cowrie start`  


Attack Simulations
- Brute-force attacks on SSH and Telnet using Hydra  
- Use of the rockyou.txt  password list  
- Capturing both successful and failed login attempts  
- Reverse shell test using Netcat, fully logged by Cowrie  


Analysis & Findings
- Most attacks targeted the `root` account with common weak passwords  
- Cowrie successfully captured all login attempts and commands  
- Even failed brute-force attempts provided valuable log data  
- Reverse shell attempts were recorded without compromising the system  


Conclusion
  This project provided hands-on experience with:
- Honeypot deployment and monitoring  
- Understanding attacker behavior and brute-force techniques  
- Safe log collection and analysis for cybersecurity research  

Future improvements could include integrating Cowrie with ELK or Splunk dashboards and automating log analysis using Python scripts.


 References
- [Cowrie GitHub Repository](https://github.com/cowrie/cowrie)  
- [Hydra Tool Documentation](https://github.com/vanhauser-thc/thc-hydra)  
- [rockyou.txt Wordlist](https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt)  
