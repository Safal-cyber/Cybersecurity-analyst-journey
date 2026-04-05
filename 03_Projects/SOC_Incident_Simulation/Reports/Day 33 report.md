# Day 33 — Splunk Incident Investigation


## Incident Summary  

Multiple failed login attempts detected from a single IP over multiple days, followed by a successful login.

---

## Findings  

- Attacker IP: 192.168.56.102  
- Total Failed Attempts: 61  
- Successful Login: Yes  
- Attack Pattern: Repeated + burst  
- Peak Activity: 3 April (42 attempts)  
- Time Range: 29 March – 4 April  

---

## Investigation  

- Queried logs using: "Failed password"  
- Extracted IP using rex  
- Counted attempts using stats count by ip  
- Identified attacker using top ip  
- Analyzed timeline using timechart  

---

## Actions Taken  

- Identified brute force pattern  
- Flagged successful login as compromise indicator  
- Recommended blocking attacker IP  

---

## Verification  

- Pattern confirmed via log correlation  
- No false positive indicators observed  

---

## Conclusion  

Confirmed brute force attack with successful compromise attempt.  
Risk Level: High  

---

## Lessons Learned  

- Time-based analysis reveals attack patterns  
- Repeated failures indicate brute force  
- Successful login after failures is critical alert
