
## OSINT

- OSINT CheatSheet:
    1. GitHub Dorking
	    1. Look through repos and issues, for credentials, subdomains, sensitive files.
    2. Google Dorking
	    1. Can Google dork for S3 buckets, exact matches.
    3. LinkedIn
	    1. Leaking tech stack, finding social engineering targets


- Scanning CheatSheet:
    1. Nmap
	    1. Look through repos and issues, for credentials, subdomains, sensitive files.
    2. Nuclei
	    2. Can Google dork for S3 buckets, exact matches.
    3. Directory Busting
	    3. Leaking tech stack, finding social engineering targets
	4. Burp Scanner
		1. Install extensions 

- Enumeration CheatSheet:
    1. Directory Busting 
	    3. Fuzz for extensions
	    4. Use short wordlist (dirb common.txt) then long (raft)
	    5. You can directory bust within directories, even if you don't have read permissions. 
	    6. If you need authentication, you can dirsearch with headers.
	2. Find API parameters (automated tool)
	3. Check for default or common credentials


- Exploitation CheatSheet:
    1. Search for  `<software> <version> <exploit> GitHub`   or look for writeups or blog posts.
	    1. Look through repos and issues, for credentials, subdomains, sensitive files.
    2. Look at and understand the exploit. Are modifications needed?
	    2. Can Google Dork for S3 buckets, exact matches.
	3. Use Ffuf or Burp intruder to mass-test payloads
		1. Seclists payloads (SSTI/LFI/Path Traversal)
	4. What looks weird? Are there directories that look odd?


Linux Post-Exploitation CheatSheet:
    1. What looks out of place or weird? 
	    1. Unusual directories, files, activities, both in user and root directories.
    2. PSPY to monitor for running stuff.
	    2. Can Google Dork for S3 buckets, exact matches.
	3. Lazagne, Mimikatz to dump credentials
	4. CronJobs (would be seen by PSPY)


Windows Post-Exploitation CheatSheet
    1. What looks out of place or weird? 
	    1. Unusual directories, files, activities, both in user and root directories.
    2. PSPY to monitor for running stuff.
	    2. Can Google Dork for S3 buckets, exact matches.
	3. Lazagne, Mimikatz to dump credentials
	4. BloodHound 
	5. 


Persistence Post-Exploitation CheatSheet
    1. Autoruns, Cronjobs, Scheduled Tasks
	    1. You can have these reference other persistence mechanisms (ie have a Cronjob that sets up a service backdoor in addition to being its own backdoor)
    2. Consider using password bind shells
	    1. Multiple people can use these 
	3. Have persistence mechanisms reference each other, and enable each other
	4. 




