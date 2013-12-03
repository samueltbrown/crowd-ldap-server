# Crowd LDAP Server

Implementation of an LDAP server that delegates authentication to an Atlassian Crowd installation
using the Crowd REST API. 

This service allows your favourite SSO authentication source to be used from many legacy devices, appliances and systems.

The LDAP implementation is based on the Apache Directory Server v1.5.7,  which is distributed under the Apache v2.0 License.

STB 12/2/2013

Had to add the following iptables rule to run the server on localhost:
iptables -t nat -I OUTPUT -p tcp -d 127.0.0.1 --dport 80 -j REDIRECT --to-ports 8095

