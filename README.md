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

- Create a Resource Group
- Set up 2 Virtual Machines, one running Windows 10 and another running Linux (Ubuntu) within Azure
    - Note: While creating the VM, select the previously created Resource Group and Virtual Network—the Virtual Network MUST BE THE SAME.
    - Ensure both VM's are on the same Virtual Network and Subnet before proceeding.
- Remote desktop into the windows 10 machine and observe ICMP traffic with wireshark
- Configure a Firewall [Network Security Group]
    - (Observe SSH Traffic)
    - (Observe DHCP Traffic)
    - (Observe DNS Traffic)
    - (Observe RDP Traffic)
- Cleanup

<h2>Actions and Observations</h2>

<p>
  
- Create a Resource group as well as 2 virtual machines in Azure. Have one machine running Windows 10 and the other machine running Linux (Ubuntu) --> (authentication type: Username/Password)
    - Refer to [this tutorial](https://github.com/MatthewThompsonIT/creating-virtual-machines) on how to create the virtual machine and resource groups if needed.
        - Note: While creating the VM, select the previously created Resource Group and Virtual Network—the Virtual Network MUST BE THE SAME.
        - Ensure both VM's are on the same Virtual Network and Subnet before proceeding.
<img src="https://i.imgur.com/w9EmWOK.png" alt="Create Virtual Machines"/>

</p>
<br />

<p>
  
- Now lets remote into the windows 10 virtual machine. [This tutorial](https://github.com/MatthewThompsonIT/creating-virtual-machines) also teaches you how to do that if needed.
- On the windows 10 VM Install [Wireshark](https://www.wireshark.org/)
  - Select NPcap 1.79, hit next, skip USBcap... then install.
<img src="https://i.imgur.com/8pkhaYc.png" alt="Install Wireshark"/>
    
- Run Wireshark, start a packet capture( hit the green arrow) and begin a filter for ICMP traffic only
    - In the "filter" bar at the top enter in icmp
        - The results should be nothing for now
<img src="https://i.imgur.com/jE1q9y9.png" alt="icmp traffic"/>

- Retrieve the private IP address of the Ubuntu VM (linux-vm) and attempt to ping it from within the Windows 10 VM
  - This can be found under the Overview tab when selecting the linux-vm
<img src="https://i.imgur.com/iYHsF3U.png" alt="get ip"/>
</p>
<p>
  


</p>
<br />

<p>


</p>
<p>
  
<img src="" alt=""/>
</p>
<br />
