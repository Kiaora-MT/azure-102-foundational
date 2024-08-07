---
title: "Task 4:  Configure FortiGate Policies"
weight: 4
---





Now that you have confirmed traffic from both Linux VMs is being routed to the ForitGate, you will create policies that will accomplish the security guidelines requested by company ABC.
As a reminder the following access needs to be setup for each Linux VM.

<ins>The security policy for company ABC is as follows:</ins>
- **Linux-A-VM** will be the management server.  Per company ABC security policy, it should only have SSH and PING access to **Linux-B-VM** and port 80 access to the Internet.  There should only be SSH access to **Linux-A-VM** from the Internet.

- **Linux-B-VM** is the www server.  Only port 80 services from the Internet should be allowed.  It should have 80 and 443 access to the Internet and only PING access to **Linux-A-VM**.

**Securing access for **Linux-A-VM****

In the following steps, you will create an address object, a VIP, and a Firewall Policy for **Linux-A-VM**.

- 1. From the FotiGate GUI, navigate to **Policy & Objects**, **Addresses**, and click "**+ Create new**".  
![](../Images/4-4-Azure-fgt-policy-1.PNG)

- 2. Enter the following:
        - **Name**:  "Linux-A-VM**"
        - **Interface**:  "**port2**"
        - **Type**:  "**Subnet**"
        - **IP/Netmask**:  "**192.168.1.132/32**"

Click **OK** and confirm the new address for **Linux-A-VM** is displayed.
![](../Images/4-4-Azure-fgt-policy-2.PNG)

- 3. Navigate to **Policy & Objects**, **Virtual IPs**, and click "**+ Create new**".  
![](../Images/4-4-Azure-fgt-policy-3.PNG)

- 4. Enter the following:
        - **Name**:  "Linux-A-VM_VIP**"
        - **Interface**:  "**port1**"
        - **External IP address/range**:  "**192.168.1.4**"
        - **Map to IPv4 address/range**:  "**192.168.1.132**"
        - **Port Forwarding**:  "**Enable**"
        - **External service port**:  "**22**"
        - **Map to IPv4 port**: "**22**"

Click **OK** and confirm the new VIP for **Linux-A-VM** is displayed.
![](../Images/4-4-Azure-fgt-policy-4.PNG)

- 5. Navigate to **Policy & Objects**, **Firewall Policy**, and click "**+ Create new**".
![](../Images/4-4-Azure-fgt-policy-5.PNG)

- 6. 