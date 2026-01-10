# LAB PRACTICE:INSTALLING SOPHOS FIREWALL ON VMWARE WORKSTATION.

This Documentation provides a step by step process to install Sophos Firewall on VMware Workstation Pro on a Windows Host and to configure some firewall policies and endpoint installation.

## WHAT IS SOPHOS FIREWALL

**Sophos Firewall** is a **next‑generation network security system** (a firewall) made by Sophos, designed to protect networks from cyberthreats by inspecting, filtering, and controlling traffic between your internal network and the wider internet. 

Think of it as a **guard at your digital gates** that actively watches, analyzes, and responds to network traffic to stop intrusions, malware, ransomware, and other attacks before they can do harm

# FEATURS OF SOPHOS FW.

**Sophos Firewall — Core Features (Next‑Gen NGFW)**

**Threat Protection & Inspection**

- **Deep Packet Inspection (DPI)** with IPS (Intrusion Prevention) – blocks exploits and protocol attacks.
- **TLS 1.3 Encrypted Traffic Inspection** with high‑performance optimization.
- **Zero‑Day & ML Threat Detection** using machine learning.
- **Cloud Sandboxing** to analyze unknown files safely.

**Web & Application Control**

- **Web Filtering** (HTTPS/HTTP, categories).
- **DNS Protection** to block malicious domains.
- **Application Control & QoS** (user‑based app management).

**Automated Response & Integration**

- **Synchronized Security & Active Threat Response** with Sophos endpoints.
- **NDR Essentials (Cloud‑based network detection/response).**
- **ZTNA (Zero Trust Network Access)** support.

**Networking & Secure Access**

- **SD‑WAN & VPN (IPsec/SSL)** for secure inter‑site and remote connections.
- **User Identity Policies & 2FA Support.**

**Management & Reporting**

- **Centralized Cloud Management (Sophos Central).**
- **Firewall Health Check & Configuration Insights.**

# STEP  1: DOWNLOAD AND INSTALL VMWARE WORKSTATION PRO ON WINDOWS 11

