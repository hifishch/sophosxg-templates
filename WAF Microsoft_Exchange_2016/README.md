# WAF Template for Microsoft Exchange 2016 or newer
This Rule creates following Objects in your Sophos Firewall:
* IP Adress Object named "WS EXCHANGE" with IP "172.20.20.20"
* Webserver Named "WS EXCHANGE" Pointing to the IP Adressobject "WS EXCHANGE"
* Two Protection Policies named "Microsoft Exchange 2016 Webservices" and "Microsoft Exchange 2016 Autodiscover"
* WAF-Firewall-Rule named "WAF owa.example.com" Referencing to Webserver Named "WS EXCHANGE" using the Protection Policy "Microsoft Exchange 2016 Webservices"
* WAF-Firewall-Rule named "WAF autodiscover.example.com" Referencing to Webserver Named "WS EXCHANGE" using the Protection Policy "Microsoft Exchange 2016 Autodiscover"
* Firewal-Rule Group "WAF Rules" containing those two WAF-Firewall-Rules.

## Some Assembly Required: This file needs to be modifyed before it is ready to be imported.
Please Note that you need to make the exported File to a TAR-Ball before uploading to your Sophos Appliance.
### Suggested Workflow:
1. Search & Replace "example.com Wildcard" with the Name for your Wildcard Certificate
2. Search & Replace "owa.example.com" with your OWA-Domain
3. Search & Replace "autodiscover.example.com" with your Autodiscover-Domain
4. Search & Replace "172.20.20.20" with your Exchange-Servers internal IP.
5. Create TAR-Ball and Import it to your Sophos Appliance
6. Change other Details (EG Public IP etc.) in the WebGUI of your Appliance.
