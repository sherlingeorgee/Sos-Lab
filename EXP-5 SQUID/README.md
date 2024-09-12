SQUID
Experiment: 5
Aim: To create and configure Squid -proxy server
Description:
SQUID – PROXY SERVER
Squid is a full-featured web proxy cache server application which provides proxy and
cache services for HyperText Transport Protocol (HTTP), File Transfer Protocol (FTP),
and other popular network protocols. Squid can implement caching and proxying of
Secure Sockets Layer (SSL) requests and caching of Domain Name Server (DNS)
lookups, and perform transparent caching. Squid also supports a wide variety of
caching protocols, such as Internet Cache Protocol (ICP), the HyperText Caching
Protocol (HTCP), the Cache Array Routing Protocol (CARP), and the Web Cache
Coordination Protocol (WCCP).
The Squid proxy cache server is an excellent solution to various proxy and caching
server needs, and scales from the branch office to enterprise-level networks while
providing extensive, granular access control mechanisms, and monitoring of critical
parameters via the Simple Network Management Protocol (SNMP). When selecting a
computer system for use as a dedicated Squid caching proxy server for many users
ensure it is configured with a large amount of physical memory as Squid maintains
an in-memory cache for increased performance.
Port No: 3128
Package name: squid
Configuration file: /etc/squid/squid.conf
Procedure:
1. At a terminal prompt, enter the following command to install the Squid server:
$sudo apt install squid
2. Squid is configured by editing the directives contained within
the /etc/squid/squid.conf configuration file.
3. Change the access as shown below:
acl localnet src 192.168.234.139(your ip address)
acl blocksite dstdomain &quot;/etc/squid/blocksite&quot;
http_access deny blocksite
http_access allow localnet
#http_access deny all
http_access allow all
4. To block access to the website we must configure using
&quot;/etc/squid/blocksite”
we edit the file by running:
$cd /etc/squid
$sudo gedit blocksite
5. Add the websites to block:
in this case, I am blocking youtube, facebook, google
6. To check the actual functioning of the proxy server go to the browser and click
settings, search proxy in connection settings.
7. To configure Proxy access to the internet
8. Select Manual Proxy configuration
9. Type your HTTP Proxy(IP Address) and Port number as 3128.
10. Select SOCKS v5
CONNECTING TO WEBSITE
11. Search for the blocked websites
12. Access is denied to the above websites