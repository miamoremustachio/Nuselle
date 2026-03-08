The *Transmission Control Protocol* (TCP) is a transport [[protocols|protocol]] which controls the way data is sent and received on the Internet.

Before transmitting data, TCP opens a connection with the recipient, ensuring that all packets arrive in order once transmission begins.
The recipient will acknowledge receiving each packet that arrives, and if no acknowledgement is received, missing packets will be sent again.

TCP is designed for *reliability*, not speed.
Because TCP has to make sure all packets arrive in order, loading data via TCP can take longer if some packets are missing.

TCP and [[IP]] were originally designed to be used together, and these are often referred to as the *TCP/IP*.
However, other transport protocols can be used with IP.




[^1]: Sources:
	https://www.cloudflare.com/learning/network-layer/internet-protocol/
