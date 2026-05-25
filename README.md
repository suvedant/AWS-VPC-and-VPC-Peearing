# AWS VPC Peering Project (Hands-On Lab)
"This repository documents an AWS infrastructure project demonstrating a secure multi-VPC network design. It details the configuration of public and private subnets, outbound internet connectivity via NAT Gateways, and secure cross-VPC communication using peering connections. 

**Creating VPC Network**
Step 1: Create the VPC
What it does: You are carving out an isolated, private virtual network inside AWS just for your resources.
Key Action: You define an IP range (e.g., 10.0.0.0/16), which acts as the "master pool" of IP addresses for everything inside this network.

**Step 2: Configure Subnets**
What it does: You split your large VPC network into smaller, manageable chunks called subnets.
Key Action: * Public Subnets: Designed for web servers or gateways that face the public.
Private Subnets: Designed for backend databases and applications that must stay hidden from the internet.

**Step 3: Configure Gateways (Internet & NAT)** 
What it does: This step creates the "doors" for traffic to enter and exit your network.
Key Action:
Internet Gateway (IGW): A two-way door attached to the VPC allowing direct public internet access.
NAT Gateway: A one-way security door placed in the public subnet. It allows private resources to securely download updates from the internet without allowing outsiders to initiate a connection inside.

**Step 4: Route Tables (The Traffic Police)**
What it does: Route tables contain a set of rules (routes) that determine where network traffic is directed.
Key Action: * The Public Route Table sends internet traffic ($0.0.0.0/0$) straight to the Internet Gateway.
The Private Route Table sends internet traffic ($0.0.0.0/0$) straight to the NAT Gateway.


<img width="1201" height="1016" alt="diagram-export-5-25-2026-12_06_46-PM" src="https://github.com/user-attachments/assets/8efef389-4ccf-4446-94ac-f0c15343d1fa" />


