# Day 29 — Incident Response Simulation


## Incident Summary  
Multiple failed login attempts detected along with suspicious system activity.

---

## Findings  

- Attacker IP: 192.168.56.102  
- Activity: Multiple failed SSH login attempts  
- Suspicious Process: Detected running in system  
- Network Activity: External connection observed  
- Persistence: Cron job entry found  

---

## Investigation  

- Checked logs using: grep "Failed password" /var/log/auth.log  
- Identified attacker IP from logs  
- Analyzed processes using: ps aux  
- Checked network connections using: ss -antp  
- Verified persistence using: crontab -l  

---

## Actions Taken  

- Killed suspicious process  
- Removed malicious cron job  
- Blocked attacker IP using firewall  

---

## Verification  

- No suspicious processes running  
- No cron persistence found  
- No active malicious connections  

---

## Conclusion  

Incident successfully detected and contained.  
Attack involved brute force attempt with persistence mechanism.

---

## Lessons Learned  

- Importance of checking logs first  
- Persistence mechanisms must be verified  
- Quick containment prevents further compromise
