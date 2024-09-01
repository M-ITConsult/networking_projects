# Cisco Packet Tracer: Connect Three Computers and two Routers with Switchs

## Project Overview
This project demonstrates a basic network setup in Cisco Packet Tracer, where two computers are connected through three routers and two Switchs. The setup will allow the three computers to communicate with each other over the network.

## Requirements
- Cisco Packet Tracer: Version 7.0 or later

- Basic understanding of networking concepts

## Topology Overview
- Router: The central device that connects the two computers.

- Switch: To connect many machines via a router.

- Computer 1 (PC1): The first computer in the network.

- Computer 2 (PC2): The second computer in the network.

- Computer 3 (Laptop1): The third computer in the network.

- Connection Type: Ethernet cables (copper straight-through cables) are used to connect the devices.

## Steps to Create the Network

1. #### Launch Cisco Packet Tracer:

- Open Cisco Packet Tracer on your computer.

2. #### Add Devices to the Workspace:

- Drag and drop two Routers from the "Network Devices" section.
- Drag and drop two Switchs from the "Network Devices" section.
- Drag and drop two PCs and one laptop from the "End Devices" section.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725194340/Screenshot_2024-09-01_143818_v2q1ml.png)

3. #### Connect the Devices:

- Select the Copper Cross-Over Cable from the "Connections" section to connect two PC at the first Switch.

- Click on PC0 and connect to the GigabitEthernet1/0/1 port on the Switch.

- Repeat the process for PC2, connecting it to the Switch GigabitEthernet1/0/2 port.

- Select the Copper Straight-Through Cable from the "Connections" section to connect the first Switch at the first Router.

- Connect the Router's GigabitEthernet0/0/0 port to the Switch's GigabitEthernet1/0/3.

- Select the Copper Cross-Over Cable from the "Connections" section to connect the two routers.

- Connect the first Router's GigabitEthernet0/0/1 at the second Router GigabitEthernet0/0/0.

- Select Copper-Straight-Through Cable from the "Connections" section to connect the second Router to the second Switch.

- Connect the second Router's GigabitEthernet0/0/1 at the second Switch's GigabitEthernet1/0/2.

- Select the Copper Cross-Over Cable from the "Connections" section to connect the second Switch to the Laptop.

- Connect the second Switch's GigabitEthernet1/0/1 at the Laptop FastEthernet0.


![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725193951/Screenshot_2024-09-01_143140_s17t5w.png)


4. #### Configure IP Addresses:

- For the PC0, PC1 and the Laptop, let check DHCP checkbox on.

    ![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725195773/Screenshot_2024-09-01_150229_i9qnvh.png)


5. #### Configure the Routers:

- Click on the Router1 and go to the CLI tab.

- Enter the following commands to configure the router:

```
Router> en
Router# conf t
Router(config)# host R1
R1(config)# int GigabitEthernet0/0/0
R1(config-if)# ip address 10.1.1.254 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# int GigabitEthernet0/0/1
R1(config-if)# ip address 8.8.8.1
R1(config-if)# exit
R1(config)# ip route 10.1.2.0 255.255.255.0 8.8.8.2
R1(config-if)# exit
R1(config)# router rip 
R1(config-router)# network 8.0.0.0
R1(config-router)# network 10.0.0.0
R1(config-router)# exit

```

- Click on the Router2 and go to the CLI tab.

- Enter the following commands to configure the router:

```
Router> en
Router# conf t
Router(config)# host R2
R2(config)# int GigabitEthernet0/0/1
R2(config-if)# ip address 10.1.2.254 255.255.255.0
R2(config-if)# no shutdown
R2(config-if)# exit
R2(config)# int GigabitEthernet0/0/0
R2(config-if)# ip address 8.8.8.2
R2(config-if)# exit
R2(config)# ip route 10.1.1.0 255.255.255.0 8.8.8.1
R2(config-if)# exit
R2(config)# router rip 
R2(config-router)# network 8.0.0.0
R2(config-router)# network 10.0.0.0
R2(config-router)# exit

```

6. Test the Connectivity:

- Go to PC1 and open the Command Prompt from the Desktop tab.

- Enter ipconfig to show the ip generated, here 10.1.1.102

- Go to Laptop and open the Command Prompt from the Desktop tab, type ping 10.1.1.102 and press enter to check the connection between the two PCs.

- You should see replies from 10.1.1.102, confirming the network is set up correctly.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1725200932/Screenshot_2024-09-01_162826_wp6mhm.png)

## Project Files

- Packet Tracer File: You can download the completed .pkt file from the repository to see the configured network.

## Troubleshooting

- No Connectivity: Ensure that the cables are connected to the correct ports and that the devices are powered on.

- Incorrect IP Address: Double-check the IP configuration on both PCs and the router.

- Router Configuration: Make sure the router interfaces are configured and not in a shutdown state.

## License
This project is licensed under the MIT License - see the LICENSE file for details.