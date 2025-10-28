The open systems interconnection (OSI) model is a conceptual model which provides diverse communication systems to communicate using standard [protocols](https://www.cloudflare.com/learning/network-layer/what-is-a-protocol/)

In other words, the OSI is a standard for different computers to be able to communicate with each other.

# 🧅 Layers

Each layer of the OSI Model handles a specific job and communicates with other layers:
![[osi_model_7_layers.png]]


## 7. App layer

The only layer that directly interacts with data from the user. Software applications like web browsers and email clients rely on the application layer to initiate communications.

Application layer protocols include [HTTP](https://www.cloudflare.com/learning/ddos/glossary/hypertext-transfer-protocol-http/) as well as [SMTP](https://www.cloudflare.com/learning/email-security/what-is-smtp/).
![[osi_model_application_layer_7 1.png]]

## 6. Presentation layer

Makes the data presentable for applications to consume.

Responsible for translation, [encryption](https://www.cloudflare.com/learning/ssl/what-is-encryption/), and compression of data.
![[osi_model_presentation_layer_6.png]]


## 5. Session layer

Responsible for opening and closing communication between the two devices.

The time between when the communication is opened and closed is known as the _session_.

The session layer ensures that the session stays open long enough to transfer all the data being exchanged, and then promptly closes the session in order to avoid wasting resources.
![[osi_model_session_layer_5.png]]

## 4. Transport layer

Responsible for end-to-end communication between devices. This includes taking data from the session layer and breaking it up into chunks called segments before sending it to layer 3.

Transport layer protocols include the [Transmission Control Protocol (TCP)](https://www.cloudflare.com/learning/ddos/glossary/tcp-ip/) and the [User Datagram Protocol (UDP)](https://www.cloudflare.com/learning/ddos/glossary/user-datagram-protocol-udp/).
![[osi_model_transport_layer_4.png]]

## 3. Network layer

Responsible for facilitating data transfer between two different networks. If the two devices communicating are on the same network, then the network layer is unnecessary.

The network layer breaks up segments from the transport layer into smaller units, called [packets](https://www.cloudflare.com/learning/network-layer/what-is-a-packet/), on the sender’s device, and reassembling these packets on the receiving device.

Network layer protocols include IP, the [Internet Control Message Protocol (ICMP)](https://www.cloudflare.com/learning/ddos/glossary/internet-control-message-protocol-icmp/), the [Internet Group Message Protocol (IGMP)](https://www.cloudflare.com/learning/network-layer/what-is-igmp/), and the [IPsec](https://www.cloudflare.com/learning/network-layer/what-is-ipsec/) suite.
![[osi_model_network_layer_3.png]]

## 2. Data link layer

Facilitates data transfer between two devices on the _same_ network.

The data link layer takes packets from the network layer and breaks them into smaller pieces called frames.

Like the network layer, the data link layer is also responsible for flow control and error control in intra-network communication.
![[data_link_layer_osi_model.png]]

## 1. Physical layer

Responsible for transmission of the raw data, which is simply a series of 0s and 1s.

Includes the physical equipment involved in the data transfer, such as the cables, connectors, receivers, and [switches](https://www.cloudflare.com/learning/network-layer/what-is-a-network-switch/).
![[osi_model_physical_layer_1.png]]


> **Source:**
> https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/
