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
Note that clientMal is constantly listening for new user to match with and will make the server sleep for 20 sec if an user is a female. As soon as clientMal receives a new user to match with start clientMal2 , which will time the execution time of trying to match with clientMal. If it takes a significant long time to match, then the user is a female otherwise a male. NOTE: clientMal2 will exit as soon as the timing is done, if you wish to continue testing other users just run "make dating-clientMal2" again.

* make dating-clientMal
* make dating-clientMal2

## To run the server together with the provided GoT clients, do the following:

* cd ~/dating
* Modify the dating-server.trp by removing the comment:  (* send (whereis ("@dispatcher", "dispatcher"), ("DISPATCH", thisNode)); *) on line 63.

**Call the Troupe files using the makefile**
* make dating-server-own 

