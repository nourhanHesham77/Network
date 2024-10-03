
# LAB => 3.1.4 packet tracer => who hears the broadcast
  - **Simulation Mode** in Cisco Packet Tracer is used for step-by-step observation of network activities and traffic :
	  - - **Detailed Packet Analysis**: It allows you to see exactly how packets travel through your network, including the protocols used, device interactions, and how different types of traffic are handled.
    
	- **Troubleshooting**: In **Real-Time Mode**, traffic flows continuously, making it difficult to spot problems or packet behavior. In **Simulation Mode**, you can pause or slow down the traffic, making it easier to identify and troubleshoot network issues.

- ### Add Complex PDU tool
	The **Add Complex PDU tool** in Cisco Packet Tracer allows you to create custom packets for testing purposes, such as sending broadcast messages or simulating specific types of traffic. It’s represented by an **envelope icon** and is used to manually create and configure PDUs (Protocol Data Units).
	
	 - ### PDU
		 - Think of it as a **package** of information that gets passed around between devices. The name changes depending on where it is in the communication process:
		- **Data**: When it's at the application level (like when you send a message).
		- **Segment**: When it’s being sent using the transport layer (like TCP).
		- **Packet**: When it’s at the network layer (like when it’s being routed).
		- **Frame**: When it’s at the data link layer (like when it's being sent over Ethernet).


- **Sequence Number** and **One Shot Time**
		are part of the configuration settings when creating a Complex PDU in Cisco Packet Tracer
		
	### **Sequence Number**:
	- **Purpose**: This number helps **identify** and **track individual packets** in a sequence.
	- **Why it's used**: If you are sending multiple packets, each one will have a unique sequence number (like 1, 2, 3, etc.) so that you can tell them apart and see their order of transmission. For example, when sending multiple ICMP (ping) messages, each will have a different sequence number to track how many were sent and their responses.
	
	### **One Shot Time**:
	- **Purpose**: This specifies the amount of time (in seconds) **before the packet is sent**  => delay


- ### Reflection Questions
		1.  What happens to a frame sent from a PC in VLAN 10 to a PC in VLAN 30?
			- The frame will not be forwarded to the PC in VLAN 30 because VLANs are separate broadcast domains. A frame sent from VLAN 10 will only be received by devices within VLAN 10 unless a router or a Layer 3 switch is used to route the traffic between VLANs
		2.  Which ports on the switch light up if a PC connected to port 11 sends a unicast message to a PC connected to port 13?
			- Only port 11 (the sender) and port 13 (the receiver) will light up. The switch learns which devices are connected to which ports based on the MAC addresses of the frames it receives, and it only sends the frame out the port that is connected to the destination device.
		3. In terms of ports, what are the collision domains on the switch?
			- Each port is its own collision domain => Each port handles its own traffic separately, so there’s no interference between devices on different ports
			- On a switch, **each port** = **1 collision domain**, which helps prevent data collisions.
		4. In terms of ports, what are the broadcast domains on the switch?
			- Each VLAN is its own broadcast domain
- Main Points
	- Broadcast messages are limited to devices in the same VLAN.
	- Unicast messages only light up the sending and receiving ports , only if they r in the same VLAN
	- Each port represents a separate collision domain. 
	- VLANs define broadcast domains, isolating broadcast traffic to specific groups of devices.