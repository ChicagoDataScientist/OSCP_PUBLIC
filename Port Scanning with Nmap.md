up:[[Active Information Gathering]]
up[[Network Mapping]]
[[nmap]]
#nmap 
# Port Scanning with Nmap

ping the website name to get the ip address:
```
ping target.ine.local
```

![[Pasted image 20250228123438.png]]

ip address is 192.103.255.3

do a basic nmap scan (scans most common 1000 ports)
```
nmap 10.4.19.218
```

![[Pasted image 20250228164041.png]]

host is blocking out scan, so we try:
```
nmap -Pn 10.4.19.218
```

![[Pasted image 20250228164241.png]]

if we want to scan ALL ports:

```
nmap -Pn -p- 10.4.19.218
```

or specific ports:

```
nmap -Pn p80,445,3389  10.4.19.218
```
![[Pasted image 20250228164627.png]]

or we can acan a range of ports
```
nmap -Pn p1-1000  10.4.19.218
```

![[Pasted image 20250228164818.png]]

Fast Scan:
```
nmap -Pn -F  10.4.19.218
```

![[Pasted image 20250228165024.png]]

To do a UDP scan. THis may take a long time.....

```
nmap -Pn -sU  10.4.19.218
```
 (waiting......)
 ![[Pasted image 20250228165239.png]]

after all that, all UDP ports found open|filtered:

![[Pasted image 20250228165340.png]]



To do a fast scan:

```
nmap -Pn -F 10.4.19.218
```

![[Pasted image 20250228165809.png]]

 sV lets us get a service version:

```
nmap -Pn -F -sV 10.4.19.218
```


![[Pasted image 20250228165948.png]]


now we try -O to try to see what OS is running and we add -v VERBOSE

```
nmap -Pn -F -sV -O 10.4.19.218 -v
```

![[Pasted image 20250228183939.png]]


It shows verbose services running

![[Pasted image 20250228184105.png]]

![[Pasted image 20250228184139.png]]

next, we add an nmap script scan to run special nmap scripts to see if it can discover more

```
nmap -Pn -F -sV -O -sC 10.4.19.218 -v
```
![[Pasted image 20250228184805.png]]![[Pasted image 20250228184844.png]]

it gives us a lot more info from the scripts, for example http-favicon script

![[Pasted image 20250228184947.png]]
Nmap aggressive scan:
it replaces -sV -O -sC with one flag instead which is -A
```
#these are the same
nmap -Pn -F -sV -O -sC 10.4.19.218 -v
nmap -Pn -F -A 10.4.19.218 -v
```

Change speed. nmap scans are sped from T1 - T5. the lower the number, the slower the scan.

```
nmap -Pn -F -T5 -sV -O -sC 10.4.19.218 -v
```

![[Pasted image 20250228185711.png]]

You can output into another file with -oN example.txt
```
nmap -Pn -F 10.4.19.218 -oN test.txt
```

now if you type
```
cat test.txt
```

you will see the same results in the file:
![[Pasted image 20250228190352.png]]
 or you can make an XML file
 ```
 nmap -Pn -F 10.4.19.218 -oX test.xml
```

so now if we type:

```
cat test.xml
```

we get the contents of the xml file:

![[Pasted image 20250228190810.png]]

