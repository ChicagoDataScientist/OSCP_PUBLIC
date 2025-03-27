up:[[Active Information Gathering]]
up: [[Network Mapping]]
[[Host Discovery Techniques]]
#nmap #hostdiscovery
# Host Discovery with Nmap

to get my IP address:
```
ip a s
```

![[Pasted image 20250228112418.png]]

Do a scan without doing a full port scan. This lets you know what hosts are on the network:

```
sudo nmap -sn 192.168.0.12/24
```

![[Pasted image 20250228120338.png]]

## netdiscover
sends ARP requests... is resolves mac addresses to IP addresses

```
sudo netdiscover -i eth0 -r 192.168.0.12/24
```

![[Pasted image 20250228121402.png]]



