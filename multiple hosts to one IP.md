up:[[unable to connect]]
# Multiple hosts to one IP
Because DNS is involved when translating the hostnames to the one IP address available on the server's side, this will prove to be an issue once the target is isolated, such as in our case. In order to solve this, we can edit our own local hosts file which includes correlations between hostnames and IP addresses to accommodate for the lack of a DNS server doing it on our behalf. Until then, we must first confirm that we are correct. In order to get a better view of the exact requests and responses being made and to confirm our suspicion, we will need to make use of a popular and easy to use tool called cURL . This tool will allow us to manipulate HTTP requests made to a server and receive the responses directly in the terminal, without the latter being interpreted by our browser as generic error messages such as in the example above.

To get a better Idea of what's going on, we use the [[curl]] -h command:

![[Pasted image 20240610092936.png]]

-v : Make the operation more talkative. More detailed output will be displayed during runtime.

``curl -v http://{target_IP}``


