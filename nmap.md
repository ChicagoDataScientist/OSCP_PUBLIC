up:[[Hacking Process]]
up:[[Port Scanning with Nmap]]
#nmap
# NMAP
![[Pasted image 20250228205224.png]]
![[Pasted image 20250228205309.png]]


- sudo nmap -sC -sV 
- sudo nmap -sC -sV -V
- ### Ryan John likes: nmap -A -F -T1 10.10.10 -v (for beginners)
- 

-sC: Performs a script scan using the default set of scripts. It is equivalent to -- script=default. -sV: Version detection 
-v: Increases the verbosity level, causing Nmap to print more information about the scan in progress.

## [[open ports]]