Kindly install VMware Workstation using the steps from this link: [Registration](https://profile.broadcom.com/web/registration) and register with your email address

![Registering on Broadcom to Download VMware Workstation Pro](image.png)

Registering on Broadcom to Download VMware Workstation Pro

![Registering on Broadcom to Download VMware Workstation Pro](image%201.png)

Registering on Broadcom to Download VMware Workstation Pro

![Registered Successfully](image%202.png)

Registered Successfully

After the registering and logging in with your credentials, visit this link [Free Downloads - Support Portal - Broadcom support portal](https://support.broadcom.com/group/ecx/free-downloads) and choose VMware Workstation and download Version 17.5.2 

(I chose this version because i am on Windows 11 Version 23H2), so you can choose the one suitable for your Windows or Linux OS and Version.

Follow the prompts highlighted from the screenshots, then download and install VMware Workstation Pro.

![Follow the prompts highlighted from the screenshots, then download and install VMware Workstation Pro.](image%203.png)

Follow the prompts highlighted from the screenshots, then download and install VMware Workstation Pro.

![Follow the prompts highlighted from the screenshots, then download and install VMware Workstation Pro.](image%204.png)

Follow the prompts highlighted from the screenshots, then download and install VMware Workstation Pro.

![Select VMware Workstation Version to  Download](image%205.png)

Select VMware Workstation Version to  Download

![Agree to T&C](image%206.png)

Agree to T&C

![Additional Verification for Download of setup file](image%207.png)

Additional Verification for Download of setup file

![Additional Verification for Download of setup file](image%208.png)

Additional Verification for Download of setup file

![Download using IDM](image%209.png)

Download using IDM

# STEP 2: DOWNLOAD THE SOPHOS FIREWALL OS FOR VMWARE WORKSTATION.

Navigate to this link https://www.sophos.com/en-us/support/downloads/firewall-installers and follow the steps highlighted in the screenshots below

![Download of Sophos FW for VMware](image%2010.png)

Download of Sophos FW for VMware

Choose the Virtual Installers: Firewall OS for VMware option and click on the Download Button.

![Download of Sophos FW for VMware](image%2011.png)

Download of Sophos FW for VMware

![Download of Sophos FW for VMware](image%2012.png)

Download of Sophos FW for VMware

Clicking on the download button will redirect you to another page called “**End User Terms of Use & Export Compliance**”, fill in all the form fields and click submit to proceed with the download.

This will download the zipped file which you will need to extract with **7Zip** or WinRAR or the Windows 11 Zip Extractor.

I extracted the Zipped file using 7Zip Extractor and you will see the following file contents after extraction

![Extraction of Sophos Setup File](image%2013.png)

Extraction of Sophos Setup File

![Extraction of Sophos Setup File](image%2014.png)

Extraction of Sophos Setup File

# **STEP 3: CONFIGURE SOPHOS FIREWALL ON VMWARE WORKSTATION PRO.**

Kindly open the VMware Workstation Pro and click on File> Open, Navigate to the extract Sophos Firewall file and choose this specific file **“sf_virtual_vm8.ovf” then click Open to import the file specific for VMware Workstation Pro.**

![Importing Sophos OVF file to VMware](image%2015.png)

Importing Sophos OVF file to VMware

![Importing Sophos OVF file to VMware](image%2016.png)

Importing Sophos OVF file to VMware

After Importing the file, you will be required to fill in the details for the **“Name of the Virtual Machine**” ( i titled mine as Sophos NGFW), as you do this, the file path will be auto generated and you can choose to change it but i won’t because i have all my Virtual Machines in a preferred location which i chose,

After that I will click on import to continue with the installation

![Importing Sophos OVF file to VMware](image%2017.png)

Importing Sophos OVF file to VMware

![Importing Sophos OVF file to VMware](image%2018.png)

Importing Sophos OVF file to VMware

After clicking on import, the firewall will appear on the VMware interface as one of the Virtual Machines on your VMware.

![Importing Sophos OVF file to VMware](image%2019.png)

Importing Sophos OVF file to VMware

![Successfully Imported Sophos OVF file to VMware ](image%2020.png)

Successfully Imported Sophos OVF file to VMware 

You can choose to change the RAM Specification from 4GB to maybe 8GB for smooth Operation if you decide.

# **STEP 4: NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

You will observe that the Sophos Firewall Virtual Machine as 3 Network Adapters, so we need to configure the 2 NICs as Below

Network Adapter 1: Host Only

Network Adapter 2: Bridged Mode

Network 3: Not Needed, this will be removed as Sophos Needs 2 Network Adapters:- One for Internal Network Connection and One for Internet Connection.

For the Host Only Network Adapter, we would need to configure the IP range, this would be presented in the screenshots, Likewise we would set Network Adapter 2 as Bridged.

Click on the Edit Tab on VMware and click on the Virtual Network Editor to access the network configuration, this will launch the **Virtual Network Editor Interface**, then click on the **“Change Settings Shield Icon”**

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2021.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2022.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

After Clicking the  **“Change Settings Shield Icon”, You will observe that the option to “Add Network” is highlighted, click on it and select the VMNet Options, and click Ok ( I will be choosing VMNet1 as my preferred Virtual Network.)**

Also observe that VMnet0 and VMNet8 are already taken and used for Auto Bridging and NAT (Network Address Translation )connection, which is why i chose VMNet1.

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2023.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

From the Screenshot below I choose the VMNet1 option and configured the following:

Host Only, then i chose the Subnet IP: 192.168.12.0 with Subnet Mask: /24 or 255.255.255.0, 

I also ticked the connect a virtual host adapter to this network, and use local DHCP Service to distribute IPs to this VM.

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2024.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

After that I clicked on DHCP Settings to configure the Start and End IPs to sync with my Subnet IP

**Starting IP: 192.168.12.2** 

**Ending IP: 192.168.12.254**

Subnet Mask: 255.255.255.0

I used the default lease time on the VMware Interface.

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2025.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

After configuring the DHCP Settings, I clicked Ok and Apply then Ok to save the configurations and exit the Virtual Network Editor.

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2026.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2027.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

For this guide, I am using my WiFi Adapter, so i need to change my Bridged Network Interface from Automatic to my WiFi Adapter, I will be doing this while on the Virtual Network Editor.

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2028.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2029.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2030.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

![**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**](image%2031.png)

**NETWORK CONFIGURATIONS FOR SOPHOS FIREWALL ON VMWARE NETWORK MANAGER.**

The Next Step is to configure Network Adapters 1 and 2 as Host Only and Bridged respectively.

Click on “Edit Virtual Machine Settings” then navigate to Network Adapter 1.

![ Configure Network Adapters 1 and 2 as Host Only and Bridged respectively.](image%2032.png)

 Configure Network Adapters 1 and 2 as Host Only and Bridged respectively.

While on the same interface, navigate to Network Adapter 1, click on **“Host Only: A Private Network Shared with the Host”.**

![ Configure Network Adapters 1 and 2 as Host Only and Bridged respectively.](image%2033.png)

 Configure Network Adapters 1 and 2 as Host Only and Bridged respectively.

Then navigate to Network Adapter 2, under the Network Option, click on the **“Bridged connection: Connected Directly to the Physical Network”**

![ Configure Network Adapters 1 and 2 as Host Only and Bridged respectively.](image%2034.png)

 Configure Network Adapters 1 and 2 as Host Only and Bridged respectively.

While on the Same Interface, choose Network Adapter 3 and click on remove then click Ok to apply the settings you made.

![ Configure Network Adapters 1 and 2 as Host Only and Bridged respectively.](image%2035.png)

 Configure Network Adapters 1 and 2 as Host Only and Bridged respectively.

# **STEP 5: POWER ON THE SOPHOS VIRTUAL MACHINE AND CONFIGURE.**

Click on “Power on this Virtual Machine” to start the installation process and allow the installation to proceed automatically.

![**POWER ON THE SOPHOS VIRTUAL MACHINE**](image%2036.png)

**POWER ON THE SOPHOS VIRTUAL MACHINE**

The Installation process will boot to this interface and would prompt for a password, Kindly type **admin (the words won’t appear on the screen as you type but type admin and hit enter on your keyboard to continue the installation process).**

![Input Default Password](image%2037.png)

Input Default Password

Hit the letter “a” on your keyboard to accept the license terms (to accept input from your keyboard, you might need to use ctrl+ G then hit the letter a or use the navigation keys to highlight on Accept on hit enter).

![Accept Terms & Conditions](image%2038.png)

Accept Terms & Conditions

Kindly type 1 to enter into **“Network Configuration”, type 1 again and hit enter to enter into “interface configuration”**

![Kindly type 1 to enter into **“Network Configuration”, type 1 again and hit enter to enter into “interface configuration”**](image%2039.png)

Kindly type 1 to enter into **“Network Configuration”, type 1 again and hit enter to enter into “interface configuration”**

![Kindly type 1 to enter into **“Network Configuration”, type 1 again and hit enter to enter into “interface configuration”**](image%2040.png)

Kindly type 1 to enter into **“Network Configuration”, type 1 again and hit enter to enter into “interface configuration”**

When you get to the interface configuration, the installation will prompt you to hit enter, continue to hit enter till you see the interface to set the IPv4 address.

![Kindly type 1 to enter into **“Network Configuration”, type 1 again and hit enter to enter into “interface configuration”**](image%2041.png)

Kindly type 1 to enter into **“Network Configuration”, type 1 again and hit enter to enter into “interface configuration”**

Kindly type “y” for yes to set the IPv4 Address  for PORT A, then it will display the default IP: 172.16.16.16 and ask that you set the New IP Address, 

I will be choose an IPv4 Address from the range of IP Address we configured (recall: **Starting IP: 192.168.12.2 ,Ending IP: 192.168.12.254**).

![I will type my preferred IP **192.168.12.7**, ignore the prompt for the subnet mask and hit enter, then it will prompt me to enter the subnet mask, then i will hit enter again.](image%2042.png)

I will type my preferred IP **192.168.12.7**, ignore the prompt for the subnet mask and hit enter, then it will prompt me to enter the subnet mask, then i will hit enter again.

I will type my preferred IP **192.168.12.7**, ignore the prompt for the subnet mask and hit enter, then it will prompt me to enter the subnet mask, then i will hit enter again.

![I will type my preferred IP **192.168.12.7**, ignore the prompt for the subnet mask and hit enter, then it will prompt me to enter the subnet mask, then i will hit enter again.](image%2043.png)

I will type my preferred IP **192.168.12.7**, ignore the prompt for the subnet mask and hit enter, then it will prompt me to enter the subnet mask, then i will hit enter again.

![I will type my preferred IP **192.168.12.7**, ignore the prompt for the subnet mask and hit enter, then it will prompt me to enter the subnet mask, then i will hit enter again.](image%2044.png)

I will type my preferred IP **192.168.12.7**, ignore the prompt for the subnet mask and hit enter, then it will prompt me to enter the subnet mask, then i will hit enter again.

After hitting enter it will save the IP configuration and display the default IP for Port B (WAN IP: 172.17.115.199 with Subnet Mask: 255.255.255.0) as seen below, 

![After hitting enter it will save the IP configuration and display the default IP for Port B (WAN IP: 172.17.115.199 with Subnet Mask: 255.255.255.0) as seen below, ](image%2045.png)

After hitting enter it will save the IP configuration and display the default IP for Port B (WAN IP: 172.17.115.199 with Subnet Mask: 255.255.255.0) as seen below, 

It will bring up a prompt to set the IPv6 address but type “n” and hit enter to refuse changing the IP address and you will taken back to the Network Configuration Menu.

![ Type “n” and hit enter to refuse changing the IP address and you will taken back to the Network Configuration Menu.](image%2046.png)

 Type “n” and hit enter to refuse changing the IP address and you will taken back to the Network Configuration Menu.

![Network Configuration Completed Successfully.](image%2047.png)

Network Configuration Completed Successfully.

# **STEP 6: SETTING UP SOPHOS FIREWALL ON THE WEB ADMIN CONSOLE.**

Kindly minimize the VMware Application, then open a web browser, I will be using Microsoft Edge,

Copy and Paste this URL: [Sophos Firewall with Endpoint Synchronization | Free Trial](https://www.sophos.com/en-us/products/next-gen-firewall/free-trial) on your web browser to register for a free 30 days trial for Sophos Firewall.

Fill in all the necessary details and click submit, you will get a confirmation page informing you to check your email for evaluation serial number

![Fill in all the necessary details and click submit, you will get a confirmation page informing you to check your email for evaluation serial number](image%2048.png)

Fill in all the necessary details and click submit, you will get a confirmation page informing you to check your email for evaluation serial number

![Fill in all the necessary details and click submit, you will get a confirmation page informing you to check your email for evaluation serial number](image%2049.png)

Fill in all the necessary details and click submit, you will get a confirmation page informing you to check your email for evaluation serial number

The next step is to navigate to my Edge Browser and type my Static IP i configured which is 192.168.12.7 and Port 4444, its also important to type it like this because Sophos Firewall accepts https:// connections only, so i will type this on Edge Browser: [https://192.168.12.7:4444](https://192.168.12.7:4444) 

You will receive the caution sign that “Your connection is private”, Click on Advanced and click on **Continue to 192.168.12.7 (unsafe)**

![You will receive the caution sign that “Your connection is private”, Click on Advanced and click on **Continue to 192.168.12.7 (unsafe)**](image%2050.png)

You will receive the caution sign that “Your connection is private”, Click on Advanced and click on **Continue to 192.168.12.7 (unsafe)**

![You will receive the caution sign that “Your connection is private”, Click on Advanced and click on **Continue to 192.168.12.7 (unsafe)**](image%2051.png)

You will receive the caution sign that “Your connection is private”, Click on Advanced and click on **Continue to 192.168.12.7 (unsafe)**

After that you will be redirected to the Sophos Firewall welcome page, tick the option to **“I accept the Sophos End User Terms of Use” and choose Start Setup.**

![Tick the option to **“I accept the Sophos End User Terms of Use” and choose Start Setup.**](image%2052.png)

Tick the option to **“I accept the Sophos End User Terms of Use” and choose Start Setup.**

![Tick the option to **“I accept the Sophos End User Terms of Use” and choose Start Setup.**](image%2053.png)

Tick the option to **“I accept the Sophos End User Terms of Use” and choose Start Setup.**

I will go ahead to configure a new admin password, which i will store safely.

![ Configure a new admin password and store safely.](image%2054.png)

 Configure a new admin password and store safely.

After inputting the password, Kindly click on Continue and create a Storage Master Key (also store this safely in order not to forget it).

![Create a Storage Master Key (also store this safely in order not to forget it).](image%2055.png)

Create a Storage Master Key (also store this safely in order not to forget it).

Then tick the option that you have stored the storage master key in secure place and click on Continue.

![Tick the option that you have stored the storage master key in secure place and click on Continue.](image%2056.png)

Tick the option that you have stored the storage master key in secure place and click on Continue.

Next, you will give your firewall a preferred name of your choice and configure the time zone and click on Continue.

![Configure the time zone and click on Continue.](image%2057.png)

Configure the time zone and click on Continue.

The Next Step is to register your firewall using the serial key that was sent to your email after registering for a free trial, choose the “i have an existing serial key” option, insert the key, Tick “I don’t want to register now  and click Continue.

![ Register your firewall using the serial key that was sent to your email after registering for a free trial,](image%2058.png)

 Register your firewall using the serial key that was sent to your email after registering for a free trial,

Click on Continue to setup the Network LAN Configuration.

![Click on Continue to setup the Network LAN Configuration.](image%2059.png)

Click on Continue to setup the Network LAN Configuration.

You will observe that the IP we setup previously has been already inputted automatically, untick the DHCP Server option (because we already have a DHCP Server on VMware Workstation Pro) then click on Continue.

![Untick the DHCP Server option (because we already have a DHCP Server on VMware Workstation Pro) then click on Continue.](image%2060.png)

Untick the DHCP Server option (because we already have a DHCP Server on VMware Workstation Pro) then click on Continue.

After this, Tick all the boxes to protect your Network (all the options are needed for maximum security) and click on continue

![ Tick all the boxes to protect your Network (all the options are needed for maximum security) and click on continue](image%2061.png)

 Tick all the boxes to protect your Network (all the options are needed for maximum security) and click on continue

You can configure 2 email accounts which can be used to send Notifications and backup and the encryption password and don’t tick the option of using an external email server.

![Don’t tick the option of using an external email server.](image%2062.png)

Don’t tick the option of using an external email server.

After that you will be directed to the Configuration Summary page, click on Finish to apply all our configurations

Kindly be patient as it applies the configurations, the firewall will reboot from VMware Workstation Pro.

![Kindly be patient as it applies the configurations, the firewall will reboot from VMware Workstation Pro.](image%2063.png)

Kindly be patient as it applies the configurations, the firewall will reboot from VMware Workstation Pro.

![Kindly be patient as it applies the configurations, the firewall will reboot from VMware Workstation Pro.](image%2064.png)

Kindly be patient as it applies the configurations, the firewall will reboot from VMware Workstation Pro.

The Sophos Firewall will reboot from VMware and you will need to login with the new password

![The Sophos Firewall will reboot from VMware and you will need to login with the new password](image%2065.png)

The Sophos Firewall will reboot from VMware and you will need to login with the new password

![The Sophos Firewall will reboot from VMware and you will need to login with the new password](image%2066.png)

The Sophos Firewall will reboot from VMware and you will need to login with the new password

![The Sophos Firewall will reboot from VMware and you will need to login with the new password](image%2067.png)

The Sophos Firewall will reboot from VMware and you will need to login with the new password

Login with the Username as admin and with your new password.

![Login with the Username as admin and with your new password.](image%2068.png)

Login with the Username as admin and with your new password.

# STEP 7: CLAIM 30 DAYS TRAIL WITH SERIAL NUMBER.

After logging in using your credentials, you will see the serial number, click on continue to claim your 30days free trial.

![After logging in using your credentials, you will see the serial number, click on continue to claim your 30days free trial.](image%2069.png)

After logging in using your credentials, you will see the serial number, click on continue to claim your 30days free trial.

Click on Claim in Sophos Central and you will be redirected to the next page, if it asks for credentials, login with the same email which was used to register for the serial number

![Click on Claim in Sophos Central and you will be redirected to the next page, if it asks for credentials, login with the same email which was used to register for the serial number](image%2070.png)

Click on Claim in Sophos Central and you will be redirected to the next page, if it asks for credentials, login with the same email which was used to register for the serial number

You will be redirected to a page where you will see your serial number then click on Claim Firewall (the option to claim with 30 days… is automatically highlighted),

![You will be redirected to a page where you will see your serial number then click on Claim Firewall (the option to claim with 30 days… is automatically highlighted),](image%2071.png)

You will be redirected to a page where you will see your serial number then click on Claim Firewall (the option to claim with 30 days… is automatically highlighted),

Click on Continue to finish the setup.

![Click on Continue to finish the setup.](image%2072.png)

Click on Continue to finish the setup.

Our configuration is successful and we are on the Control Center.

![Our configuration is successful and we are on the Control Center.](image%2073.png)

Our configuration is successful and we are on the Control Center.

# STEP 8: CONFIGURING POLICIES ON SOPHOS FIREWALL.

It’s important to note that when creating and applying policies in Sophos Firewall, they are processed from Top to Bottom, this mean **policies to block traffic must come first**, followed by **policies to allow traffic**, because rules are processed from **top to bottom**, and the first match is applied.

So I will be using my Kali Virtual Machine to validate the Firewall policies i will create, this means i must configure the network interface to “” and a static IP with Sophos Firewall IP as the Gateway so the Kali VM is on the same IP range as Sophos i.e. “192.168.12.x & 255.255.255.0”

On VMware, Navigate to the Kali VM → click on **Edit Virtual Machine Settings → Click on Network Adapter** and change to “Host Only: A Private Network shared with the host” → Click Ok to apply changes.

![On VMware, Navigate to the Kali VM → click on **Edit Virtual Machine Settings → Click on Network Adapter** and change to “Host Only: A Private Network shared with the host” → Click Ok to apply changes.](image%2074.png)

On VMware, Navigate to the Kali VM → click on **Edit Virtual Machine Settings → Click on Network Adapter** and change to “Host Only: A Private Network shared with the host” → Click Ok to apply changes.

![On VMware, Navigate to the Kali VM → click on **Edit Virtual Machine Settings → Click on Network Adapter** and change to “Host Only: A Private Network shared with the host” → Click Ok to apply changes.](image%2075.png)

On VMware, Navigate to the Kali VM → click on **Edit Virtual Machine Settings → Click on Network Adapter** and change to “Host Only: A Private Network shared with the host” → Click Ok to apply changes.

## POLICY 1: ALLOW ALL LAN TO WAN TRAFFIC

Login to the Web admin console using this URL: [192.168.12.7:4444](https://192.168.12.7:4444/)

![Login to the Web admin console using this URL: [192.168.12.7:4444](https://192.168.12.7:4444/)](image%2076.png)

Login to the Web admin console using this URL: [192.168.12.7:4444](https://192.168.12.7:4444/)

Navigate to In the left-hand menu, click **“Rules and Policies”** → **“Firewall Rules”**.

You’ll see the list of current rules. (Remember: Rules are evaluated **top-down**.)

Click **“Add Firewall Rule”** → choose **“User/Network Rule”,** A new rule editor will open.

**Name:** Allow LANtoWAN (or any descriptive name)

**Description (optional):** Allow all traffic from LAN to the Internet
**Action:** Select **Accept**

| Section | What to do |
| --- | --- |
| **Rule Name** | Enter: Allow LANtoWAN |
| **Source Zone** | Select LAN |
| **Source Network** | Select LAN Subnet (`192.168.12.0/24)` |
| **Destination Zone** | Select `WAN` |
| **Destination Network** | Select `Any` |
| **Services** | Select `Any` (all protocols/ports) |
|  |  |

Then click on Save to Apply this rule.

![Click **“Add Firewall Rule”** → choose **“User/Network Rule”,** A new rule editor will open.](image%2077.png)

Click **“Add Firewall Rule”** → choose **“User/Network Rule”,** A new rule editor will open.

![**Name:** Allow LANtoWAN (or any descriptive name)](image%2078.png)

**Name:** Allow LANtoWAN (or any descriptive name)

![**Description (optional):** Allow all traffic from LAN to the Internet **Action:** Select **Accept**](image%2079.png)

**Description (optional):** Allow all traffic from LAN to the Internet **Action:** Select **Accept**

![Click Save](image%2080.png)

Click Save

Then Navigate to the NAT Rule Tab and click to create a NAT Rule

![Then Navigate to the NAT Rule Tab and click to create a NAT Rule](image%2081.png)

Then Navigate to the NAT Rule Tab and click to create a NAT Rule

![Then Navigate to the NAT Rule Tab and click to create a NAT Rule and configure the following](image%2082.png)

Then Navigate to the NAT Rule Tab and click to create a NAT Rule and configure the following

Then configure the following

| Field | Value / Action | Notes |
| --- | --- | --- |
| **Name** | Allow LANtoWAN&NAT | Any descriptive name |
| **Original Source Zone** | `LAN` | Your LAN devices are here |
| **Original Source Network** | `LAN_Subnet` | `192.168.12.0/24` (created earlier) |
| **Original Destination Zone** | `WAN` | Traffic going to the Internet |
| **Original Destination Network** | `Any` | All external IPs |
| **Translated Source (SNAT)** | `MASQUERADE` | Translates LAN IPs to WAN IP automatically |
| **Services** | `Any` | All ports/protocols |

![Click Save to apply configurations](image%2083.png)

Click Save to apply configurations

Now let’s test the rule, Let’s ping Google’s DN Server 8.8.8.8 works using the Sophos diagnostic tool.

On the Dashboard, Navigate to Diagnostics> Tools then type the following and click on Ping.

| Field | Value |
| --- | --- |
| IP address / Hostname | 8.8.8.8 |
| IP Version | IPv4 |
| Interface | Port B (This is our WAN Port ) |
| Size | 7 (number of pings) |

![On the Dashboard, Navigate to Diagnostics> Tools then type the following and click on Ping.](image%2084.png)

On the Dashboard, Navigate to Diagnostics> Tools then type the following and click on Ping.

![On the Dashboard, Navigate to Diagnostics> Tools then type the following and click on Ping.](image%2085.png)

On the Dashboard, Navigate to Diagnostics> Tools then type the following and click on Ping.

Ping response was successful

![Ping response was successful](image%2086.png)

Ping response was successful

So let’s validate via Kali. I will configure Kali with this static IP (192.168.12.4) and make the Sophos LAN IP my default gateway IP (192.168.12.7) using this command

Open the Terminal and run this command: 

```yaml
sudo nano /etc/network/interfaces
```

Then type this 

> auto lo
iface lo inet loopback
> 

> auto eth0
iface eth0 inet static
address 192.168.12.4
netmask 255.255.255.0
gateway 192.168.12.7
> 

> Press **CTRL+O** → Enter
> 

> Press **CTRL+X** to exit
> 

![So let’s validate via Kali. I will configure Kali with this static IP (192.168.12.4) and make the Sophos LAN IP my default gateway IP (192.168.12.7)](image%2087.png)

So let’s validate via Kali. I will configure Kali with this static IP (192.168.12.4) and make the Sophos LAN IP my default gateway IP (192.168.12.7)

Then run this command to restart the networking service: sudo systemctl restart networking

![ sudo systemctl restart networking](image%2088.png)

 sudo systemctl restart networking

Verify Static IP and the gateway IP too, run these commands

ip a    #shows the static ip

> ┌──(paul㉿Paul)-[~]
└─$ ip a
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
link/ether 00:0c:29:3c:2a:d3 brd ff:ff:ff:ff:ff:ff
inet 192.168.12.4/24 brd 192.168.12.255 scope global eth0
valid_lft forever preferred_lft forever
inet6 fe80::20c:29ff:fe3c:2ad3/64 scope link proto kernel_ll
valid_lft forever preferred_lft forever
> 

ip r      # Should show default via 192.168.12.7

┌──(paul㉿Paul)-[~]
└─$ ip r

default via 192.168.12.7 dev eth0 onlink
192.168.12.0/24 dev eth0 proto kernel scope link src 192.168.12.4

Then Ping Google DNS Server

![IP config on Interfaces](image%2089.png)

IP config on Interfaces

Ping is successful

![Successful Ping from Google DNS.](image%2090.png)

Successful Ping from Google DNS.

We have an issue, ping to [google.com](http://google.com) isn’t responding.

┌──(paul㉿Paul)-[~]
└─$ ping -c 4 [google.com](http://google.com/)

ping: [google.com](http://google.com/): Temporary failure in name resolution  ## this points to an issue with DNS because Kali is unable to resolve google.com

![Ping to [google.co](http://google.co)m wasn’t successful](image%2091.png)

Ping to [google.co](http://google.co)m wasn’t successful

Let’s run this command to check the DNS Configuration on my Kali VM.

sudo nano /etc/resolv.conf

![sudo nano /etc/resolv.conf](image%2092.png)

sudo nano /etc/resolv.conf

![sudo nano /etc/resolv.conf](image%2093.png)

sudo nano /etc/resolv.conf

The Output above shows that Google DNS isn’t configured hence why name resolution fails with the error.

So i want to make my Sophos LAN IPv4 address to be my DNS so i can access Websites like [Google.com](http://Google.com) by running this command and hitting enter.

sudo nano /etc/resolv.conf

![So i want to make my Sophos LAN IPv4 address to be my DNS so i can access Websites like [Google.com](http://google.com/) by running this command and hitting enter.

](image%2094.png)

So i want to make my Sophos LAN IPv4 address to be my DNS so i can access Websites like [Google.com](http://google.com/) by running this command and hitting enter.

![So i want to make my Sophos LAN IPv4 address to be my DNS so i can access Websites like [Google.com](http://google.com/) by running this command and hitting enter.](image%2095.png)

So i want to make my Sophos LAN IPv4 address to be my DNS so i can access Websites like [Google.com](http://google.com/) by running this command and hitting enter.

The current configuration shows this and we are updating the nameserver to 192.168.12.7 and use 

 **CTRL + O to Save and**  **CTRL + X to Exit.**

rated by NetworkManager
search localdomain
nameserver 192.168.12.1

After Updating it will look like this

rated by NetworkManager
search localdomain
nameserver 192.168.12.7

So Let’s Ping Google.com, Bing.com, From the screenshots, they are both successful and the webpage works too.

![So Let’s Ping [Google.com](http://google.com/), [Bing.com](http://bing.com/), From the screenshots, they are both successful and the webpage works too.](image%2096.png)

So Let’s Ping [Google.com](http://google.com/), [Bing.com](http://bing.com/), From the screenshots, they are both successful and the webpage works too.

![So Let’s Ping [Google.com](http://google.com/), [Bing.com](http://bing.com/), From the screenshots, they are both successful and the webpage works too.](image%2097.png)

So Let’s Ping [Google.com](http://google.com/), [Bing.com](http://bing.com/), From the screenshots, they are both successful and the webpage works too.

The Webpages also load successfully.

![The Webpages also load successfully.](image%2098.png)

The Webpages also load successfully.

![The Webpages also load successfully.](image%2099.png)

The Webpages also load successfully.

## POLICY 2: BLOCK [INSTAGRAM.COM](http://INSTAGRAM.COM) USING URL FILTER.

STEP 1: Login to the Sophos Web Console, Under Protect 

Go to Web → URL Groups → Click Add → Name it Block-Instagram→ Add these entries one by one:

and click Save.

[instagram.com](http://instagram.com/)
[www.instagram.com](http://www.instagram.com/)

![STEP 1: Login to the Sophos Web Console, Under Protect ](image%20100.png)

STEP 1: Login to the Sophos Web Console, Under Protect 

![Go to Web → URL Groups → Click Add → Name it Block-Instagram](image%20101.png)

Go to Web → URL Groups → Click Add → Name it Block-Instagram

![The Block- Instagram rule exists under URL Groups.](image%20102.png)

The Block- Instagram rule exists under URL Groups.

Kindly follow the steps below to Create a Web Filter Policy:

Go to: Web → Policies → Add Policy → Name: Block-Instagram-Policy → URL Groups: Block-Instagram →Save

![Go to: Web → Policies → Add Policy → Name: Block-Instagram-Policy → URL Groups: Block-Instagram →Save](image%20103.png)

Go to: Web → Policies → Add Policy → Name: Block-Instagram-Policy → URL Groups: Block-Instagram →Save

You will be redirected to this page Below, follow these steps below:

1. Add Rule → Under Activities Click on All Web Traffic, Use the Minus or dash sign to remove All Web Traffic→ then Click on Add New Item 
2. → Click on the drop down list change to URL Groups→ check the box with Block-Instagram → 
3. Click on Apply selected item → Change the action to Block for the rule we added (do this for Action & the padlock sign, one is for http while the padlock is for https) → 
4. Then under Status toggle the button to change from off to on → Scroll down and click Save

![Add Rule → Under Activities Click on All Web Traffic, Use the Minus or dash sign to remove All Web Traffic→ then Click on Add New Item ](image%20104.png)

Add Rule → Under Activities Click on All Web Traffic, Use the Minus or dash sign to remove All Web Traffic→ then Click on Add New Item 

![Click on the drop down list change to URL Groups→ check the box with Block-Instagram → ](image%20105.png)

Click on the drop down list change to URL Groups→ check the box with Block-Instagram → 

From the Screenshot Below, we are being directed to visit the Firewall Rules to add this policy, Kindly click on **Goto Firewall Rules to continue.**

![From the Screenshot Below, we are being directed to visit the Firewall Rules to add this policy, Kindly click on **Goto Firewall Rules to continue.**](image%20106.png)

From the Screenshot Below, we are being directed to visit the Firewall Rules to add this policy, Kindly click on **Goto Firewall Rules to continue.**

Click on Add Firewall Rule → New Firewall Rule and fill out the details below:

Rule Group: None
Tick Log Firewall Traffic
Rule Name: Block-Instagram-Policy
Source Zones: LAN
Destination Zones: WAN
Under Security Features, You will see Web Filtering→ Under Web Policy Click on the drop down list choose Block-Instagram-Policy → Click Save.

![Click on Add Firewall Rule → New Firewall Rule and fill out the details below:](image%20107.png)

Click on Add Firewall Rule → New Firewall Rule and fill out the details below:

![Under Security Features, You will see Web Filtering→ Under Web Policy Click on the drop down list choose Block-Instagram-Policy → Click Save.](image%20108.png)

Under Security Features, You will see Web Filtering→ Under Web Policy Click on the drop down list choose Block-Instagram-Policy → Click Save.

On Sophos Firewall, rules are evaluated top to bottom. 

The first rule that matches the traffic is the one that applies, and the rest are ignored. 

From the screenshot below, the  Block-Instagram-Policy is sitting below “Allow LAN → WAN” rules, this means [instagram.com](http://instagram.com) will still be accessible.

So I need to move the Instagram policy to Number 1 and check if its still accessible.

![So I need to move the Instagram policy to Number 1 and check if its still accessible.](image%20109.png)

So I need to move the Instagram policy to Number 1 and check if its still accessible.

To Move it to number 1, I will click on the 3 horizontal dots with a circle (…) highlighted on the screenshot which will bring a notification box, i will type 1 close to “Move to” and hit enter and click **Ok** to apply the changes.

![To Move it to number 1, I will click on the 3 horizontal dots with a circle (…) highlighted on the screenshot which will bring a notification box.](image%20110.png)

To Move it to number 1, I will click on the 3 horizontal dots with a circle (…) highlighted on the screenshot which will bring a notification box.

![ I will type 1 close to “Move to” and hit enter and click **Ok** to apply the changes.](image%20111.png)

 I will type 1 close to “Move to” and hit enter and click **Ok** to apply the changes.

As you can see the Instagram Policy is now Number 1, so let’s access [Instagram.com](http://Instagram.com) from Kali Virtual Machine.

![As you can see the Instagram Policy is now Number 1, so let’s access [Instagram.com](http://Instagram.com) from Kali Virtual Machine.](image%20112.png)

As you can see the Instagram Policy is now Number 1, so let’s access [Instagram.com](http://Instagram.com) from Kali Virtual Machine.

As you can see the [www.instagram.com](http://www.instagram.com) page is inaccessible.

![As you can see the [www.instagram.com](http://www.instagram.com) page is inaccessible.](image%20113.png)

As you can see the [www.instagram.com](http://www.instagram.com) page is inaccessible.

Using the Sophos Policy Tester

![Using the Sophos Policy Tester](image%20114.png)

Using the Sophos Policy Tester

Other Sites like [Google.com](http://Google.com) and [Altschoolafrica.com](http://Altschoolafrica.com) are still accessible which shows that our firewall rule is working from Top to Bottom.

![Other Websites are accessible](image%20115.png)

Other Websites are accessible

## POLICY 3: BLOCK AUDIO FILES DOWNLOADS ON SOPHOS FIREWALL.

Navigate to the Web Console, Go to Web → Policies → Add Policy and Create a policy using the following details:

Name: Block Audio Files Download

Click on Add Rule → a Template would be created → Click on all web traffic, use the minus (-) sign to remove All Web Traffic → 

Click on Add Item → Click Add→ for Name Type  Block Audio Files Downloads →

Click on Add New Item and choose Audio Files, Apply the selected items and Save

![Navigate to the Web Console, Go to Web → Policies → Add Policy and Create a policy using the following details:](image%20116.png)

Navigate to the Web Console, Go to Web → Policies → Add Policy and Create a policy using the following details:

![Click on Add Rule → a Template would be created → Click on all web traffic, use the minus (-) sign to remove All Web Traffic → ](image%20117.png)

Click on Add Rule → a Template would be created → Click on all web traffic, use the minus (-) sign to remove All Web Traffic → 

Tick the rule you created and click on Apply selected item Scroll down and click on Save

![Tick the rule you created and click on Apply selected item Scroll down and click on Save](image%20118.png)

Tick the rule you created and click on Apply selected item Scroll down and click on Save

Also click on the default action to block HTTP Connection then click Apply.

![Also click on the default action to block HTTP Connection then click Apply.](image%20119.png)

Also click on the default action to block HTTP Connection then click Apply.

Toggle on the status and Click Apply changes

![Toggle on the status and Click Apply changes](image%20120.png)

Toggle on the status and Click Apply changes

Next Click on Goto Firewall Rules so this policy can be added to an existing firewall rule.

![Next Click on Goto Firewall Rules so this policy can be added to an existing firewall rule.](image%20121.png)

Next Click on Goto Firewall Rules so this policy can be added to an existing firewall rule.

Navigate to the Allow LAN to WAN rule an click on Edit → Scroll to Security Features → Web Filtering 

→ Web Policy click on the drop down list and choose Block Audio MP3 Downloads Policy that was created → Click on Save.

![Navigate to the Allow LAN to WAN rule an click on Edit → Scroll to Security Features ](image%20122.png)

Navigate to the Allow LAN to WAN rule an click on Edit → Scroll to Security Features 

![→ Web Filtering → Web Policy click on the drop down list and choose Block Audio MP3 Downloads Policy that was created → Click on Save.](image%20123.png)

→ Web Filtering → Web Policy click on the drop down list and choose Block Audio MP3 Downloads Policy that was created → Click on Save.

Choose the Block Audio MP3 Download, Tick the Block QUIC Protocol and click on **Save** to apply the policy

![Choose the Block Audio MP3 Download, Tick the Block QUIC Protocol and click on **Save** to apply the policy](image%20124.png)

Choose the Block Audio MP3 Download, Tick the Block QUIC Protocol and click on **Save** to apply the policy

![First Policy on the list is the Block Instagram Rule.](image%20125.png)

First Policy on the list is the Block Instagram Rule.

To Test this using the Policy Tester, Navigate to Monitor & Analyze → Diagnostics → Click on Policy Tester, Fill in the below details and Click on Test

URL 2: [https://sample.cat/en/mp3](https://sample.cat/en/mp3)

Test Method: Web Policy

Web Policy: Click the drop down and choose Block Audio MP3 Download and click on Test and ut shows BLOCKED.

![MP3 Download was BLOCKED Successfully.](image%20126.png)

MP3 Download was BLOCKED Successfully.

## POLICY 4: POLICY TO FORCE SAFESEARCH ON BROWSERS.

To configure this Policy, Kindly follow the instructions below.

Kindly Navigate  to the Sophos Dashboard→ then click on Web → Policies → Add Policy

![Kindly Navigate  to the Sophos Dashboard→ then click on Web → Policies → Add Policy](image%20127.png)

Kindly Navigate  to the Sophos Dashboard→ then click on Web → Policies → Add Policy

Tick Enforce SafeSearch… & Enforce YouTube Restrictions, Restriction Level should be set to Strict, also Allowed Time Quota is fine for 1 hour.

Then Click on Add Rule and Use the following Settings:

In the rule table above:
• 	Users: “Anybody” — good for applying to all users
• 	Activities: “All web traffic” — this covers search engines
• 	Action & Constraints: Click the shield icon, and choose block HTTP and for the other shield icon, click and choose block HTTPS, 

• 	Under Constraint, Choose All the Time
• 	Set Status to be toggled
• 	Under Constraints, confirm SafeSearch enforcement is active

Click on Save to apply these settings.

These settings will rewrite search queries to force strict filtering on Google, Bing, Yahoo, and YouTube.

![These settings will rewrite search queries to force strict filtering on Google, Bing, Yahoo, and YouTube.](image%20128.png)

These settings will rewrite search queries to force strict filtering on Google, Bing, Yahoo, and YouTube.

Click on Goto Firewall Rules, choose the LAN to WAN rule and click on Edit

![Click on Goto Firewall Rules, choose the LAN to WAN rule and click on Edit](image%20129.png)

Click on Goto Firewall Rules, choose the LAN to WAN rule and click on Edit

We will need to create a LAN to WAN Rule then apply this Enforce Safe Search as the web policy

Goto Protect → Rules & Policies → Firewall Rules → Add Firewall Rule → New Firewall Rule

![We will need to create a LAN to WAN Rule then apply this Enforce Safe Search as the web policy](image%20130.png)

We will need to create a LAN to WAN Rule then apply this Enforce Safe Search as the web policy

Kindly Configure the following:

Rule Name: SafeSearch FW

Action: Drop and Tick Log Firewall Traffic

Source Zone is LAN

Destination Zone is WAN

Destination Network: Click on Add New Item → Add → IP Range→ Name LAN Subnet  192.168.12.0, Choose IPv4 for IP Version → Choose Network for Type → for IP Address type  192.168.12.0, Subnet remains /24 → Click on Save

Navigate to “Security Features” → Under Web Filtering → Choose Web Policy → Scroll to Enforce SafeSearch, → Tick Block QUICK Protocol → Click Save

![Kindly Configure the following:](image%20131.png)

Kindly Configure the following:

As you can see below, the firewall rule has been created

![As you can see below, the firewall rule has been created](image%20132.png)

As you can see below, the firewall rule has been created

To Test this using the Policy Tester, Navigate to Monitor & Analyze → Diagnostics → Click on Policy Tester, Fill in the below details and Click on Test

URL: [https://www.google.com/search?q=test](https://www.google.com/search?q=test)

Test Method: Web Policy

Web Policy: Click the drop down and choose Enforce SafeSearch and click on Test

You will observe the result shows BLOCKED, which means its working

![You will observe the result shows BLOCKED, which means its working](image%20133.png)

You will observe the result shows BLOCKED, which means its working

# INSTALLING SOPHOS ENDPOINT ON WINDOWS DEVICE

To Install the Sophos Endpoint on our Windows Device, we would need to login to the Sophos Central URL: [Sophos Central](https://central.sophos.com/manage/) since we linked the firewall to the account.

During the Login Process, You will be asked to setup a Passkey or Multi Factor Authentication (MFA), I chose the MFA Method and follow the steps from Sophos Central.

![Sophos Central Dashboard](image%20134.png)

Sophos Central Dashboard

Upon Successful Login, Kindly navigate to My Products → Endpoint → Installers

![Upon Successful Login, Kindly navigate to My Products → Endpoint → Installers](image%20135.png)

Upon Successful Login, Kindly navigate to My Products → Endpoint → Installers

 

![Choose Endpoint Installer for Windows ](image%20136.png)

Choose Endpoint Installer for Windows 

Click on the Windows Installer to download then you will install on the Windows Endpoint, 

After Installation, your Windows Device will automatically be visible on the Sophos Central Dashboard.

Kindly Navigate to Products → Endpoint → Computers

![Kindly Navigate to Products → Endpoint → Computers](image%20137.png)

Kindly Navigate to Products → Endpoint → Computers

![Windows PC onboarded successfully](image%20138.png)

Windows PC onboarded successfully

![This is the Interface of the Sophos Endpoint on the Windows Machine.](image%20139.png)

This is the Interface of the Sophos Endpoint on the Windows Machine.

### CONFIGURING POLICIES ON WINDOWS ENDPOINT.

From the Sophos Dashboard, Kindly Navigate to Products → Endpoint → Computers → Click on Orion (The Name of my Windows Device)

![From the Sophos Dashboard, Kindly Navigate to Products → Endpoint → Computers → Click on Orion (The Name of my Windows Device)](image%20140.png)

From the Sophos Dashboard, Kindly Navigate to Products → Endpoint → Computers → Click on Orion (The Name of my Windows Device)

Then, Kindly click on Policies as highlighted on the Screenshot.

![Policies on Endpoint Dashboard](image%20141.png)

Policies on Endpoint Dashboard

**Note:** The policies at the top of the list override the policies at the bottom of the list, like we stated earlier Sophos Firewall checks policies from Top to Bottom.

### CONFIGURING  POLICIES ON OUR ENDPOINT

### **1. APPLICATION CONTROL POLICY**

While on the Endpoint Dashboard, Navigate to Base Policy- Application Control.

![While on the Endpoint Dashboard, Navigate to Base Policy- Application Control.](image%20142.png)

While on the Endpoint Dashboard, Navigate to Base Policy- Application Control.

Navigate to Settings Tab

![Navigate to Settings Tab](image%20143.png)

Navigate to Settings Tab

Click on Add/Edit List to select the list of Applications to block

![Click on Add/Edit List to select the list of Applications to block](image%20144.png)

Click on Add/Edit List to select the list of Applications to block

I will like to block the following Applications which are installed on my Windows PC:

1. Archive Tool- 7Zip
2. Internet Browser- Vivaldi
3. Media Player - Spotify

![Select Archive Tool then Choose 7Zip](image%20145.png)

Select Archive Tool then Choose 7Zip

![Select Internet Browser and Choose Vivaldi](image%20146.png)

Select Internet Browser and Choose Vivaldi

![Select Media Player  and Choose Spotify](image%20147.png)

Select Media Player  and Choose Spotify

After making the selections, then click on Save to List and click on save to apply changes.

You can also choose to toggle on the detection Options and to type a customized Desktop message.

![Select the Radio Button to block the 3 Applications](image%20148.png)

Select the Radio Button to block the 3 Applications

![Create a customized Desktop Message for Blocked Applications](image%20149.png)

Create a customized Desktop Message for Blocked Applications

![Save Changes to Policy](image%20150.png)

Save Changes to Policy

![Changes to Application Policy Saved Successfully](image%20151.png)

Changes to Application Policy Saved Successfully

### VALIDATING APPLICATION CONTROL POLICY.

![Spotify Blocked Successfully](image%20152.png)

Spotify Blocked Successfully

![7-Zip Blocked Successfully](image%20153.png)

7-Zip Blocked Successfully

![Vivaldi Blocked Successfully](image%20154.png)

Vivaldi Blocked Successfully

You can also view the reports from who tried to access the applications by navigating to the Endpoint Dashboard → People → Click on your PC Name (Orion for me) → Click on Events Tab for a more detailed view or you can click on the Summary Tab.

![Viewing Reports for Application Policy](image%20155.png)

Viewing Reports for Application Policy

![Events Summary for Application Policy](image%20156.png)

Events Summary for Application Policy

## 2. WEB CONTROL POLICY

While on the Endpoint Dashboard, Kindly Click on Policies and choose Base Policy: Web Control

![While on the Endpoint Dashboard, Kindly Click on Policies and choose Base Policy: Web Control](image%20157.png)

While on the Endpoint Dashboard, Kindly Click on Policies and choose Base Policy: Web Control

Navigate to settings → Acceptable Web Usage→ View Details → Choose Block for “**Social Networking” & “Adult and potentially inappropriate categories”**

![Navigate to settings → Acceptable Web Usage→ View Details → Choose Block for “**Social Networking” & “Adult and potentially inappropriate categories”**](image%20158.png)

Navigate to settings → Acceptable Web Usage→ View Details → Choose Block for “**Social Networking” & “Adult and potentially inappropriate categories”**

![Navigate to settings → Acceptable Web Usage→ View Details → Choose Block for “**Social Networking” & “Adult and potentially inappropriate categories”**](image%20159.png)

Navigate to settings → Acceptable Web Usage→ View Details → Choose Block for “**Social Networking” & “Adult and potentially inappropriate categories”**

Click on Save to apply policies

![Click on Save to apply policies](image%20160.png)

Click on Save to apply policies

### VALIDATING WEB POLICY

From the Screenshots below, The Sophos Web Policy we configured blocked the following sites- WhatsApp, Facebook, TikTok, Adult Sites, Twitter (X).

![WhatsApp Blocked Successfully](image%20161.png)

WhatsApp Blocked Successfully

![Facebook Blocked Successfully](image%20162.png)

Facebook Blocked Successfully

![Twitter Blocked Successfully](image%20163.png)

Twitter Blocked Successfully

![XVideos Blocked Successfully](image%20164.png)

XVideos Blocked Successfully

![TikTok Blocked Successfully](image%20165.png)

TikTok Blocked Successfully

The Sophos Endpoint Agent on the Windows PC also records these firewall rules, you can access using the Endpoint and navigate to the Events Tab.

![Events logged on Sophos Endpoint Agent on the Windows PC](image%20166.png)

Events logged on Sophos Endpoint Agent on the Windows PC

## 3. DATA LOSS PREVENTION (DLP) POLICY

On Sophos, DLP (Data Loss Prevention) is a security feature that helps prevent sensitive or confidential data from being accidentally or intentionally leaked outside your organization. 

It works by monitoring, controlling, and restricting the transfer of files containing sensitive information  like Bank Card Details across endpoints, email, USB devices, and cloud service.

I can create custom policies on Sophos by cloning the specific policy when access, in this case , i want to clone the DLP Policy. when we create cloned policies we can apply them to specific device but when we use the default policies, it applies it to all devices linked to Sophos Firewall 

As usual on the Endpoint Dashboard, I will navigate to the Policies Tab and choose DLP then select Clone and give it a suitable name.

![Cloning DLP Default Base Policy](image%20167.png)

Cloning DLP Default Base Policy

Then you will be required to input a name for your policy and I want this policy to be applied on the Device itself then click on Continue.

![Cloning DLP Default Base Policy for My Windows Device](image%20168.png)

Cloning DLP Default Base Policy for My Windows Device

You will need to select your Device and use the > to move it to assigned categories 

![You will need to select your Device and use the > to move it to assigned categories ](image%20169.png)

You will need to select your Device and use the > to move it to assigned categories 

The Next step is to make the Policy Active by enabling it from the Policy Inactive Tab, then Click Save

![Activating the Clone DLP Policy](image%20170.png)

Activating the Clone DLP Policy

![Creating Sophos Policy Templates for DLP](image%20171.png)

Creating Sophos Policy Templates for DLP

The Next Step is to pick the exact Rule that i need and to also enable the message when the file transfer is blocked, also toggle on the “use rules for data transfer”

Finance and share trading activities [USA] - Bank & card accounts [USA]
Finance and share trading activities [USA] - Contact details - mixed [USA]

Then click on save.

![The Next Step is to pick the exact Rule that i need and to also enable the message when the file transfer is blocked, also toggle on the “use rules for data transfer”](image%20172.png)

The Next Step is to pick the exact Rule that i need and to also enable the message when the file transfer is blocked, also toggle on the “use rules for data transfer”

Then I can also make changes on the 2 alerts by clicking on the policy and clicking on each individual rule.

I will enabled the action to block transfer for the 2 rules:

Finance and share trading activities [USA] - Bank & card accounts [USA]
Finance and share trading activities [USA] - Contact details - mixed [USA] 

![Configuring Destination where file uploads can be done like Instant Messaging, Internet Browsers, etc. for the 2 Rules](image%20173.png)

Configuring Destination where file uploads can be done like Instant Messaging, Internet Browsers, etc. for the 2 Rules

![For File Contains for the 2 DLP Rules](image%20174.png)

For File Contains for the 2 DLP Rules

After this click on save, them we will create one more rule called PAN Card

A PAN card (Permanent Account Number card) is a government-issued identification document in India that serves as a unique tax and financial identity for individuals and entities.

The Nigerian equivalent is TIN, NIN.

![Adding a New Content Rule called PAN Card in addition to the 2 Rules](image%20175.png)

Adding a New Content Rule called PAN Card in addition to the 2 Rules

These are the fields i filled and i chose the block transfer radio button, then also click on Next Rule Configuration.

![Blocking Transfer for PAN Card Rule](image%20176.png)

Blocking Transfer for PAN Card Rule

For File contains, search and choose PAN (India)

![For File contains, search and choose PAN (India)](image%20177.png)

For File contains, search and choose PAN (India)

For Destination Is, choose the previous options we picked

![For Destination Is, choose the previous options we picked](image%20178.png)

For Destination Is, choose the previous options we picked

Then Click on Finish and Save.

![Then Click on Finish and Save.](image%20179.png)

Then Click on Finish and Save.

### VALIDATING DLP POLICY

To Test this, i created a fake Master card details in a notepad file. from this site: https://developers.bluesnap.com/reference/test-credit-cards

### **Test via  Uploading on WhatsApp, ChatGPT**

![**Test via  Uploading on ChatGPT**](image%20180.png)

**Test via  Uploading on ChatGPT**

![**Test via  Uploading on WhatsApp**](image%20181.png)

**Test via  Uploading on WhatsApp**

![**Test via  Uploading on WhatsApp & ChatGPT**](image%20182.png)

**Test via  Uploading on WhatsApp & ChatGPT**

### Test via DLPTest Website (HTTP Post)

I tried to upload the same notepad file via this link:- https://dlptest.com/http-post/

![Test via DLPTest Website (HTTP Post)](image%20183.png)

Test via DLPTest Website (HTTP Post)

I can check the Logs from the Endpoint Dashboard by clicking on Reports and the specific policy which is DLP

![Endpoint Reports Dashboard for DLP](image%20184.png)

Endpoint Reports Dashboard for DLP

![Endpoint Reports Dashboard for DLP](image%20185.png)

Endpoint Reports Dashboard for DLP

Logs from Sophos Endpoint Agent

![Logs from Sophos Endpoint Agent](image%20186.png)

Logs from Sophos Endpoint Agent

## 4. PERIPHERAL CONTROL POLICY

Its important to note that when modifying default Sophos policies and saving them, it automatically applies them to all devices linked to Sophos, If we want specific policies to be applied to just one device then we have the option to clone the default policy, modify and save it.

So we would clone the peripheral control policy and apply it 1 windows device.

Navigate to the Endpoint Dashboard on Sophos Central, Click on Base Policy- Peripheral Control

![Cloned Policy for Peripheral Control Policy via Default Policy](image%20187.png)

Cloned Policy for Peripheral Control Policy via Default Policy

Click on Clone and follow the prompts to give it name,  You can choose for the policy to be applied to either the Windows user profile or the Windows Device itself, for me i am choosing the Windows Device then click on **Continue.**

![Cloned Policy for Peripheral Control Policy via Endpoint Dashboard](image%20188.png)

Cloned Policy for Peripheral Control Policy via Endpoint Dashboard

![Cloned Policy for Peripheral Control for Device](image%20189.png)

Cloned Policy for Peripheral Control for Device

Then choose the specific Windows Device Name (Orion) and use the > sign to move it to the right and click on **Save**

![Assigned Computers for Peripheral Control Policy](image%20190.png)

Assigned Computers for Peripheral Control Policy

Clicking **Save** will load the policies page and you will see the cloned profile for Peripheral Control, we will select it and configure the specific peripheral to block.

![Cloned Policy for Peripheral Control Policy](image%20191.png)

Cloned Policy for Peripheral Control Policy

Kindly click on Settings and click on Control access by peripheral type and add exemptions  (to block specific peripheral)

Select  Secure Removable Storage & Removable Storage (USB Devices ) and choose Block, you can also choose to add a Desktop Custom message like i did  **“This is NOT Allowed.”,** 

![Enabling  Peripheral Control Policy for Removable Storage](image%20192.png)

Enabling  Peripheral Control Policy for Removable Storage

![Desktop Message for Peripheral Control Policy](image%20193.png)

Desktop Message for Peripheral Control Policy

To make the Policy Active, click on the “Policy Inactive” Tab and toggle on to Active and click on Save to apply all the changes.

![Enabling Peripheral Policy to be Active](image%20194.png)

Enabling Peripheral Policy to be Active

![Enabling Peripheral Policy to be Active](image%20195.png)

Enabling Peripheral Policy to be Active

### VALIDATING PERIPHERAL CONTROL POLICY

From the Screenshot below, we can see the USB inserted to the Laptop was blocked.

![Test via Peripheral Control Policy](image%20196.png)

Test via Peripheral Control Policy

![Sophos Endpoint Events Page](image%20197.png)

Sophos Endpoint Events Page

## 5. THREAT PROTECTION POLICY

From our previous policies configuration, we would be cloning the Threat Protection Default Policy and applying it to our device.

![Clone Policy for Threat Protection Policy](image%20198.png)

Clone Policy for Threat Protection Policy

The Next step is to add the assigned device for this policy, then make it active from the Policy Inactive Tab and click on save

![Assigned Computer for Threat Protection Policy](image%20199.png)

Assigned Computer for Threat Protection Policy

Let’s configure our policies from the Settings Tab, i only edited the scan period and for it to perform a deep scan

![Scan Period for Threat Protection Policy](image%20200.png)

Scan Period for Threat Protection Policy

I also added a Desktop Message as seen below and i clicked Save

### VALIDATING THREAT PROTECTION POLICY

To validate this policy, i will download an antimalware test file from eicar from https://www.eicar.org/download-anti-malware-testfile/

You can choose either zip or txt file from the site.

![EICAR ANTIMALWARE TEST FILE](image%20201.png)

EICAR ANTIMALWARE TEST FILE

![Threat Protection Policy Test using EICAR Antimalware file test](image%20202.png)

Threat Protection Policy Test using EICAR Antimalware file test

![Threat Protection Policy Test using EICAR Antimalware file test](image%20203.png)

Threat Protection Policy Test using EICAR Antimalware file test

So Sophos doesn’t just block the download of the file, it also cleans up the threat from the attempted download.

![Threat Protection Policy Test using EICAR Antimalware file test](image%20204.png)

Threat Protection Policy Test using EICAR Antimalware file test

We can also navigate to the Threat Analysis Centre from Sophos Dashboard to view our logs

![Threat Analysis Dashboard to monitor Threat Protection Policy](image%20205.png)

Threat Analysis Dashboard to monitor Threat Protection Policy

Then Navigate to Threat Graphs to see our logs using the EICAR Anti-malware Test File, to dive deep, Kindly click on one of the alerts.

![Threat Analysis Center: Threat Graphs for Threat Control Policy](image%20206.png)

Threat Analysis Center: Threat Graphs for Threat Control Policy

![Analysis for the ECIAR Anti-Malware Test File we used to validate the Threat Control Policy](image%20207.png)

Analysis for the ECIAR Anti-Malware Test File we used to validate the Threat Control Policy

![View from Sophos Endpoint Agent ](image%20208.png)

View from Sophos Endpoint Agent 

In conclusion, we configured Sophos Firewall using VMware and Validated Four (4) policies and tested them using the policy tester within Sophos.

We also installed the Sophos Endpoint Agent on a Windows 11 Machine and configured five (5) polices and validated them.