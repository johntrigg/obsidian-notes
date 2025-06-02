Nuclei is a free and open-source vulnerability scanner, maintained by Project Discovery 

https://github.com/projectdiscovery/nuclei

## Installing
```bash
# Run as root
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest

# Against every target in urls.txt, run everything in the directory ./nuclei-templates
nuclei -l urls.txt -t nuclei-templates

# Same as above, but only run templates with the tag cve
nuclei -l urls.txt -t nuclei-templates -tags cve
```

Nuclei is used with templates, a lot of these are community maintained. See [[notes/Atomic-Notes/40-TOOLS/4000-OFFENSIVE-TOOLS/4120-NUCLEI/4122-CENT]] for reference.