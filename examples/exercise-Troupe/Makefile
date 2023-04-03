MKID=node $(TROUPE)/rt/built/p2p/mkid.js
MKALIASES=node $(TROUPE)/rt/built/p2p/mkaliases.js
START=$(TROUPE)/network.sh

myserver:
	$(START) server.trp --id=ids/id-server.json #--trustmap=./trustmaps/server.json --aliases=aliases.json #--debug --debugp2p 

client-alice:
	$(START) clients/alice.trp --id=ids/id-alice.json --trustmap=./trustmaps/clients.json --aliases=aliases.json

client-bob:
	$(START) clients/bob.dist.trp --id=ids/id-bob.json --aliases=aliases.json

create-network-identifiers:
	mkdir -p ids 
	$(MKID) --outfile=ids/id-server.json
	$(MKID) --outfile=ids/id-alice.json
	$(MKID) --outfile=ids/id-bob.json
	$(MKALIASES) --include ids/id-server.json --include ids/id-alice.json --include ids/id-bob.json --outfile aliases.json
