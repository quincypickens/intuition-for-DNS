<p align="center">
<img src="https://i.imgur.com/PVSIB2I.png" alt="DNS" height="40%" width="40%"/>
</p>

<h1>Building an Intuition for DNS </h1>
Various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Step One:</h2
               
- Connect/log into DC-1 as your domain admin account (mydomain.com\jane_admin).<br />
- Connect/log into Client-1 as an admin (mydomain\jane_admin) <br />

<h3>Step Two:</h3>

- Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address.<br />
- Go to Start menu--> Windows Administrative Tools -->DNS-->
- dc-1 -->Forward Lookup Zones-->mydomain.com-->right click---New Host (A or AAAA)--> Add New Host <br /> 

<img src="https://i.imgur.com/keSqBzZ.png" height="50%" width="50%" alt="DNS"/> <img src="https://i.imgur.com/thobYEF.png" height="50%" width="50%" alt="DNS"/>

- Go back to Client-1 and try to ping it. Observe that it works.

<h4>Step Three:</h4>

- Go back to DC-1 and change mainframe’s record address to 8.8.8.8
     - Double click to change IP
 
<img src="https://i.imgur.com/vAGAbfs.png" height="60%" width="60%" alt="DNS"/>

- Go back to Client-1 and ping “mainframe” again. Observe that it still pings the old address
- Observe the local dns cache (ipconfig /displaydns)
- Flush DNS cache/ Observe as empty
- Ping mainframe

<img src="https://i.imgur.com/CyJ5Awh.png" height="60%" width="60%" alt="DNS"/>

<h5>Step Four:</h5>

- Go back to DC-1 and create a CNAME record that points the host “search” to “www.google.com”
- Go back to Client-1 and attempt to ping “search”, observe the results of the CNAME record
- On Client-1, nslookup “search”, observe the results of the CNAME record







