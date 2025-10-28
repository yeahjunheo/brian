#MQTT 

**MQTT**, or **Message Queuing Telemetry Transfer**, gained widespread use in a range of applications mainly due to its capacity to communicate at low bandwidths, the necessity for minimum memory, and reduced packet loss (1).

- lightweight and efficient:
	- IoT device requires minimal resources (small microcontrollers)
- scalable
	- minimal amount of code → consumes little power.
	- designed to support large number of IoT devices (millions)
- reliable
	- can also manage unreliable cellular networks (low bandwidth and high latency)
	- at most once (0); at least once (1); and exactly once (2)
- secure
	- easy to encrypt messages and authenticate devices and users (modern authentication protocols)
- well-supported
	- python has extensive support.

MQTT works on the simple principle of a pub/sub model. This is used to decouple the message sender (publisher) from the message receiver (subscriber). A third component, alled a message broker, handles the communication between the publisher and the subscribers.
- *space decoupling*: both pubber and subber are not aware of each other's network location and do not exchange that information (nor the IP or port)
- *time decoupling*: pubber and subber dont run or have network connectivity at the same time.
- *synchronization decoupling*: pubber and subber dont have to wait to send / receive messages.

MQTT client is any device from a server to a microcontroller that runs an MQTT library. 

MQTT broker is the backend system that coordinates messages between different clients.
- receiving and filtering messages
- identifying clients subscribed to each message
- sending clients the message
- authorizing and authenticating MQTT clients
- passing messages to other systems for further analysis
- handling missed messages and client sessions

MQTT connection

clients and brokers begin communicating using an MQTT connection. Clients initiate the connection by sending a CONNECT message to the MQTT broker. The broker confirms that connection by responding with a CONNACK message. both client and borker require a TCP/IP stack to communicate. *clients only conncet with broker*

MQTT topic: 'topic' refers to keywords the MQTT broker uses to filter messages. organized hierarchically (file or folder).

MQTT publish
MQTT clients publish messages that contain the topic and data inbyte format.

MQTT subscribe

sends a SUBSCRIBE message to the broker, to receive messages on topics of interest. unique identifier and list of subscriptions. 

MQTT over WSS?MQTT over WSS is an MQTT implementation to receive data directly into a web browser. the protocol defines a .js client to provide WSS support for browsers. prtoocol adds additional headers to the MQTT message to support. MQTT message is wrapped in a WSS envelope.

MQTT security
uses SSL protocol to protect sensitive data transmitted by IoT devices. SSL certificates and/or passwords. broker authenticates clients using their passwords as well as unique client identifiers it allocates to each client. client authenticates the server with certificates or DNS lookups. 
- identity
- authentication
- authroization
- encryption protocols with MQTT?

MQTT RESTful?
not RESTful. Representational state transfer is an architectural approach to tnetwork communication that uses the request-response pttern of communication between message senders and receivers. MQTT uses pub/sub model of communication over application layer and requires a standing TCP connection to transmit messages in a psuh manner. MQTT.v5 adds a new req/res method to act in a way similar to REST, where in the pubber can attach a special response topic, which the receiver processes and generates an approrpaite response.

