
# Lab - Mapping the Internet

## Part 1: Test Network Connectivity Using Ping

To trace the route to a distant network, the PC used must have a working connection to the Internet.

- The first tool we will use is ping. Ping is a tool used to test whether a host is reachable. Packets of information are sent to the remote host with instructions to reply. Your local PC measures whether a response is received to each packet, and how long it takes for those packets to cross the network. The name ping comes from active sonar technology in which a pulse of sound is sent underwater and bounced off of terrain or other ships.

- From Windows, press Windows Button + R, type powershell in the Search box, and then press Enter

- At the command-line prompt, type ping www.cisco.com

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724663150/Screenshot_2024-08-26_104828_a05u4g.png)

## Part 2: Trace a Route to a Remote Server Using Tracert

Now that basic reachability has been verified by using the ping tool, it is helpful to look more closely at each
network segment that is crossed. To do this, the tracert tool will be used.

- At the command-line prompt, type tracert www.cisco.com.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724663150/Screenshot_2024-08-26_104925_ilf7hc.png)

## Part 3: Trace a Route to a Remote Server Using Web-Based

- Using https://traceroute-online.com/ and trace the route to the following website: www.cisco.com 

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724663152/Screenshot_2024-08-26_105611_ritdsy.png)

