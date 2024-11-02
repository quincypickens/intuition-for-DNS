<p align="center">
<img src="https://i.imgur.com/PVSIB2I.png" alt="DNS" height="40%" width="40%"/>
</p>

<h1>Building an Intuition for DNS </h1>
Various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Step One:</h2>
- Connect/log into DC-1 as your domain admin account (mydomain.com\jane_admin).<br />
- Connect/log into Client-1 as an admin (mydomain\jane_admin)
- dc-1 --> Forward Lookup Zones-->mydomain.com-->right click---New Host (A or AAAA) <br />
<h3>Step Two:</h3>
- Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address.<br />
- Go to Start menu--> Windows Administrative Tools --> DNS <br />
- 
- Go back to Client-1 and try to ping it. Observe that it works




