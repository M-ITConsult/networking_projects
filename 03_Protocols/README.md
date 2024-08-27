# Packet Tracer - Investigating the TCP/IP and OSI Models in Action

Objectives

- Part 1: Examine HTTP Web Traffic

- Part 2: Display Elements of the TCP/IP Protocol Suite

Background

This simulation activity is intended to provide a foundation for understanding the TCP/IP protocol suite and the relationship to the OSI model. Simulation mode allows you to view the data contents being sent across the network at each layer.

As data moves through the network, it is broken down into smaller pieces and identified so that the pieces can be put back together when they arrive at the destination. Each piece is assigned a specific name (protocol data unit [PDU]) and associated with a specific layer of the TCP/IP and OSI models. Packet Tracer simulation mode enables you to view each of the layers and the associated PDU. The following steps lead the user through the process of requesting a web page from a web server by using the web browser application available on a client PC.

Even though much of the information displayed will be discussed in more detail later, this is an opportunity to explore the functionality of Packet Tracer and be able to visualize the encapsulation process.

## Part 1:     Examine HTTP Web Traffic

In Part 1 of this activity, you will use Packet Tracer (PT) Simulation mode to generate web traffic and examine HTTP.

### Step 1:     Switch from Realtime to Simulation mode.

In the lower right corner of the Packet Tracer interface are tabs to toggle between Realtime and Simulation mode. PT always starts in Realtime mode, in which networking protocols operate with realistic timings. However, a powerful feature of Packet Tracer allows the user to “stop time” by switching to Simulation mode. In Simulation mode, packets are displayed as animated envelopes, time is event driven, and the user can step through networking events.

- Click the Simulation mode icon to switch from Realtime mode to Simulation mode.

- Select HTTP from the Event List Filters.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_093833_hiv8e5.png)

- HTTP may already be the only visible event. Click Edit Filters to display the available visible events. Toggle the Show All/None check box and notice how the check boxes switch from unchecked to checked or checked to unchecked, depending on the current state.

- Click the Show All/None check box until all boxes are cleared and then select HTTP. Click anywhere outside of the Edit Filters box to hide it. The Visible Events should now only display HTTP.

### Step 2:     Generate web (HTTP) traffic.

Currently the Simulation Panel is empty. There are six columns listed across the top of the Event List within the Simulation Panel. As traffic is generated and stepped through, events appear in the list. The Info column is used to inspect the contents of a particular event.

Note: The Web Server and Web Client are displayed in the left pane. The panels can be adjusted in size by hovering next to the scroll bar and dragging left or right when the double-headed arrow appears.

- Click Web Client in the far left pane.

- Click the Desktop tab and click the Web Browser icon to open it.

- In the URL field, enter www.osi.local and click Go.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746411/Screenshot_2024-08-27_094142_u5pjwa.png)

Because time in Simulation mode is event-driven, you must use the Capture/Forward button to display network events.

- Click Capture/Forward four times. There should be four events in the Event List.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746411/Screenshot_2024-08-27_094150_hfeeki.png)


### Step 3:     Explore the contents of the HTTP packet.

- Click the first colored square box under the Event List > Info column. It may be necessary to expand the Simulation Panel or use the scrollbar directly below the Event List.

The PDU Information at Device: Web Client window displays. In this window, there are only two tabs (OSI Model and Outbound PDU Details) because this is the start of the transmission. As more events are examined, there will be three tabs displayed, adding a tab for Inbound PDU Details. When an event is the last event in the stream of traffic, only the OSI Model and Inbound PDU Details tabs are displayed.

- Ensure that the OSI Model tab is selected. Under the Out Layers column, ensure that the Layer 7 box is highlighted.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746411/Screenshot_2024-08-27_094719_kz1ua4.png)

What information is listed in the numbered steps directly below the In Layers and Out Layers boxes?

- Click Next Layer. Layer 4 should be highlighted. 

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746411/Screenshot_2024-08-27_094702_q7haak.png)

