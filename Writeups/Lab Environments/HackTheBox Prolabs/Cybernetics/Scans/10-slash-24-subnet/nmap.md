```
# Nmap 7.94SVN scan initiated Thu May  1 11:56:12 2025 as: nmap -sC -sV -v -p- -o nmap --min-rate 10000 10.10.110.0/24
Nmap scan report for 10.10.110.0 [host down]
Nmap scan report for 10.10.110.1 [host down]
Nmap scan report for 10.10.110.3 [host down]
Nmap scan report for 10.10.110.4 [host down]
Nmap scan report for 10.10.110.5 [host down]
Nmap scan report for 10.10.110.6 [host down]
Nmap scan report for 10.10.110.7 [host down]
Nmap scan report for 10.10.110.8 [host down]
Nmap scan report for 10.10.110.9 [host down]
Nmap scan report for 10.10.110.2
Host is up (0.050s latency).
All 65535 scanned ports on 10.10.110.2 are in ignored states.
Not shown: 65535 filtered tcp ports (no-response)

Nmap scan report for 10.10.110.10
Host is up (0.049s latency).
Not shown: 65531 filtered tcp ports (no-response)
PORT      STATE  SERVICE VERSION
80/tcp    open   http    Microsoft IIS httpd 10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
| http-robots.txt: 30 disallowed entries (15 shown)
| /admin/ /App_Browsers/ /App_Code/ /App_Data/ 
| /App_GlobalResources/ /bin/ /Components/ /Config/ /contest/ /controls/ 
|_/DesktopModules/ /Documentation/ /HttpModules/ /images/ /Install/
|_http-favicon: Unknown favicon MD5: 2DE6897008EB657D2EC770FE5B909439
|_http-title: Home
443/tcp   closed https
3391/tcp  closed savant
49443/tcp closed unknown
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Nmap scan report for 10.10.110.11
Host is up (0.049s latency).
Not shown: 65531 filtered tcp ports (no-response)
PORT      STATE  SERVICE  VERSION
80/tcp    open   http     Microsoft IIS httpd 10.0
|_http-server-header: Microsoft-IIS/10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-title: IIS Windows Server
443/tcp   open   ssl/http Microsoft IIS httpd 10.0
| tls-alpn: 
|   h2
|_  http/1.1
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
|_http-title: IIS Windows Server
| ssl-cert: Subject: commonName=certenroll.cyber.local
| Issuer: commonName=Cyber-CA
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: ecdsa-with-SHA256
| Not valid before: 2024-01-13T06:54:32
| Not valid after:  2026-01-12T06:54:32
| MD5:   5083:51d1:f465:a511:ef2d:9186:ace3:9ffd
|_SHA-1: 2320:5c90:75f1:1a1f:f85d:1825:7162:786b:8baa:a3fb
|_ssl-date: 2025-05-01T15:57:30+00:00; -1s from scanner time.
3391/tcp  closed savant
49443/tcp closed unknown
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: -1s

Nmap scan report for 10.10.110.12
Host is up (0.050s latency).
Not shown: 65531 filtered tcp ports (no-response)
PORT      STATE  SERVICE VERSION
80/tcp    open   http    Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
443/tcp   open   https?
3391/tcp  closed savant
49443/tcp open   unknown
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Nmap scan report for 10.10.110.13 [host down]
Nmap scan report for 10.10.110.14 [host down]
Nmap scan report for 10.10.110.16 [host down]
Nmap scan report for 10.10.110.17 [host down]
Nmap scan report for 10.10.110.18 [host down]
Nmap scan report for 10.10.110.19 [host down]
Nmap scan report for 10.10.110.20 [host down]
Nmap scan report for 10.10.110.21 [host down]
Nmap scan report for 10.10.110.22 [host down]
Nmap scan report for 10.10.110.23 [host down]
Nmap scan report for 10.10.110.24 [host down]
Nmap scan report for 10.10.110.25 [host down]
Nmap scan report for 10.10.110.26 [host down]
Nmap scan report for 10.10.110.27 [host down]
Nmap scan report for 10.10.110.28 [host down]
Nmap scan report for 10.10.110.29 [host down]
Nmap scan report for 10.10.110.30 [host down]
Nmap scan report for 10.10.110.31 [host down]
Nmap scan report for 10.10.110.32 [host down]
Nmap scan report for 10.10.110.33 [host down]
Nmap scan report for 10.10.110.34 [host down]
Nmap scan report for 10.10.110.35 [host down]
Nmap scan report for 10.10.110.36 [host down]
Nmap scan report for 10.10.110.37 [host down]
Nmap scan report for 10.10.110.38 [host down]
Nmap scan report for 10.10.110.39 [host down]
Nmap scan report for 10.10.110.40 [host down]
Nmap scan report for 10.10.110.41 [host down]
Nmap scan report for 10.10.110.42 [host down]
Nmap scan report for 10.10.110.43 [host down]
Nmap scan report for 10.10.110.44 [host down]
Nmap scan report for 10.10.110.45 [host down]
Nmap scan report for 10.10.110.46 [host down]
Nmap scan report for 10.10.110.47 [host down]
Nmap scan report for 10.10.110.48 [host down]
Nmap scan report for 10.10.110.49 [host down]
Nmap scan report for 10.10.110.50 [host down]
Nmap scan report for 10.10.110.51 [host down]
Nmap scan report for 10.10.110.52 [host down]
Nmap scan report for 10.10.110.53 [host down]
Nmap scan report for 10.10.110.54 [host down]
Nmap scan report for 10.10.110.55 [host down]
Nmap scan report for 10.10.110.56 [host down]
Nmap scan report for 10.10.110.57 [host down]
Nmap scan report for 10.10.110.58 [host down]
Nmap scan report for 10.10.110.59 [host down]
Nmap scan report for 10.10.110.60 [host down]
Nmap scan report for 10.10.110.61 [host down]
Nmap scan report for 10.10.110.62 [host down]
Nmap scan report for 10.10.110.63 [host down]
Nmap scan report for 10.10.110.64 [host down]
Nmap scan report for 10.10.110.65 [host down]
Nmap scan report for 10.10.110.66 [host down]
Nmap scan report for 10.10.110.67 [host down]
Nmap scan report for 10.10.110.68 [host down]
Nmap scan report for 10.10.110.69 [host down]
Nmap scan report for 10.10.110.70 [host down]
Nmap scan report for 10.10.110.71 [host down]
Nmap scan report for 10.10.110.72 [host down]
Nmap scan report for 10.10.110.73 [host down]
Nmap scan report for 10.10.110.74 [host down]
Nmap scan report for 10.10.110.75 [host down]
Nmap scan report for 10.10.110.76 [host down]
Nmap scan report for 10.10.110.77 [host down]
Nmap scan report for 10.10.110.78 [host down]
Nmap scan report for 10.10.110.79 [host down]
Nmap scan report for 10.10.110.80 [host down]
Nmap scan report for 10.10.110.81 [host down]
Nmap scan report for 10.10.110.82 [host down]
Nmap scan report for 10.10.110.83 [host down]
Nmap scan report for 10.10.110.84 [host down]
Nmap scan report for 10.10.110.85 [host down]
Nmap scan report for 10.10.110.86 [host down]
Nmap scan report for 10.10.110.87 [host down]
Nmap scan report for 10.10.110.88 [host down]
Nmap scan report for 10.10.110.89 [host down]
Nmap scan report for 10.10.110.90 [host down]
Nmap scan report for 10.10.110.91 [host down]
Nmap scan report for 10.10.110.92 [host down]
Nmap scan report for 10.10.110.93 [host down]
Nmap scan report for 10.10.110.94 [host down]
Nmap scan report for 10.10.110.95 [host down]
Nmap scan report for 10.10.110.96 [host down]
Nmap scan report for 10.10.110.97 [host down]
Nmap scan report for 10.10.110.98 [host down]
Nmap scan report for 10.10.110.99 [host down]
Nmap scan report for 10.10.110.100 [host down]
Nmap scan report for 10.10.110.101 [host down]
Nmap scan report for 10.10.110.102 [host down]
Nmap scan report for 10.10.110.103 [host down]
Nmap scan report for 10.10.110.104 [host down]
Nmap scan report for 10.10.110.105 [host down]
Nmap scan report for 10.10.110.106 [host down]
Nmap scan report for 10.10.110.107 [host down]
Nmap scan report for 10.10.110.108 [host down]
Nmap scan report for 10.10.110.109 [host down]
Nmap scan report for 10.10.110.110 [host down]
Nmap scan report for 10.10.110.111 [host down]
Nmap scan report for 10.10.110.112 [host down]
Nmap scan report for 10.10.110.113 [host down]
Nmap scan report for 10.10.110.114 [host down]
Nmap scan report for 10.10.110.115 [host down]
Nmap scan report for 10.10.110.116 [host down]
Nmap scan report for 10.10.110.117 [host down]
Nmap scan report for 10.10.110.118 [host down]
Nmap scan report for 10.10.110.119 [host down]
Nmap scan report for 10.10.110.120 [host down]
Nmap scan report for 10.10.110.121 [host down]
Nmap scan report for 10.10.110.122 [host down]
Nmap scan report for 10.10.110.123 [host down]
Nmap scan report for 10.10.110.124 [host down]
Nmap scan report for 10.10.110.125 [host down]
Nmap scan report for 10.10.110.126 [host down]
Nmap scan report for 10.10.110.127 [host down]
Nmap scan report for 10.10.110.128 [host down]
Nmap scan report for 10.10.110.129 [host down]
Nmap scan report for 10.10.110.130 [host down]
Nmap scan report for 10.10.110.131 [host down]
Nmap scan report for 10.10.110.132 [host down]
Nmap scan report for 10.10.110.133 [host down]
Nmap scan report for 10.10.110.134 [host down]
Nmap scan report for 10.10.110.135 [host down]
Nmap scan report for 10.10.110.136 [host down]
Nmap scan report for 10.10.110.137 [host down]
Nmap scan report for 10.10.110.138 [host down]
Nmap scan report for 10.10.110.139 [host down]
Nmap scan report for 10.10.110.140 [host down]
Nmap scan report for 10.10.110.141 [host down]
Nmap scan report for 10.10.110.142 [host down]
Nmap scan report for 10.10.110.143 [host down]
Nmap scan report for 10.10.110.144 [host down]
Nmap scan report for 10.10.110.145 [host down]
Nmap scan report for 10.10.110.146 [host down]
Nmap scan report for 10.10.110.147 [host down]
Nmap scan report for 10.10.110.148 [host down]
Nmap scan report for 10.10.110.149 [host down]
Nmap scan report for 10.10.110.150 [host down]
Nmap scan report for 10.10.110.151 [host down]
Nmap scan report for 10.10.110.152 [host down]
Nmap scan report for 10.10.110.153 [host down]
Nmap scan report for 10.10.110.154 [host down]
Nmap scan report for 10.10.110.155 [host down]
Nmap scan report for 10.10.110.156 [host down]
Nmap scan report for 10.10.110.157 [host down]
Nmap scan report for 10.10.110.158 [host down]
Nmap scan report for 10.10.110.159 [host down]
Nmap scan report for 10.10.110.160 [host down]
Nmap scan report for 10.10.110.161 [host down]
Nmap scan report for 10.10.110.162 [host down]
Nmap scan report for 10.10.110.163 [host down]
Nmap scan report for 10.10.110.164 [host down]
Nmap scan report for 10.10.110.165 [host down]
Nmap scan report for 10.10.110.166 [host down]
Nmap scan report for 10.10.110.167 [host down]
Nmap scan report for 10.10.110.168 [host down]
Nmap scan report for 10.10.110.169 [host down]
Nmap scan report for 10.10.110.170 [host down]
Nmap scan report for 10.10.110.171 [host down]
Nmap scan report for 10.10.110.172 [host down]
Nmap scan report for 10.10.110.173 [host down]
Nmap scan report for 10.10.110.174 [host down]
Nmap scan report for 10.10.110.175 [host down]
Nmap scan report for 10.10.110.176 [host down]
Nmap scan report for 10.10.110.177 [host down]
Nmap scan report for 10.10.110.178 [host down]
Nmap scan report for 10.10.110.179 [host down]
Nmap scan report for 10.10.110.180 [host down]
Nmap scan report for 10.10.110.181 [host down]
Nmap scan report for 10.10.110.182 [host down]
Nmap scan report for 10.10.110.183 [host down]
Nmap scan report for 10.10.110.184 [host down]
Nmap scan report for 10.10.110.185 [host down]
Nmap scan report for 10.10.110.186 [host down]
Nmap scan report for 10.10.110.187 [host down]
Nmap scan report for 10.10.110.188 [host down]
Nmap scan report for 10.10.110.189 [host down]
Nmap scan report for 10.10.110.190 [host down]
Nmap scan report for 10.10.110.191 [host down]
Nmap scan report for 10.10.110.192 [host down]
Nmap scan report for 10.10.110.193 [host down]
Nmap scan report for 10.10.110.194 [host down]
Nmap scan report for 10.10.110.195 [host down]
Nmap scan report for 10.10.110.196 [host down]
Nmap scan report for 10.10.110.197 [host down]
Nmap scan report for 10.10.110.198 [host down]
Nmap scan report for 10.10.110.199 [host down]
Nmap scan report for 10.10.110.200 [host down]
Nmap scan report for 10.10.110.201 [host down]
Nmap scan report for 10.10.110.202 [host down]
Nmap scan report for 10.10.110.203 [host down]
Nmap scan report for 10.10.110.204 [host down]
Nmap scan report for 10.10.110.205 [host down]
Nmap scan report for 10.10.110.206 [host down]
Nmap scan report for 10.10.110.207 [host down]
Nmap scan report for 10.10.110.208 [host down]
Nmap scan report for 10.10.110.209 [host down]
Nmap scan report for 10.10.110.210 [host down]
Nmap scan report for 10.10.110.211 [host down]
Nmap scan report for 10.10.110.212 [host down]
Nmap scan report for 10.10.110.213 [host down]
Nmap scan report for 10.10.110.214 [host down]
Nmap scan report for 10.10.110.215 [host down]
Nmap scan report for 10.10.110.216 [host down]
Nmap scan report for 10.10.110.217 [host down]
Nmap scan report for 10.10.110.218 [host down]
Nmap scan report for 10.10.110.219 [host down]
Nmap scan report for 10.10.110.220 [host down]
Nmap scan report for 10.10.110.221 [host down]
Nmap scan report for 10.10.110.222 [host down]
Nmap scan report for 10.10.110.223 [host down]
Nmap scan report for 10.10.110.224 [host down]
Nmap scan report for 10.10.110.225 [host down]
Nmap scan report for 10.10.110.226 [host down]
Nmap scan report for 10.10.110.227 [host down]
Nmap scan report for 10.10.110.228 [host down]
Nmap scan report for 10.10.110.229 [host down]
Nmap scan report for 10.10.110.230 [host down]
Nmap scan report for 10.10.110.231 [host down]
Nmap scan report for 10.10.110.232 [host down]
Nmap scan report for 10.10.110.233 [host down]
Nmap scan report for 10.10.110.234 [host down]
Nmap scan report for 10.10.110.235 [host down]
Nmap scan report for 10.10.110.236 [host down]
Nmap scan report for 10.10.110.237 [host down]
Nmap scan report for 10.10.110.238 [host down]
Nmap scan report for 10.10.110.239 [host down]
Nmap scan report for 10.10.110.240 [host down]
Nmap scan report for 10.10.110.241 [host down]
Nmap scan report for 10.10.110.242 [host down]
Nmap scan report for 10.10.110.243 [host down]
Nmap scan report for 10.10.110.244 [host down]
Nmap scan report for 10.10.110.245 [host down]
Nmap scan report for 10.10.110.246 [host down]
Nmap scan report for 10.10.110.247 [host down]
Nmap scan report for 10.10.110.248 [host down]
Nmap scan report for 10.10.110.249 [host down]
Nmap scan report for 10.10.110.251 [host down]
Nmap scan report for 10.10.110.252 [host down]
Nmap scan report for 10.10.110.253 [host down]
Nmap scan report for 10.10.110.254 [host down]
Nmap scan report for 10.10.110.255 [host down]
Nmap scan report for 10.10.110.15
Host is up (0.13s latency).
Not shown: 65531 filtered tcp ports (no-response)
PORT      STATE  SERVICE  VERSION
80/tcp    open   http     Microsoft IIS httpd 10.0
|_http-title: IIS Windows Server
|_http-server-header: Microsoft-IIS/10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
443/tcp   open   ssl/http Microsoft IIS httpd 10.0
|_ssl-date: 2025-05-01T16:00:32+00:00; 0s from scanner time.
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
|_http-title: IIS Windows Server
| ssl-cert: Subject: commonName=cygw.cyber.local
| Subject Alternative Name: DNS:gateway.cyber.local
| Issuer: commonName=Cyber-CA
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: ecdsa-with-SHA256
| Not valid before: 2020-06-03T03:39:02
| Not valid after:  2022-06-03T03:39:02
| MD5:   acbd:38b1:c67f:07ee:0b9b:76a6:d71e:96f1
|_SHA-1: 1974:25b5:aeac:91c9:404e:f243:e0cd:0488:b649:927b
| tls-alpn: 
|_  http/1.1
3391/tcp  closed savant
49443/tcp closed unknown
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Nmap scan report for 10.10.110.250
Host is up (0.082s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT   STATE SERVICE VERSION
80/tcp open  http    OPNsense
|_http-trane-info: Problem with XML parsing of /evox/about
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: OPNsense
|_http-title: Login
|_http-favicon: Unknown favicon MD5: E4FD990B4B8A5D61BD5DDB98CDFC7190
| fingerprint-strings: 
|   GetRequest: 
|     HTTP/1.0 200 OK
|     Content-Security-Policy: default-src 'self'; script-src 'self' 'unsafe-inline' 'unsafe-eval'; style-src 'self' 'unsafe-inline' 'unsafe-eval';
|     X-Frame-Options: SAMEORIGIN
|     X-Content-Type-Options: nosniff
|     X-XSS-Protection: 1; mode=block
|     Referrer-Policy: same-origin
|     Set-Cookie: PHPSESSID=40ad367bcbaa7d843e14588d63f6ec44; path=/
|     Set-Cookie: PHPSESSID=40ad367bcbaa7d843e14588d63f6ec44; path=/; HttpOnly
|     Expires: Thu, 19 Nov 1981 08:52:00 GMT
|     Cache-Control: no-store, no-cache, must-revalidate
|     Pragma: no-cache
|     Content-type: text/html; charset=UTF-8
|     Content-Length: 1798
|     Connection: close
|     Date: Thu, 01 May 2025 15:58:10 GMT
|     Server: OPNsense
|     <!doctype html>
|     <!--[if IE 8 ]><html lang="en" class="ie ie8 lte9 lte8 no-js"><![endif]-->
|     <!--[if IE 9 ]><html lang="en" class="ie ie9 lte9 no-js"><![endif]-->
|     <!--[if (gt IE 9)|!(IE)]><!--><html lang="en" class="no-js"><!--<![e
|   HTTPOptions: 
|     HTTP/1.0 403 Forbidden
|     Set-Cookie: PHPSESSID=907242d4fbb241c2de50326985b1e520; path=/
|     Set-Cookie: PHPSESSID=907242d4fbb241c2de50326985b1e520; path=/; HttpOnly
|     Expires: Thu, 19 Nov 1981 08:52:00 GMT
|     Cache-Control: no-store, no-cache, must-revalidate
|     Pragma: no-cache
|     Content-type: text/html; charset=UTF-8
|     Content-Length: 563
|     Connection: close
|     Date: Thu, 01 May 2025 15:58:10 GMT
|     Server: OPNsense
|     <html><head><title>CSRF check failed</title>
|     <script>
|     document ).ready(function() {
|     $.ajaxSetup({
|     'beforeSend': function(xhr) {
|     xhr.setRequestHeader("X-CSRFToken", "Z0haTVpqVmVheTdlWjRJRkZMVk1mZz09" );
|     </script>
|     </head>
|     <body>
|_    <p>CSRF check failed. Your form session may have expired, o
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port80-TCP:V=7.94SVN%I=7%D=5/1%Time=68139A13%P=x86_64-pc-linux-gnu%r(Ge
SF:tRequest,9A5,"HTTP/1\.0\x20200\x20OK\r\nContent-Security-Policy:\x20def
SF:ault-src\x20'self';\x20script-src\x20'self'\x20'unsafe-inline'\x20'unsa
SF:fe-eval';\x20style-src\x20'self'\x20'unsafe-inline'\x20'unsafe-eval';\r
SF:\nX-Frame-Options:\x20SAMEORIGIN\r\nX-Content-Type-Options:\x20nosniff\
SF:r\nX-XSS-Protection:\x201;\x20mode=block\r\nReferrer-Policy:\x20same-or
SF:igin\r\nSet-Cookie:\x20PHPSESSID=40ad367bcbaa7d843e14588d63f6ec44;\x20p
SF:ath=/\r\nSet-Cookie:\x20PHPSESSID=40ad367bcbaa7d843e14588d63f6ec44;\x20
SF:path=/;\x20HttpOnly\r\nExpires:\x20Thu,\x2019\x20Nov\x201981\x2008:52:0
SF:0\x20GMT\r\nCache-Control:\x20no-store,\x20no-cache,\x20must-revalidate
SF:\r\nPragma:\x20no-cache\r\nContent-type:\x20text/html;\x20charset=UTF-8
SF:\r\nContent-Length:\x201798\r\nConnection:\x20close\r\nDate:\x20Thu,\x2
SF:001\x20May\x202025\x2015:58:10\x20GMT\r\nServer:\x20OPNsense\r\n\r\n<!d
SF:octype\x20html>\n<!--\[if\x20IE\x208\x20\]><html\x20lang=\"en\"\x20clas
SF:s=\"ie\x20ie8\x20lte9\x20lte8\x20no-js\"><!\[endif\]-->\n<!--\[if\x20IE
SF:\x209\x20\]><html\x20lang=\"en\"\x20class=\"ie\x20ie9\x20lte9\x20no-js\
SF:"><!\[endif\]-->\n<!--\[if\x20\(gt\x20IE\x209\)\|!\(IE\)\]><!--><html\x
SF:20lang=\"en\"\x20class=\"no-js\"><!--<!\[e")%r(HTTPOptions,3CC,"HTTP/1\
SF:.0\x20403\x20Forbidden\r\nSet-Cookie:\x20PHPSESSID=907242d4fbb241c2de50
SF:326985b1e520;\x20path=/\r\nSet-Cookie:\x20PHPSESSID=907242d4fbb241c2de5
SF:0326985b1e520;\x20path=/;\x20HttpOnly\r\nExpires:\x20Thu,\x2019\x20Nov\
SF:x201981\x2008:52:00\x20GMT\r\nCache-Control:\x20no-store,\x20no-cache,\
SF:x20must-revalidate\r\nPragma:\x20no-cache\r\nContent-type:\x20text/html
SF:;\x20charset=UTF-8\r\nContent-Length:\x20563\r\nConnection:\x20close\r\
SF:nDate:\x20Thu,\x2001\x20May\x202025\x2015:58:10\x20GMT\r\nServer:\x20OP
SF:Nsense\r\n\r\n<html><head><title>CSRF\x20check\x20failed</title>\n\x20\
SF:x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20<script>\n\x20\x20\x20\x20\x
SF:20\x20\x20\x20\x20\x20\x20\x20\x20\x20\$\(\x20document\x20\)\.ready\(fu
SF:nction\(\)\x20{\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x20\x20\x20\x20\$\.ajaxSetup\({\n\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20\x20\x20\x20\x20\x20\x20\x20\x20'beforeSend':\x20function\(xhr\)\x
SF:20{\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x20\x20\x20\x20\x20xhr\.setRequestHeader\(\"X-CSRFToken\",\x20\"Z0ha
SF:TVpqVmVheTdlWjRJRkZMVk1mZz09\"\x20\);\n\x20\x20\x20\x20\x20\x20\x20\x20
SF:\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20}\n\x20\x20\x20\x20\x20\x20\x20
SF:\x20\x20\x20\x20\x20\x20\x20\x20\x20}\);\n\x20\x20\x20\x20\x20\x20\x20\
SF:x20\x20\x20\x20\x20\x20\x20}\);\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x20\x20</script>\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20</
SF:head>\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20
SF:\x20\x20<body>\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20\x20\x20\x20<p>CSRF\x20check\x20failed\.\x20Your\x20form\x20sessio
SF:n\x20may\x20have\x20expired,\x20o");

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu May  1 12:00:33 2025 -- 256 IP addresses (6 hosts up) scanned in 261.19 seconds

```