<h1>OPNSense Firewall Lab Project</h1>



<h2>Description</h2>
This project consists of implementing a secure network that features an Intrustion Detection and Prevention System for a fictional company, leveraging OPNSense Firewall, Windows Server, Ubuntu Server, and Active Directory. Elasticsearch stack will be utilized as our threat hunting and monitoring solution. All of this will be virtualized using VMware VirtualBox.
<br />


<h2>Programs and Utilities Used</h2>

- <b> OPNSense Firewall </b> 
- <b> Active Directory </b>
- <b> Elastic Search </b>


<h2>Environments Used </h2>

- <b> Kali Linux </b>
- <b> Oracle VM VirtualBox </b>
- <b> Windows Server </b>
- <b> Ubuntu Server </b>

<h2>Virtual Box Setup:</h2>

<p align="center">
<b> 1. </b> Inside of VM VirtualBox, install OPNSense, and Kali Linux ISOs. <b>Be sure to select Free BSD (64-bit) when installing the OPNSense ISO:</b> <br/>
 
<img src="https://i.imgur.com/V1KM0oj.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/>
<img src="https://i.imgur.com/W1lUjc5.png" height="80%" width="80%" alt="OPNSense Firewall Steps"/>
<br/> 
I assigned 2 cores, 2048 MB of RAM, and 16 GB of disk space to each Virtual Machine.
<br />
<br />
<br />
<b> 2. </b> Set Network settings for each VM to have 2 adapters: NAT and Internal Network, since we are going to be running this in a local networking configuration. <br/> 
<img src="https://imgur.com/jan3Usu.png" height="50%" width="50%" alt="OPNSense Firewall Steps"/>
<img src="https://i.imgur.com/RgFSFlW.png" height="50%" width="50%" alt="OPNSense Firewall Steps"/>
<br />
<br />
</p>


<h2>Setting up OPNSense</h2>
<p align="center">
<b> 1. </b> Start the OPNSense VM. Mount the OPNSense Firewall ISO and follow through with the Installation Wizard. Install UFS. <br/>
<img src="https://imgur.com/gwsCYln.png" height="50%" width="50%" alt="OPNSense Firewall Steps"/>
<br />
<br />
<b> 2. </b> Rewrite contents of ada0 (our VBOX HARDDISK) and confirm. This will format the disk and its contents to have the OPNSense Firewall Image installed on the VM.<br/>
 <img src="https://i.imgur.com/oh6tPC8.png" height="50%" width="50%" alt="OPNSense Firewall Steps"/>
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
