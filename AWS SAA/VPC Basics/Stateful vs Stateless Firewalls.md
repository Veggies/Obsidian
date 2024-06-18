Everyone connection (Ex. An endpoint talking to a server) has two parts, not just a single outbound request.
	There is a request from the endpoint
	Client picks an ephemeral port (1024-65535) that is assigned as the source port (192.168.245.245:2445)
			Client initiates connection to a well-known port number (192.168.245.245:2445 initiates a connection to port 80)
	There is a response from the server
			Server on port 80 connects back to source IP on the source port (Ephemeral port).
Stateless firewalls
	Firewall does not see states of connections (Inbound/Outbound)
	Have to allow the entire range of ephemeral ports to allow connections
Stateful Firewalls
	Can identify request and response connections, and link them together
	Allowing requests means the response is automatically allowed
	Lower admin overhead