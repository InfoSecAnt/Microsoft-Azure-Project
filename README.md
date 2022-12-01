# Microsoft-Azure-Project

<h1>Failed RDP to IP Geolocation Information</h1>


 ## [Medium Demonstration](https://anthonymendis.medium.com/fun-siem-project-for-cybersecurity-enthusiasts-be704b47add)


<h2>Description</h2>
<b>The Powershell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks. Using a third party API we will collect geographic information about the attackers location.
</b>
<br />
<br />
The script is used in this demo where I setup Microsoft Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot.
We will observe live attacks (RDP Brute Force) from all around the world. I will use a custom PowerShell script and a third-party API called IP Geolocation to look up the attackers Geolocation information and plot it on an Azure Sentinel Map to visualize our data.
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/RlsG1Q7.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from Netherlands coming in; Custom logs being output with geodata</h2>

<p align="center">
<img src="https://i.imgur.com/WHDhrTb.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<h2>World map visualizing attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/Qvrmfwk.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
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
