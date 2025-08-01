# Updated Documentation August 9th (Written: August 1, 2025) 
Source: Josh Madakor - Guided the initial development
# Building a SOC + Honeynet in Azure (Live Traffic)
I'm setting up a honeypot in Azure, intentionally exposing it to the public to attract attacks. I'll configure log forwarding so failed login attempts are sent to a local repository, which will then be connected to a SIEM. From there, I'll query the SIEM to generate an attack map, visualizing where live attacks are coming from in real time.

# Creating Resource Group
I'm setting up a resource group in Azure and creating a virtual network within it. I'll deploy a virtual machine inside that network, ensuring both are in the same region. To simulate an exposed system, I'll allow all inbound traffic to the VM and configure a cloud firewall with open access. This VM will act as a honeypot, attracting potential attackers. I'll also make sure to save the username and password for RDP access and use the ping command from the command line to verify connectivity before moving on.

![image](https://github.com/user-attachments/assets/36d2019d-738e-4faa-88cd-66729308b239)
![image](https://github.com/user-attachments/assets/b03b32c4-7f95-460f-a93b-d47a2be5048a)

# Analyzing Log Analytics and Creating Workspace
I'm setting up a log repository to collect attack data by forwarding logs from the honeypot. First, I'll create a Log Analytics Workspace (LAW) and set up Microsoft Sentinel as the SIEM, connecting it to the workspace. Next, I'll install and configure Windows Security Event Manager, then set up Windows Security Events via AMA. After that, I'll create a Data Collection Rule (DCR) to ensure logs are properly forwarded to the LAW workspace. Once everything is configured, I'll verify connectivity with a ping test, then leave the system running for 30 minutes to capture attack data

![image](https://github.com/user-attachments/assets/82f04875-3e25-4665-b9d7-a45d2bf70858)

# Querying Data
![image](https://github.com/user-attachments/assets/dc42cbd8-4df8-46ef-9891-8cdd5839d947)




![](https://github.com/user-attachments/assets/d6e38ed0-4057-4ce5-b37f-9fa479fa5b5e)
