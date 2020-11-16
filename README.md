# Project 8 - Pentesting Live Targets

Time spent: **4** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: SQL Injection (SQLi)

Description: using `' or sleep(0)=0--'` the sql statement queries the dbms and brings up user DBurke. 

<img src="SQL Injection - Blue.gif">

Vulnerability #2: Session Hijacking/Fixation

Description:By logging into another website with credentials I am able to copy the session id from green to blue and login to blue website without entering credentials. You are able to change the session ids with hacktools. 

<img src="Session Hijacking - Blue.gif">

## Green

Vulnerability #1: User Enumeration

Description:When entering a correct username the log in was unsuccessful message is in bold. When the username is incorrect the message in not bolded. 

<img src="User Enumaration - Green.gif">

Vulnerability #2: XSS

Description:By inserting a xss script `<script>alert(‘Luke found the XSS!');</script>` the script is activated upon loading in the green website on the feedback page. 

<img src="XSS - Green.gif">


## Red

Vulnerability #1: CSRF

Description:You are able to make changes to user info with an improper session id. 

<img src="CSRF - Red.gif">

Vulnerability #2: URL Manipulation/IDOR

Description:By changing ID number in the URL you can bring up users who are supposed to be hidden.

<img src="URL Manipulation - Red.gif">


## Notes

Describe any challenges encountered while doing the work
