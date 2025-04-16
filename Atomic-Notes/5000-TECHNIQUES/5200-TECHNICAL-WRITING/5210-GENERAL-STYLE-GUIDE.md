There are a lot of considerations that should be made. Below are a collection of the best practices/ways of doing things that I like the most, broken down by section.



## Vulnerability Reporting
What language does the client want? Do they want the word "Weakness", "Technical Vulnerability", or something else entirely?

Density vs practicality. There's a lot of fields you could include. Honestly, most are useless and only make the report look better. I personally like the design of having a table with the shorthand information, and going into detail below.

## Potential Information Fields
- Ordered:
    1. CVSS Score, Severity, and String
    2. NIST Mappings
    3. MITRE ATT&CK Mappings
    4. Remediation Difficulty
    5. Title
    6. Affected Systems
    7. 

## Document Ordering
Do you want a table of contents? You do. How do you want to label vulnerabilities? I personally like

- Vulnerabilities
    1. Critical
	    1. C001 - Domain Administrator Null Session
	2. High 
		1. H001 - Apache Shellshock Remote Code Execution



## Document Styling
Always spell out acronyms