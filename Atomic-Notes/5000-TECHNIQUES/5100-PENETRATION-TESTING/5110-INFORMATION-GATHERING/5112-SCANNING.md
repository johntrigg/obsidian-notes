Scanning is the use of utilizing tools and/or techniques to reveal information about a target. Some incredibly important tools for this include [[notes/Atomic-Notes/4000-TOOLS/4100-OFFENSIVE-TOOLS/4110-NMAP/4111-NMAP]], [[notes/Atomic-Notes/4000-TOOLS/4100-OFFENSIVE-TOOLS/4120-NUCLEI/4121-NUCLEI]]

## USEFUL COMMANDS
```bash
# Against every target in urls.txt, run everything in the directory ./nuclei-templates
nuclei -l urls.txt -t nuclei-templates

# Same as above, but use targets.txt as an input list
nmap -sC -sV -p- -il targets.txt --min-rate 10000
```
