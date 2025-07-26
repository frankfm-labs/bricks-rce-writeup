# Bricks Heist THM Walkthrough — CVE-2024-25600 & More

![Proof it works](rce.png)

---

## What I did

- Created a **custom Python exploit** for Bricks Builder RCE (exploit code in private repo)  
- Extracted the nonce from the homepage JavaScript  
- Sent PHP wrapped in an Exception to get command output  
- Obtained shell access, created reverse shell and found a hidden `.txt` flag  
- Identified suspicious process `nm-inet-dialog` and related service `ubuntu.service`  
- Located miner config file `inet.conf` and extracted the wallet address  
- Used OSINT to link wallet to a known threat group

---

## How I did it

- Developed a Python script targeting the vulnerable REST API endpoint  
- Launched a stabilized Reverse Shell  
- Explored running processes, systemd services, and log files  
- Analyzed miner config and gathered intelligence  
- Collected all flags and relevant data

---

## Challenges & Lessons

- Figuring out the exact service and hidden files took digging  
- Mining address was weird encoded, had to decode with [CyberChef](https://gchq.github.io/CyberChef/)

---

## Useful links

- [TryHackMe Profile](https://tryhackme.com/p/frankfm)  
- [Bricks Heist Room](https://tryhackme.com/room/tryhack3mbricksheist)
