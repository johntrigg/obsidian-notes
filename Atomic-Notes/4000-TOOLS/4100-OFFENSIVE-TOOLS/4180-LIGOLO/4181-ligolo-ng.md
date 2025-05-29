//TODO: UPDATE ESPANSO TO USE MODERN LIGOLO WINDOWS AGENT, LINUX AGENT, AND LINUX SERVER

Ligolo is used for pivoting

```bash
# Get windows agent, extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_agent_0.8.2_windows_amd64.zip 
&& unzip ligolo-ng_agent_0.8.2_windows_amd64.zip 
&& move agent.exe ligolo-windows-agent.exe

# Get the Linux Proxy Server, Extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_proxy_0.8.2_linux_amd64.tar.gz 
&& tar -xvf ligolo-ng_proxy_0.8.2_linux_amd64.tar.gz 
&& mv proxy ligolo-proxy-server


# Get the Linux Agent, Extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_agent_0.8.2_linux_amd64.tar.gz 
&& tar -xvf ligolo-ng_agent_0.8.2_linux_amd64.tar.gz 
&& mv agent ligolo-linux-agent




```
Ligolo