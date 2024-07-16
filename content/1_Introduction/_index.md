---
title: "Introduction"
weight: 5
---

# FortiGate: Protecting Azure vNET Traffic Flows

## Learning Objectives

Upon completion of this workshop, you will gain understanding of the following objectives:
  
  * Azure Networking Concepts *(10 minutes)*
  * Azure Architecture Concepts *(10 minutes)*
  * FortiGate FortiOS terminology *(10 minutes)*
  * Creating & applying Firewall policies with security profiles & objects to control traffic flows *(10 minutes)*
  * Testing traffic flows to validate the implemented networking and security controls *(20 minutes)*

## Workshop Components

Fortinet & Azure components used during this workshop:

  * Azure Fsv2 series instances running a FortiGate NVA
  * Azure DsV4 series instances running Ubuntu Linux OS as the testing workloads
  * Azure Networking Components:
    * Virtual Network (vNET)
    * Subnets
    * NAT Gateway
    * User-defined Route Table (UDR)

## Azure Reference Architecture Diagram

  * Azure networking offers multiple ways to organize your Azure architecture to take advantage of FortiGate traffic inspection.  Most importantly, traffic must follow a symmetrical routing path (for forward and reverse flows). As long as flows are symmetrical, the architecture will work and traffic will flow through FortiGate NGFW for inspection.
  * We will investigate the configuration of the different architecture patterns below:
    - **Traffic flows in a single VNET without a FortiGate NVA - Unsecured VNET**
    - **Inspection of traffic flows in a single VNET with a FortiGate NVA - Secured VNET**

![](../Images/Azure-Unsecured-VNET.png)
![](../Images/Azure-Secured-VNET.PNG)
