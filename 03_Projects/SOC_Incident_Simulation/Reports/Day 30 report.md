# Day 30 — SOC Analyst Final Simulation


## Incident Summary  

Simulated attack involving brute force login, malicious process, outbound connection, and persistence.

---

## Findings  

- Attacker IP: 192.168.56.102  
- Failed Logins: Multiple attempts  
- Successful Login: Yes  
- Suspicious Process: attack_sim.sh  
- Network Destination: example.com  
- Persistence: Cron job entry  

---

## Investigation  

- Detected failed logins via auth logs  
- Identified attacker IP  
- Found malicious process using ps aux  
- Verified network connection using ss -antp  
- Located persistence using crontab  

---

## Actions Taken  

- Removed cron job persistence  
- Killed malicious process using pkill  
- Blocked attacker IP via firewall  
- Terminated active session (who + pkill)  
- Changed user password  

---

## Verification  

- No malicious process running  
- No cron job present  
- No active suspicious connections  
- System stable  

---

## Conclusion  

Full attack chain successfully simulated and handled.  
System secured after proper response.

---

## Lessons Learned  

- Persistence must be removed before killing process  
- Active sessions must be terminated  
- Password reset is critical after compromise  
- Incident response must follow structured steps
