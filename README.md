<h1>OPNSense Firewall Lab Project</h1>



<h2>Description</h2>
This project consists of implementing a secure network that features an Intrustion Detection and Prevention System for a fictional company. In this project, we are going to be leveraging OPNSense Firewall, Windows Server, Ubuntu Server, and Active Directory. Elasticsearch stack will be utilized as our threat hunting and monitoring solution. All of this will be virtualized using VMware VirtualBox.
<br />


<h2>Programs and Utilities Used</h2>

- <b> [OPNSense Firewall](https://opnsense.org/download/) </b>
- <b> [Windows Active Directory](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/get-started/virtual-dc/active-directory-domain-services-overview) </b>
- <b> [Elastic Search](https://www.elastic.co/elastic-stack) </b>


<h2>Environments Used </h2>

- <b> [Kali Linux](https://www.kali.org/get-kali/#kali-virtual-machines) </b>
- <b> [Oracle VM VirtualBox](https://www.virtualbox.org/) </b>
- <b> Windows Server </b>
- <b> Ubuntu Server </b>

<h2>Virtual Box Setup</h2>

<p align="center">
<b> 1. </b> Inside of VM VirtualBox, install OPNSense, and Kali Linux ISOs.  <br/>
 
<img src="https://i.imgur.com/V1KM0oj.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/>
<br/>
<b>Be sure to select Free BSD (64-bit) when installing the OPNSense ISO:</b>
<img src="https://i.imgur.com/W1lUjc5.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/>
<br/> 
I assigned 2 cores, 2048 MB of RAM, and 16 GB of disk space to each Virtual Machine.
<br />
<br />
<br />
<b> 2. </b> Set Network settings for both of the Kali Linux and OPNSense VMs to have 2 adapters: NAT and Internal Network. We are going to be running this in a local networking configuration that allows our Virtual Machines to communicate with eachother. <br/> 
<img src="https://imgur.com/jan3Usu.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/>
<img src="https://i.imgur.com/RgFSFlW.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/>
<br />
<br />
</p>


<h2>Setting up OPNSense</h2>
<p align="center">
<b> 1. </b> Start the OPNSense VM. Mount the OPNSense Firewall ISO and follow through with the Installation Wizard. Install UFS. <br/>
<img src="https://imgur.com/gwsCYln.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/>
<br />
<br />
<b> 2. </b> Rewrite contents of ada0 (our VBOX HARDDISK) and confirm. This will format the disk and its contents to have the OPNSense Firewall Image installed on the VM.<br/>
 <img src="https://i.imgur.com/oh6tPC8.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/>
 <br />
 <br />
 <b> 3. </b> Assign interfaces for LAN and WAN. em0 for LAN and em1 for WAN. I left each interface IP as the default (192.168.1.1/24 and 10.0.2.15/24)<br/>
 <img src="https://i.imgur.com/MAR6WGB.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/><br />
 
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
