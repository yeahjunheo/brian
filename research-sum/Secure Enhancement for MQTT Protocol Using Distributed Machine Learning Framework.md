[National Library of Medicine](https://pmc.ncbi.nlm.nih.gov/articles/PMC10935133/)

#MQTT #security #ML 

This paper proposes a new solution that leverages an H2O-based distributed ML framework to improve the security of the MQTT protocol networks, particularly in IoT environments.

Enabling real-time monitoring and distributed detection and classification of anomalous behavior.

## Communication models

### Device-to-device (D2D)
Based on an IP network that allows two or more smart objects to communicate via receiving and sending data.

Exchange is done via ZigBee, Z-Wave, WiFi, and Bluetooth.

Security is simplified due to the one-to-one relationship.

Lower complexity, reducing size and cost
### Device-to-cloud (D2C)
Smart objects connect directly to internet cloud services based on TCP/IP network or WiFi connections.

More complex security than D2D because it involves two different types of network access credentials.

Application layer protocols to communicate, in our case we focus on MQTT.
### Device-to-gateway (D2G)
Smart objects access cloud services via local network gateway (applicaton software to provide security and data protocol transmission between smart objects and the cloud). 


### back-end data-sharing

