DNS
Experiment: 3
Aim: To create and configure DNS Server
Description:
DNS Server
A DNS server is a computer server that contains a database of public IP addresses
and their associated hostnames, and in most cases, serves to resolve, or translate,
those common names to IP addresses as requested.
Port No: 53
Package name: bind9
Configuration file: /etc/bind/named.conf. (Primary configuration file),/etc/bind/db.root
(root nameservers)
Procedure:
CASHING NAMESERVER
When configured as a caching nameserver BIND9 will find the answer to name
queries and
remember the answer when the domain is queried again.
1. Install bind9 by typing
$sudo apt install bind9
$sudo apt install dnsutils
2.The default configuration is set up to act as a caching server. All that is required is
simply
adding the IP Addresses of your ISP's DNS servers. Simply uncomment and edit the
following in /etc/bind/named.conf.options:
 3.Restart it by typing
 $sudo systemctl restart bind9.service
PRIMARY MASTER
As a primary master server BIND9 reads the data for a zone from a file on it's host
and is authoritative for that zone.
Forward zone file
To add a DNS zone to BIND9, turning BIND9 into a Primary Master server, the first
step is to edit /etc/bind/named.conf.local:
$sudo cp /etc/bind/db.local /etc/bind/db.example.com
$sudo systemctl restart bind9.service
Reverse Zone File
Now that the zone is set up and resolving names to IP Addresses, a Reverse zone
needs to be added to allows DNS to resolve an address to a name.
1. Edit /etc/bind/named.conf.local
2. Now create the /etc/bind/db.192 file:
$sudo cp /etc/bind/db.127 /etc/bind/db.192
3. edit /etc/bind/db.192 changing the basically the same options as
/etc/bind/db.example.com:
4.After creating the reverse zone file restart BIND9:
$sudo systemctl restart bind9.service
5.Check the status
$Sudo service bind9 status
6.Check if nslookup can resolve
$nslookup ftp.example.com
$nslookup ubuntu.example.com
7.Gather information about your DNS server
$dig ubuntu.example.com
$dig www.example.com
$dig ftp.example.com