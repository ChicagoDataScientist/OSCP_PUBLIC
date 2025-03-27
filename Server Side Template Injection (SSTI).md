up:[[Template Engines]]

# SSTI
Server-side template injection is a vulnerability where the attacker injects malicious input into a template in order to execute commands on the server. 

To put it plainly an SSTI is an exploitation technique where the attacker injects native (to the Template Engine) code into a web page. The code is then run via the Template Engine and the attacker gains code execution on the affected server. 

This attack is very common on Node.js websites and there is a good possibility that a Template Engine is being used to reflect the email that the user inputs in the contact field.

## Identification
In order to exploit a potential SSTI vulnerability we will need to first confirm its existence. After researching for common SSTI payloads on Google, we find this [Hacktricks](https://book.hacktricks.xyz/pentesting-web/ssti-server-side-template-injection)article that showcases exploitation techniques for various different template engines. The following image shows how to identify if an SSTI vulnerability exists and how to find out which Template engine is being used. Once the engine is identified a more specific payload can be crafted to allow for remote code execution.

