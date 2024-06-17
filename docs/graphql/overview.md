Problems with REST
Fixed Entity structure
- the client cannot specify the entity parts it want to retrieve
- the entity returned is set by the backend developer and cannot be modified on a per-query basis
- there is no way to retrieve only the fields are needed
- increases load time and network latency
- sometimes forces to create specialized entity types just for specific queries - maintenance and data model problem
Request-Response Only
- push notifications are becoming extremely useful
- can be implementing using:
	- Polling
	- Web Sockets
- not part of the protocol
- complex
