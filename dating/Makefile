

dating-server:
	$(TROUPE)/bin/troupec dating-server.trp -o ./out/dating-server.js
	node $(TROUPE)/rt/built/troupe.js -f=./out/dating-server.js --id=../ids/id-server.json --trustmap=../trustmaps/GoT.json --aliases=aliases.json

dating-client:
	$(TROUPE)/bin/troupec dating-client.trp -o ./out/dating-client.js
	node $(TROUPE)/rt/built/troupe.js -f=./out/dating-client.js --id=../ids/id-client1.json --trustmap=../trustmaps/client.json --aliases=aliases.json

dating-server-own:
	$(TROUPE)/bin/troupec dating-server.trp -o ./out/dating-server-own.js
	node $(TROUPE)/rt/built/troupe.js -f=./out/dating-server-own.js --id=../ids/id-server.json --trustmap=../trustmaps/client.json --aliases=aliases.json




