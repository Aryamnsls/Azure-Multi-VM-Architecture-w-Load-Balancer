# Azure-Multi-VM-Architecture-w-Load-Balancer
Azure Multi-VM Architecture w/ Load Balancer

Project Summary
Designed and deployed a scalable, highly available web architecture using Azure Load Balancer to distribute traffic across both Windows and Linux virtual machines, each serving distinct web content. Demonstrated real-world skills in infrastructure provisioning, load balancing, network security, port mapping, and cross-platform server configuration.
________________________________________
🔧 Tech Stack
Category	Tools / Technologies
Cloud Platform	Microsoft Azure
Compute	Azure Virtual Machines (Linux & Windows)
Networking	Azure Public Load Balancer, NSG, VNet
Web Servers	IIS (Windows), Apache2 (Linux)
OS Used	Windows Server 2019, Ubuntu 20.04 LTS
Access	RDP, SSH, Azure Cloud Shell
Scripting	PowerShell, Bash
Monitoring	Azure Health Probes
________________________________________
🧱 Key Features & Implementation Steps
1.	Infrastructure Setup
o	Created a Windows VM with IIS Web Server hosting a custom HTML page.
o	Created a Linux VM (Ubuntu 20.04) with Apache2 serving a different HTML page.
o	Both VMs were deployed under the same Virtual Network and Subnet.
2.	Web Server Configuration
o	Configured Windows VM to serve content using IIS via port 80.
o	Configured Linux VM to serve content using Apache2 via port 80.
o	Added personalized HTML content to verify source machine when accessed.
3.	Load Balancer Setup
o	Created an Azure Public Load Balancer to handle traffic on port 80.
o	Configured a Backend Pool and added both VM NICs.
o	Created a Health Probe to monitor HTTP (TCP 80) response.
o	Created a Load Balancing Rule to forward frontend traffic to backend VMs.
4.	Security & Connectivity
o	Configured NSG rules to allow HTTP (port 80) traffic.
o	Managed firewall rules in both Windows (via PowerShell) and Linux (via ufw).
o	Ensured connectivity using Test-NetConnection, curl, and browser tests.
5.	Testing & Validation
o	Accessed the Load Balancer IP through a browser.
o	Verified that requests were routed to either the Windows or Linux VM randomly.
o	Ensured high availability and distribution using refresh cycles.
________________________________________
📄 Outcomes
•	Demonstrated the ability to architect and manage real-world cloud deployments.
•	Showcased cross-platform server management and load balancing in Azure.
•	Practiced DevOps principles: automation-ready infra, monitoring (via probes), and scalable design.
________________________________________
🔚 Sample Output in Browser
cpp
CopyEdit
http://<LoadBalancer-IP>
•	➤ "Hello from Aryaman’s Azure VM Web Server – Windows"
•	➤ "Hello from Linux VM! 🌐 – Apache Server"
________________________________________
🧠 Key Skills Demonstrated
•	✅ Azure VM provisioning (Linux + Windows)
•	✅ Load Balancer setup and backend pool management
•	✅ NSG & firewall rule configuration
•	✅ Port mapping, web server deployment
•	✅ Real-time debugging using CLI tools
•	✅ Network troubleshooting (netstat, curl, PowerShell)

## OutPut 

![image](https://github.com/user-attachments/assets/a37ab9fe-0c43-4504-b4ba-ec01e68b29b2)
![image](https://github.com/user-attachments/assets/9fef132f-0dbb-48ff-95ac-80a17547ee23)
![image](https://github.com/user-attachments/assets/e8a90b13-161a-4275-b544-898d1d56dde9)
![image](https://github.com/user-attachments/assets/b70ed702-7817-4a51-80b5-4fae68c5b369)
![image](https://github.com/user-attachments/assets/8088675c-5231-4b0e-8dd2-84a2100e232a)





