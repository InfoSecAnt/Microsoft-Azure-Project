# Failed RDP Logon Attempts

#### [Step-by-Step Guide on Medium](https://anthonymendis.medium.com/fun-siem-project-for-cybersecurity-enthusiasts-be704b47add)

## Table of contents
* [Introduction](#introduction)
* [Technologies](#technologies)
* [Conclusion](#conclusion)

## Introduction
The PowerShell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks. Using a third party API we will collect geographic information about the attackers location.

I will be setting up Microsoft Sentinel (SIEM) and connecting it to a live virtual machine acting as a honey pot. We will observe incoming RDP Brute Force attacks from around the world. I will then use a [custom PowerShell script](https://github.com/anthonymendis/Microsoft-Azure-Project/blob/main/Powershell_Script_Security_Log.ps1) and a third-party API called IP Geolocation to look up the attacker's geolocation information and plot it on an Azure workbooks map to visualize the data.

<p align="center">
<img src="https://i.imgur.com/RlsG1Q7.png" height="85%" width="85%" alt=""/>
</p>

## Technologies
Project is created with:
* PowerShell: Extracts all 'EventID=4625' events from Windows Event Viewer and documents vital information about the attackers failed attempt at logging on

Utilities used:
* ipgeolocation.io: IP Address to Geolocation conversion API

## Conclusion
### Attacks from Netherlands coming in; Custom logs being outputted with Geodata
<p align="center">
<img src="https://i.imgur.com/WHDhrTb.png" height="85%" width="85%" alt=""/>
</p>

### World map visualizing attacks after 24 hours (Built custom logs including Geodata)
<p align="center">
<img src="https://i.imgur.com/Qvrmfwk.png" height="85%" width="85%" alt=""/>
</p>
