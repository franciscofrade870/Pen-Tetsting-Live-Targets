# Pen Testing Live Targets

Time spent: **X** hours spent in total

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

Description:
In ` 104.198.208.81 ` has a tab called ` Find a Salesperson `. Once thing I noticed was at the very bottom it shows a SQLi test. Putting the basic SQL injection for admin ( ` 'OR 1=1' `) in the URL with a random Salesperson it redirected me saying ` Database query failed. `. This tells me that the ` Find a Salesperson ` page is not  properly sanitizing queries. So adding the double hyphen ` -- ` into the attack turns it to a comment which takes me to the admin account; or in this case `id=1`. 

<img src="SQL.gif">


Vulnerability #2: Session Hijacking

Description:
Looking into users via ` pperson ` credentials I notice that the PHP sessions were vulnerable thorugh burp. Using the  `change PHP session ` tool I was able to change the ` index.php ` PHPSESSID from ` ocppafsrts0fdj5mq7d50uloi3 ` to ` Hellothere `. This can be a problem because if a threatactor see's that the session is susceptible for a hijacking attack then the user is vulnerable. 

<img src=".gif">


## Green

Vulnerability #1: __________________

Description:

<img src=".gif">


Vulnerability #2: __________________

Description:

<img src=".gif">

## Red

Vulnerability #1: __________________

Description:

<img src=".gif">


Vulnerability #2: __________________

Description:

<img src=".gif">

## Notes

Describe any challenges encountered while doing the work
