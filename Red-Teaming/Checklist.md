
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
	2. Find API parameters (automated tool)
	3. Check for default or common credentials


- Exploitation CheatSheet:
    1. Search for  `<software> <version> <exploit> GitHub`   or look for writeups or blog posts.
	    1. Look through repos and issues, for credentials, subdomains, sensitive files.
    2. Look at and understand the exploit. Are modifications needed?
	    2. Can Google Dork for S3 buckets, exact matches.
	3. Use Ffuf or Burp intruder to mass-test payloads
		1. Seclists payloads (SSTI/LFI/Path Traversal)