- Click Next Layer. Layer 3 should be highlighted. What is the Dest. IP value? 

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_094708_xjrjh5.png)

- Click Next Layer. What information is displayed at this layer?

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_094708_xjrjh5.png)

- Click the Outbound PDU Details tab.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_094748_ejnh0n.png)

Information listed under the PDU Details is reflective of the layers within the TCP/IP model.

Note: The information listed under the Ethernet II section provides even more detailed information than is listed under Layer 2 on the OSI Model tab. The Outbound PDU Details provides more descriptive and detailed information. The values under DEST MAC and SRC MAC within the Ethernet II section of the PDU Details appear on the OSI Model tab under Layer 2, but are not identified as such.

- Click the next colored square box under the Event List > Info column. Only Layer 1 is active (not grayed out). The device is moving the frame from the buffer and placing it on to the network.

- Advance to the next HTTP Info box within the Event List and click the colored square box. This window contains both In Layers and Out Layers. Notice the direction of the arrow directly under the In Layers column; it is pointing upward, indicating the direction the information is travelling. Scroll through these layers making note of the items previously viewed. At the top of the column the arrow points to the right. This denotes that the server is now sending the information back to the client.

Comparing the information displayed in the In Layers column with that of the Out Layers column, what are the major differences?

- Click the Outbound PDU Details tab. Scroll down to the HTTP section.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_095036_wedi5m.png)

What is the first line in the HTTP message that displays?

- Click the last colored square box under the Info column. How many tabs are displayed with this event and why?

## Part 2:     Display Elements of the TCP/IP Protocol Suite

In Part 2 of this activity, you will use the Packet Tracer Simulation mode to view and examine some of the other protocols comprising of the TCP/IP suite.

### Step 1:     View Additional Events

- Close any open PDU information windows.

- In the Event List Filters > Visible Events section, click Show All.

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_095708_hj34wj.png)

These extra entries play various roles within the TCP/IP suite. If the Address Resolution Protocol (ARP) is listed, it searches MAC addresses. DNS is responsible for converting a name (for example, www.osi.local) to an IP address. The additional TCP events are responsible for connecting, agreeing on communication parameters, and disconnecting the communications sessions between the devices. These protocols have been mentioned previously and will be further discussed as the course progresses. Currently there are over 35 possible protocols (event types) available for capture within Packet Tracer.

- Click the first DNS event in the Info column. Explore the OSI Model and PDU Detail tabs and note the encapsulation process. As you look at the OSI Model tab with Layer 7 highlighted, a description of what is occurring is listed directly below the In Layers and Out Layers (“1. The DNS client sends a DNS query to the DNS server.”). This is very useful information to help understand what is occurring during the communication process.

- Click the Outbound PDU Details tab. What information is listed in the NAME: in the DNS QUERY section?

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_095932_cnyww6.png)

- Click the last DNS Info colored square box in the event list. Which device is displayed?

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_100141_zkydud.png)

What is the value listed next to ADDRESS: in the DNS ANSWER section of the Inbound PDU Details?

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_100236_kc2lzz.png)

- Find the first HTTP event in the list and click the colored square box of the TCP event immediately following this event. Highlight Layer 4 in the OSI Model tab. In the numbered list directly below the In Layers and Out Layers, what is the information displayed under items 4 and 5?

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_100425_mlrkkv.png)

TCP manages the connecting and disconnecting of the communications channel along with other responsibilities. This particular event shows that the communication channel has been ESTABLISHED.

- Click the last TCP event. Highlight Layer 4 in the OSI Model tab. Examine the steps listed directly below In Layers and Out Layers. What is the purpose of this event, based on the information provided in the last item in the list (should be item 4)?

![Alt text](https://res.cloudinary.com/dceb4nzy9/image/upload/v1724746412/Screenshot_2024-08-27_100711_i2kcs4.png)