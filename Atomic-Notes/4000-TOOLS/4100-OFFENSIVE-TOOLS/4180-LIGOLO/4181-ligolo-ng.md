//TODO: UPDATE ESPANSO TO USE MODERN LIGOLO WINDOWS AGENT, LINUX AGENT, AND LINUX SERVER

Ligolo is used for pivoting. We can install it with the below commands.

```bash
# Get windows agent, extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_agent_0.8.2_windows_amd64.zip && unzip ligolo-ng_agent_0.8.2_windows_amd64.zip && mv agent.exe ligolo-windows-agent.exe && rm *.gz && rm *.md && rm LICENSE

# Get the Linux Proxy Server, Extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_proxy_0.8.2_linux_amd64.tar.gz && tar -xvf ligolo-ng_proxy_0.8.2_linux_amd64.tar.gz && mv proxy ligolo-proxy-server && rm *.gz && rm *.md && rm LICENSE


# Get the Linux Agent, Extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_agent_0.8.2_linux_amd64.tar.gz && tar -xvf ligolo-ng_agent_0.8.2_linux_amd64.tar.gz && mv agent ligolo-linux-agent && rm *.gz && rm *.md && rm LICENSE

```

There's two parts: a proxy server running on our attack machine, and agents running on compromised machines. The agents will call back to the attacking machine's proxy server.