# The Dark Web Browser (Tor)

Tor is a network that anonymizes web traffic to provide private web browsing. It hides your IP address and web browsing history by redirecting traffic through a series of nodes.

Along with web browsers, Tor also provides anonymity for web server. A .onion web address is accessible only through onion broswer

Is Tor a VPN?
obsolutely N-O. They use different approach in rerouting data. moreover, VPN is operated by central service provider and Tor is decentralized.

Is Tor same as proxy server ?
Again, N-O. Proxy server is an intermediary between you and server, and it doesn't encrypt the traffic. on the other hand, Tor encrpts the traffic and there are more than 7000 nodes between you and server in Tor network.

# Working Mechanism (NeRd stuffs)

To transmit data, Tor uses three levels of nodes
* Entry node - Entry node introduces your data to Tor network. TOr browser randomly picks a entry node for you
* middle node - In middle nodes, your data is fully encrypted. node peel one layer of encryption and send it to the next node. To maintain anonymity, each middle nodes knows only it's predecessor and successor node in the network
* exit node - unencrypted data leaves the Tor network via the exit node.

Complete design : https://apps.dtic.mil/sti/pdfs/ADA465464.pdf 