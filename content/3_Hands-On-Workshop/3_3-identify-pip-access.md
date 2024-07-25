---
title: "Task 3 - identify assigned public IP (PIP), access to the Internet, and access between VMs."
weight: 3
---





Now that you have created the virtual machines, **Linux-A-VM** and **Linux-B-VM**, you are going to identify their assigned public IP (PIP), confirm access to the Internet, and connectivity between each VM via their assigned subnets.

 Access the serial console of both virthal machines in differant tabs.

- 1. Navigate into your Resource Group and right click on the virtual machine **Linux-A-VM**.  Select **Open Link in New Tab**  
![](../Images/Azure-identify-pip-access.PNG)  
    
You will see the **Linux-A-VM** Overview page in a new tab.

- 2. Under the **Essentials** and **Properties** sections, right hand side, identify the assigned private and public IP of **Linux-A_VM**
        - Navigate to the bottom left of the screen, expand the **Help** menu, and select **Serial console**.
![](../Images/Azure-identify-pip-access1.PNG)

You will be redirected to the **Linux-A-VM | Serial Console** screen.

- 3. Login to the **Linux-A-VM** console using the credentials you used when creating the **Linux-A-VM**.
![](../Images/Azure-identify-pip-access2.PNG)

- 4. Return to the **studentxx-azure102-rg** tab and right click on the virtual machine **Linux-B-VM**.  Select **Open Link in New Tab**  

You will see the **Linux-B-VM** Overview page in a new tab.

- 5. Under the **Essentials** and **Properties** sections, right hand side, identify the assigned private and public IP of **Linux-B-VM**
        - Navigate to the bottom left of the screen, expand the **Help** menu, and select **Serial console**.

You will be redirected to the **Linux-B-VM | Serial Console** screen.

- 6. Login to the **Linux-B-VM** console using the credentials you used when creating **Linux-B-VM**.

- 7. From the **Linux-A-VM** CLI:
        - Ping "**www.yahoo.com**" and confirm replies.
        - Confirm the public IP assigned to **Linux-A-VM**: "**curl https://ipinfo.io/ip**"
        - Confirm access to a website:  "**wget www.fortinet.com**"
        - Ping the private IP of **Linux-B-VM** and confirm replies.
        - Scan open ports on **Linux-B-VM via xx:  "**xx**"
        - Confirm access to **Linux-B-VM** via SSH:  **ssh studentxx@192.168.1.xxx

- 8. From the **Linux-B-VM** CLI:
        - Ping **www.yahoo.com** and confirm replies.
        - Confirm the public IP assigned to **Linux-B-VM**: "**curl https://ipinfo.io/ip**"
        - Ping the private IP of **Linux-A-VM** and confirm replies.
        - Confirm access to **Linux-A-VM** via SSH.  **ssh studentxx@192.168.1.xxx

What do steps 7 and 8 above tell you about access to/from the Internet to both Linux VMs?
What do steps 7 and 8 above tell you about access between each Linux VM in different subnets?
