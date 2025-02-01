# Palo Alto Firewall
## Strategy
- Block the deployment of malware after the recon phase
- Block the exfil of data and interception of malicious commands
- Use SSL decryption
- Tune to the correct apps
- block bad certificates
- assign security profiles 
	- anti virus
		- use wildfire signatures
	- anti-spyware
	- vulnerability protection
	- file blocking
	- url filtering
- DOS zone protection can block scoring
- wildfire analysis security policy
	- It will state the malware that was installed
	- It does not block it immediately, but will eventually inform you with a report
- security policy needs a security profile
## Steps
- Change password
- Change management interface to permitted IP only
- No insecure services (no telnet, http, snmp)
- Nuke unnecessary admin users