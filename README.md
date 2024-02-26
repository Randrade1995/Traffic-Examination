<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1 CREATE TWO VIRTUAL MACHINES USING WINDOWS AND LINUX.
- Step 2 REMOTE DESKTOP LOG INTO VM#2 AND DOWNLOAD WIRESHARK THEN START POWERSHELL APPLICATION.
- Step 3 FILTER WIRESHARK UNDER "ICMP" AND EXAMINE TRAFFIC.
- Step 4 CREATE A NETWORK SECURITY GROUP FROM AZURE AND DENY ICMP TO SEE DIFFERENCES IN TRAFFIC.

<h2>Actions and Observations</h2>

<p>
</p>
<p>

![image](https://github.com/Randrade1995/Traffic-Examination/assets/161271930/4dda857e-b7ed-45f3-979b-517142a06739)



  
While using Microsoft Azure, is it very important to create two Virtual Machines (VM) seperate lately so that the IP address are not the same. This can and will create a issue
if it is the same IP address in the future and we do not want to start over.
</p>
<br />

<p>

![image](https://github.com/Randrade1995/Traffic-Examination/assets/161271930/6207cb93-1d22-402d-a895-123dd990a023)


</p>
<p>
Remote desktop log into VM1 using the physical IP address and the same password upon creation of the virtual machine. once logged in, downloan Wireshark with all the basic settings and have Windows Powershell application loaded up and ready. 
</p>
<br />

<p>

![image](https://github.com/Randrade1995/Traffic-Examination/assets/161271930/a8b3ab73-3515-4c2e-b356-0e118ec624bf)

</p>
<p>
After loading up Wireshark, the first thing you should do it filter the search bar using "ICMP" this will show all traffic using "ICMP" should be nothing at the moment. 
</p>
<br />



![image](https://github.com/Randrade1995/Traffic-Examination/assets/161271930/c6f50a99-d19f-4098-a861-d5c4f1bd7cd9)




Create a Network Security Group from Microsoft Azure. select the correct research group that you are working on, then click on inbound security rules. create a rule for ICMP and deny all action under 200 priority.



