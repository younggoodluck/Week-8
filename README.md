# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

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

Vulnerability #1:SQL Injection <a href="https://imgur.com/iiJ0Mu8"><img src="https://i.imgur.com/iiJ0Mu8.gif" title="source: imgur.com" /></a>
-[]Use the blind SQL injection, insert ’ OR SLEEP(5)=0--' to the position of id=“ ”, the page will propagate to load, which shows
the SQL works.


Vulnerability #2: Session Hijacking/Fixation  <a href="https://imgur.com/iAqB50k"><img src="https://i.imgur.com/iAqB50k.gif" title="source: imgur.com" /></a>
-I can log into red, then change to blue site


## Green

Vulnerability #1: Username Enumeration
https://i.imgur.com/gctNFbd.gif
-If the username doesn’t exist, the error message is not bold;if the username actually exists, the error message is bold.
Hacker can use this characteristic to try different username, and tell which is valid.

Vulnerability #2: Cross-Site Scripting <a href="https://imgur.com/toqKM7C"><img src="https://i.imgur.com/toqKM7C.gif" title="source: imgur.com" /></a>
-In feedback, leave a content of <script>alert('Mallory found the XSS!');</script>, when the administrator click to see this section,
the prompt shows up


## Red

Vulnerability #1:  Insecure Direct Object Reference <a href="https://imgur.com/rJwKI1G"><img src="https://i.imgur.com/rJwKI1G.gif" title="source: imgur.com" /></a>
-Get into one of the salesperson page, then change its id number to 10 in its url, one hidden user shows up.

Vulnerability #2: Cross-Site Request Forgery <a href="https://imgur.com/uVTs2bd"><img src="https://i.imgur.com/uVTs2bd.gif" title="source: imgur.com" /></a>
-Make a html in my local address, then put this in the content of feedback, of the administrator got interested and click the url,
one of the salesman`s information got changed.



## Notes

Describe any challenges encountered while doing the work

