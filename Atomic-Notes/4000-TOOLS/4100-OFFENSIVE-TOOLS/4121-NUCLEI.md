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

Nuclei is used with templates, a lot of these are community maintained. Somebody made a nice tool to aggregate these. 

https://github.com/xm1k3/cent

```bash
# Install, run as root
go install -v github.com/xm1k3/cent@latest

# Or get the release and install manually
wget https://github.com/xm1k3/cent/releases/download/v1.3.4/cent_1.3.4_linux_amd64.zip
unzip cent_1.3.4_linux_amd64.zip

# Copy to /bin directory
cp cent /bin/cent

# Initiate the program
cent init

# Modify config file is needed
vi /home/kali/.cent.yaml

# Clone and insert nuclei templates into the a folder called 'nuclei-templates'
cent -p nuclei-templates
```
