# Honeypot Assignment

**Time spent:** **6** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

**Summary:** How did you deploy it? Did you use GCP, AWS, Azure, Vagrant, VirtualBox, etc.?

I Deployed it using GCP.

<img src="MHNadmindashboard.png">

### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?

Dionaea is trying to ultimately gain a copy of an attackers malware script. Once a copy of malware script is obtained a researcher can better understand what the
attacker is trying to exploit. 

<img src="honeypotdeployment.gif">

### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?

Mongo DB. The information exported to the JSON file record includes the protocol attacked/scanned, timestamp, source ip, source port, destination port, and an identifier. 

<img src="Database Backup.png">

*Be sure to upload session.json directly to this GitHub repo/branch in order to get full credit.*

## Notes

Describe any challenges encountered while doing the assignment.

The challeneges I encountered were at the end when I realized that I had done all of the steps before making the gif file.
