# Information Flow Control

The projects implements a dating server where the clients provide their own functions in order to match with other users.
The project is written in Troupe.

## To run the server together with client1, client2, and malicious client, do the following:

* cd ~/dating

**Call the Troupe files using the makefile**
* make dating-server-own 
* make dating-client1
* make dating-client2

The malicious clients tries to exfiltrate confidentail gender information about the other legitimate users.

make dating-clientMal
make dating-clientMal2

## To run the server together with the provided GoT clients, do the following:

