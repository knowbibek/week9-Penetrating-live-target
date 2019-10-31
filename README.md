# week9-Penetrating-live-test
# Project 8 - Pentesting Live Targets

Time spent: **7** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

### Vulnerability #1: SQLI
* The user can inject SQL code into the website by changing userID to 
```
OR SLEEP(5)=0--'
```
* That make the website to slow down, the greater the value inside SLEEP, it will slow more.

#### gif goes here SQLI
Vulnerability #2: Session HighJacking

* In the blue site, One can get into the system by highjacking the session ID
* Burp suite was used.
* One can modify the session and get into the victimaccount through this.
* Traffic is intercepted and new session ID is entered to get access


## Green
### Username Enumeration

Vulnerability #1:: Username Enumeration
* The login page show the bold " Login was Unsuccessful" when entered the username which is in the database
* Otherwise it will be normal which make the person to find out the user which exist in the system

Vulnerability #2: 4. Indirect Object Refrence 
* By change the id value on the webaddress, one can view the info of the staff which is not displayed normally
```
https://104.198.208.81/green/public/staff/users/edit.php?id=2 
```

## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)

* One can access the information of salesman who is not in the list by setting ID to 10 or 11

### gif

Vulnerability #2: Cross-Site Request Forgery (CSRF)

* The user has permissions to update info in the site with the csrf token.
* The red one also act as the blue page which dont allow the user to edit without the valid token.


## Notes
Yeah, it really have to work really hard but at the end it was good feeling.
