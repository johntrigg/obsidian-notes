Nuclei is a free and open-source vulnerability scanner, maintained by Project Discovery 

https://github.com/projectdiscovery/nuclei

## Installing
```bash
# Run as root
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
```

Nuclei is used with templates, a lot of these are community maintained. Somebody made a nice tool to aggregate these. 

https://github.com/xm1k3/cent

```bash
# Install, run as root
go install -v github.com/xm1k3/cent@latest

# Clone and insert nuclei templates into the a folder called 'nuclei-templates'
cent -p nuclei-templates
```
