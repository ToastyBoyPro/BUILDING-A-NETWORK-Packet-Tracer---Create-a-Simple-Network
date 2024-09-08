# BUILDING-A-NETWORK-Packet-Tracer---Create-a-Simple-Network
Building a Network - Activity 2

## Objective

The purpose of this activity is to guide you through building a simple network using Packet Tracer in the Logical Workspace. This will involve two main tasks: 
1) Constructing the network
2) Configuring the end devices and verifying their connectivity.

### Skills Learned

- Deployment and connection of network devices in the Logical Workspace.
- Customization of display names for network devices.
- Configuration of end devices and verification of connectivity.

### Tools Used

- Cisco Packet Tracer

## Steps

### 1. Build a Simple Network
Build a simple network by deploying and connecting the network devices in the Logical Workspace.

1. Add a PC, laptop, and a cable modem to the Logical Workspace.

2. Change the display names of the network devices in the Config tab to: PC, Laptop, and Cable Modem.

    <img src="https://github.com/user-attachments/assets/595e0dba-48a7-495f-a7c9-e7108c9d8673" 
    alt="Network Layout"
    width="525" height="225"> <br>
    *Ref 1: Network Layout*.

> A **cable modem** is a hardware device that allows communications with an Internet Service Provider (ISP). The coaxial cable from the ISP is connected to the cable modem, which is connected to the local network through an ethernet cable. The cable modem converts the coaxial connection to an Ethernet connection.

3.  Add the physical cabling between devices on the workspace.

      1. Attach a copper straight-through cable to the FastEthernet0 interface of the PC and the Ethernet 1 interface of the wireless router.

      2. Attach a copper straight-through cable to the internet interface of the wireless router and the Port 1 interface of the cable modem.

      3. Attach a coaxial cable to the Port 0 interface of the cable modem and the Coaxial 7 interface of the internet cloud.

    <img src="https://github.com/user-attachments/assets/c3dde095-bf3b-4ee1-aa92-31409d349b29"
    alt="Network Device Connections"
    width="528" height="223"> <br>
    *Ref 2: Network Device Connections*.

### 2. Configure the End Devices and Verify Connectivity
Connect to the Wireless Router with a PC using an Ethernet cable and with a laptop after replacing the wired Ethernet network interface card (NIC) with a wireless NIC.
Verify connectivity to *cisco.srv* and check that the PC and the Laptop are assigned an IP (Internet Protocol) address. 

> **Internet Protocol** is a set of rules for routing and addressing data on the internet. **IP addresses** are used to identify the devices on a network and allow the devices to connect and transfer data on a network.

> The **subnet mask** is used to differentiate the host and the network ID portion of the IP address. You can relate the IP address to your street address. The network ID part of the address is your street, 192.168.0. The house number is the host port of the IP address. For the IP address 192.168.0.2, the house number is 2 and the street is 192.168.0. If there is more than one house on the same street, for example, house number 3, will have an address 192.168.0.3. The maximum number of houses on this street is 253, ranging from 2 to 254.

1. Click the PC and navigate to IP Configuration in the Desktop tab to verify that DHCP is enabled and the PC has received an IP address. 

2. Select DHCP for the IP Configuration heading if you do not see an IP address for the IPv4 Address field. 

3. Observe the process as the PC is receiving an IP address from the DHCP server.

    <img src="https://github.com/user-attachments/assets/be3d5a5e-8833-4616-9e10-c3311e48dfa4"
    alt="Configuring the IP for PC"
    width="306" height="270"> <br>
    *Ref 3: Configuring the IP for PC*.

> **DHCP** stands for dynamic host configuration protocol. This protocol assigns IP addresses to devices dynamically. In this simple network, the Wireless Router is configured to assign IP addresses to devices that request IP addresses. If DHCP is disabled, you will need to assign an IP address and configure all the necessary information to communicate with other devices on the network and the internet.

4. Close IP Configuration and in the Desktop tab, click Command Prompt.

5. At the prompt, enter  `ipconfig /all` to review the IPv4 addressing information from the DHCP server. The PC should have received an IPv4 address in the 192.168.0.x range.

    <img src="https://github.com/user-attachments/assets/c38b3c33-c166-435a-9358-898f90ae92de"
    alt="IPv4 Assignment Verification"
    width="344" height="286"> <br>
    *Ref 4: IPv4 Assignment Verification*.

> **Note**: There are two types of IP addresses: IPv4 and IPv6. An **IPv4 (internet protocol version 4)** address is a string of numbers in the form of x.x.x.x. IP addresses for the end devices can range from 192.168.0.2 to 192.168.0.254. **IPv6 (internet protocol version 6)** was introduced in the late 1990s to address the  growing internet and limitations of IPv4. The details of IPv6 addressing are beyond the scope of this activity. Each NIC will get a unique IP address in the same network.

6. Test connectivity to the *cisco.srv* from the PC. From the command prompt, issue the command `ping cisco.srv`. It may take a few seconds for the ping to return. Four replies should be received.

    <img src="https://github.com/user-attachments/assets/749a226f-e5f6-44e6-9293-bab6ec09027b"
    alt="Pinging the Cisco Server"
    width="439" height="444"> <br>
    *Ref 5: Pinging the Cisco Server*.

7. In the Laptop, replace the wired Ethernet network interface card (NIC) with a wireless NIC.
   
      1. Click Laptop, and select the Physical tab.

      2. Power off Laptop by clicking the power button on the side of the laptop.

      3. Remove the currently installed Ethernet copper module by clicking on the module on the side of the laptop and dragging it to the MODULES pane on the left of the laptop window.

      4. Install the wireless WPC300N module by clicking it in the MODULES pane and dragging it to the empty module port on the side of the Laptop.

      5. Power on the Laptop by clicking the Laptop power button again.

8. With the wireless module installed, connect the Laptop to the wireless network.
   
      1. Click the Desktop tab and select the PC Wireless.

      2. Select the Connect tab. After a slight delay, the wireless network *HomeNetwork* will be visible in the list of wireless networks. Click Refresh if necessary to see the list of available networks. Select the *HomeNetwork* and click Connect.

    <img src="https://github.com/user-attachments/assets/bc4bb8da-b043-4efe-982a-e5eb307fe3bc"
    alt="Connecting to the Wireless Network"
    width="303" height="193"> <br>
    *Ref 6: Connecting to the Wireless Network*.

9. Close PC Wireless. Select Web Browser in the Desktop tab.

10. In the Web Browser, navigate to *cisco.srv*.

    <img src="https://github.com/user-attachments/assets/c582fe1e-253e-485c-b024-507ee69271e6"
    alt="Navigating to the Cisco Site"
    width="521" height="239"> <br>
    *Ref 7: Navigating to the Cisco Site*.

> The **default gateway** is analogous to the street intersection. The traffic from the 192.168.0 street has to exit through the intersection to another street. Another street is another network. In this network, default gateway is the wireless router that directs the traffic from the local network to the cable modem, and the traffic is then sent to the ISP.
