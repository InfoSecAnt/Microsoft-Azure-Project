# Failed RDP Logon Attempts

#### [Medium Blog Step-by-Step Guide](https://anthonymendis.medium.com/fun-siem-project-for-cybersecurity-enthusiasts-be704b47add)

## Table of contents
* [Introduction](#introduction)
* [Technologies](#technologies)
* [Summary](#summary)

## Introduction
The Powershell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks. Using a third party API we will collect geographic information about the attackers location.

The script is used in this demo where I setup Microsoft Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot.
We will observe live attacks (RDP Brute Force) from all around the world. I will use a custom PowerShell script and a third-party API called IP Geolocation to look up the attackers Geolocation information and plot it on an Azure Sentinel Map to visualize our data.

<p align="center">
<img src="https://i.imgur.com/RlsG1Q7.png" height="85%" width="85%" alt="Image Analysis"/>
</p>

## Technologies
Project is created with:
* PowerShell: Extract RDP failed logon logs from Windows Event Viewer 

Utilities Used:
* ipgeolocation.io: IP Address to Geolocation conversion API

## Summary
### Attacks from Netherlands coming in; Custom logs being outputted with Geodata
<p align="center">
<img src="https://i.imgur.com/WHDhrTb.png" height="85%" width="85%" alt="Image Analysis"/>
</p>

### World map visualizing attacks after 24 hours (built custom logs including geodata)
<p align="center">
<img src="https://i.imgur.com/Qvrmfwk.png" height="85%" width="85%" alt="Image Analysis"/>
</p>
