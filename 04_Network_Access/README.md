# Cisco Packet Tracer: Connect Two Computers and a Router
## Project Overview
This project demonstrates a basic network setup in Cisco Packet Tracer, where two computers are connected through a router. The setup will allow the two computers to communicate with each other over the network.

## Requirements
- Cisco Packet Tracer: Version 7.0 or later

- Basic understanding of networking concepts

## Topology Overview
- Router: The central device that connects the two computers.

- Switch: To connect many machines via a router.

- Computer 1 (PC1): The first computer in the network.

- Computer 2 (PC2): The second computer in the network.

- Connection Type: Ethernet cables (copper straight-through cables) are used to connect the devices.

## Steps to Create the Network

1. #### Launch Cisco Packet Tracer:

- Open Cisco Packet Tracer on your computer.

2. #### Add Devices to the Workspace:

- Drag and drop a Router from the "Network Devices" section.
- Drag and drop a Switch from the "Network Devices" section.
- Drag and drop two PCs from the "End Devices" section.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725175165/Screenshot_2024-09-01_091853_a15kkj.png)

3. #### Connect the Devices:

- Select the Copper Straight-Through Cable from the "Connections" section.

- Click on PC1 and connect to the FastEthernet0/2 port on the Switch.

- Connect the Router's FastEthernet0/0 port to the switch FastEthernet0/1.

- Repeat the process for PC2, connecting it to the Switch FastEthernet0/3 port.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725174465/Screenshot_2024-09-01_090609_i4nhvu.png)


4. #### Configure IP Addresses:

- Select PC1 and go to the Desktop tab, then select IP Configuration.

    - Set the IP address to 192.168.1.1 with a subnet mask of 255.255.255.0

    - Set the default gateway to 192.168.1.4

    ![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725175231/Screenshot_2024-09-01_092011_bkhblx.png)


- Repeat the process for PC2, setting the IP address to 192.168.1.2 and the same subnet mask and gateway.

5. #### Configure the Router:

- Click on the Router and go to the CLI tab.

- Enter the following commands to configure the router:

```
Router> enable
Router# configure terminal
Router(config)# interface FastEthernet0/0
Router(config-if)# ip address 192.168.1.4 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# exit
Router(config)# exit
```
![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725175357/Screenshot_2024-09-01_092217_q3oanc.png)

6. Test the Connectivity:

- Go to PC1 and open the Command Prompt from the Desktop tab.

- Type ping 192.168.1.2 and press enter to check the connection between the two PCs.

- You should see replies from 192.168.1.2, confirming the network is set up correctly.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725175477/Screenshot_2024-09-01_092351_lkp3w1.png)

## Project Files

- Packet Tracer File: You can download the completed .pkt file from the repository to see the configured network.

## Troubleshooting

- No Connectivity: Ensure that the cables are connected to the correct ports and that the devices are powered on.

- Incorrect IP Address: Double-check the IP configuration on both PCs and the router.

- Router Configuration: Make sure the router interfaces are configured and not in a shutdown state.

## License
This project is licensed under the MIT License - see the LICENSE file for details.