
<p align="center">
  <img src="https://i.imgur.com/Ua7udoS.png" height="80%" width="80%" alt="Ubuntu VM" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this lab, we observe network traffic to and from Azure Virtual Machines using Wireshark. We also experiment with using Network Security Groups. <br />




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

<h3 align="center">
  Set Up VM Environment
</h3>



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


<p>
<img src="https://i.imgur.com/k7nP9Pk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5 download wireshark in VM1
</p>
<br />

<p>
<img src="https://i.imgur.com/3TYIfSu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6 open wirehark and ping VM2
</p>
<br />

<p>


<p>
<img src="https://i.imgur.com/Rp6kyUa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 7 ping w w w .google. com in wireshark
</p>
<br />

<p>
<img src="https://i.imgur.com/JumuMuH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 8 ping perpetually by using ping the linux VMs private IP (10.0.0.5) in powershell
</p>
<br />

<p>


<p>
<img src="https://i.imgur.com/zyhGuw7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 9 Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic, while back in the Windows 10 VM, observe the ICM
</p>
<br />

<p>
<img src="https://i.imgur.com/IAP8UyI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 10 Create A new rule that denies ICMP traffic
</p>
<br />

<p>
Step 11 verify that ICMP traffic is now being blocked

<p>
<img src="https://i.imgur.com/zTj8xJT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 12 back in azure switch the new rule from deny to allow
</p>
<br />

<h3 align="center">
  Observe SSH traffic
</h3>

<p>
<img src="https://i.imgur.com/OyzdcEt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 13 In powershell connect to vm2 via ssh. Then analyze wireshark's display of ssh information 
</p>
<br />

<p>


<p>
<img src="https://i.imgur.com/KD9kUcX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/PeBVtmE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>




<p>
<img src="https://i.imgur.com/Tzop6r8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 16 type linux commands to verify access to terminal
</p>
<br />

<p>
<img src="https://i.imgur.com/kkAtmbT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3 align="center">
 Observe DHCP Information
</h3>


<p>
Step 17 reasign dhcp and analyse the information in wireshark
</p>
<br />

<p>


<p>
<img src="https://i.imgur.com/jNp6biz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3 align="center">
 Observe DNS Traffic
</h3>


<p>
Step 18 analyse the dns traffic after using the nslookup command
</p>
<br />

<p>
<img src="https://i.imgur.com/Poi2CMh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3 align="center">
  Observe RDP traffic
</h3>


<p>
Step 19 Lastly, check RDP or TCP  port 3389 and observe the continuous stream of traffic due to the use of the remote desktop viewer
</p>
<br />

<p>



