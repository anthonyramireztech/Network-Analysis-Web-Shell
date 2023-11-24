# Network-Analysis-Web-Shell

	Gathered a PCAP file from a lab website called blueteamlabs to determine if the file contains malicious network activity about a "Local to Local Port Scanning" alert that a SOC Analyst sent me to investigate.
-	I opened my Windows 10 VM in VMWare to investigate the PCAP file within Wireshark. (Just for extra caution)
-	Gathering data we can use to trace this behavior, such as the IP responsible for conducting this internal scan. As well as what ports were scanned and what type of port scan was conducted.

	Investigation continues.
-	To get the first reconnaissance tool, I investigated the User Agent Strings, which leaves a signature of the tool it is originating from. Which led to the finding of twouser agents.
-	Then, I proceeded to find out what the web shell uploaded to the receiving host was.

	Results.
-	At the end of the network analysis, it was clear that malicious activity was occurring within the internal network between the two hosts. Analysis of the PCAP showed recon against the target IP of port scanning. The user agent contained suspicious files and command execution to create a reverse shell.
-	Reverse shell means: A host takes advantage of the target system's vulnerabilities to initiate a shell session and then accesses the victim's computer.
