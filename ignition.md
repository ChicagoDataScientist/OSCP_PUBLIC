up:[[Machine Writeups]]
# Ignition Machine
First, I began with an Nmap scan:


![[Pasted image 20240610091550.png]]

I tried visiting the site [Site Unreachable](http://ignition.htb/)
![[Pasted image 20240610091932.png]]
I saw that there was an error in the redirect to http://ignition.htb/

After a quick Google search of the error, we learn that there might be two underlying reasons to this error appearing. 
- We've mistyped the ignition.htb address in our URL search bar, and the DNS servers can't find the associated IP address for the mistyped name. 
- We never entered any hostname such as ignition.htb into the search bar, but the website expects us to.

In short, multiple websites can share the same IP address, allowing users to access them separately by visiting the specific hostnames of each website instead of the hosting server's IP address. The webserver we are making requests to is throwing us an error because we haven't specified a certain hostname out of the ones that could be hosted on that same target IP address. From here, we'd think that simply inputting ignition.htb instead of the target IP address into the search bar would solve our issue, but unfortunately, this is not the case. When entering a hostname instead of an IP address as the request's destination, there is a middleman involved that you might not know about.

To get more info, I typed:
``curl -v http://{target_IP}``

![[Pasted image 20240610093636.png]]

After fixing the host, I was able to resolve to the ignition.htb website:

![[Pasted image 20240610104142.png]]

I looked around and did not see anything useful, so I decided to enumerate the site with gobuster:

(gobuster screenshot)
![[Pasted image 20240610122134.png]]


I found the /admin directory.  The magneto documentation says that there are safeguards against brute force, so I decided to try 2024 most common passwords that meet the #magneto requirement of seven characters, plus number and letter combinations.

![[Pasted image 20240610120452.png]]

I found the successful combo!
```
admin:qwerty123
```

I found the flag:
```
797d6c988d9dc5865e010b9410f247e0
```

