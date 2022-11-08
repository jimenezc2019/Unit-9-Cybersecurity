# Unit-9-Cybersecurity
# Pen Testing Live Targets

Time spent: **8** hours spent in total

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

Vulnerability #1: SQL Injection

Description: The user can perform an attack by adding a SQL injection to the end of the URL. I have shown in the gif that when adding ' OR SLEEP(5)=0--' to the end of the URL, the website shows a different staff member's profile. That indicates that it responded to the SQL that was added. 

<img src="http://g.recordit.co/edPaik41qW.gif">


Vulnerability #2: Session Hijacking

Description: The session ID is not regenerated for this website, even when the user agent string changes, it is vulnerable to session hijacking. I have shown in the gif that using the session ID from one browser to another you are able to gain access still.

<img src="http://g.recordit.co/HvgKjl34hh.gif">



## Green

Vulnerability #1: User Enumeration

Description: This vulnerability is on the Login page for the green website. The mistake the developer made was assigning a different class to failed login attempt message for valid usernames and invalid usernames. I have shown in the gif that when you type in an invalid username, the results show "unsuccessful" but unbolded and in the HTML "failed". Once I used "pperson" as the login, "unsuccessful" was bolded and the HTML showed "failure".

<img src="http://g.recordit.co/egcyJGqgwv.gif">


Vulnerability #2: Cross Site Scripting

Description: The user has the ability to execute an XSS attack by injecting JavaScript into the name input of the form.

<img src="http://g.recordit.co/Lerem83L37.gif">


## Red

Vulnerability #1: Insecure Direct Object Reference

Description: In the URL, each staff member's profile is identified by their ID. When you are in a salesperson profile, you can change the ID number to any other salesperson and it will pop up their profile. 

<img src="http://g.recordit.co/eGhzzCrKSY.gif">




