
<p align="center">
  <img src="https://i.imgur.com/Ua7udoS.png" height="80%" width="80%" alt="Ubuntu VM" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />




<h2>Environments and Technologies Used</h2>

* Microsoft Azure (Virtual Machines/Compute)
* Remote Desktop
* Various Command-Line Tools
* Various Network Protocols (ICMP, SSH, DHCP, DNS, RDP)
* Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

* Windows 10 (21H2)
* Ubuntu Server 20.04

<h2>High-Level Steps</h2>

* Create Resources
* Observe ICMP Traffic
* Observe SSH Traffic
* Observe DHCP Traffic
* Observe DNS Traffic
* Observe RDP Traffic




<p>
<img src="https://i.imgur.com/Pr1qH2d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1 create the resources for lab, the First VM using Windows Pro
</p>
<br />

<p>
<img src="https://i.imgur.com/4R7MSCn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create Second VM using Linux
</p>
<br />

<p>

  
<p>
<img src="https://i.imgur.com/jwBzDep.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3 navigate to network watcher and verify that VM1 and VM2 Exist on the same network
</p>
<br />

<p>
<img src="https://i.imgur.com/arjwgjb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4 Using Remote Desktop Login to VM1
</p>
<br />

<p>




