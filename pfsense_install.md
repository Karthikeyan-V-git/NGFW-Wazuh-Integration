# Prerequisites

**Download pfSense ISO:**

Go to the pfSense download page to get the latest pfSense ISO.
Choose the appropriate architecture (usually AMD64 for most modern systems).
Select ISO installer (CD Image) for installation.
https://shop.netgate.com/products/netgate-installer

**VirtualBox Installation:**

If you haven't already, download and install VirtualBox.

**Hardware Requirements:**
For pfSense to run smoothly in VirtualBox, your system should meet these minimum requirements:

- RAM: 1 GB (recommended 2 GB or more for better performance)
- CPU: Any modern x86_64 processor (AMD or Intel)
- Storage: At least 4 GB of free space (for pfSense OS installation)
- Network Interfaces: At least 2 virtual network interfaces (WAN and LAN)
  
## Steps to Add pfSense in VirtualBox
**Create a New Virtual Machine:**

- Open VirtualBox and click on New.
  Set the VM name (e.g., pfSense), select BSD as the type, and FreeBSD (64-bit) as the version.
  Click Next.
  **Allocate RAM:**
  Assign at least 1 GB of RAM (preferably 2 GB if possible).

- **Create a Virtual Hard Disk:**

  Choose Create a virtual hard disk now.
  Select VDI (VirtualBox Disk Image) as the disk type.
  Set dynamically allocated storage.
  Allocate at least 4 GB for the disk size.
  Attach the pfSense ISO:
  In the VM settings, go to System > Optical and add the pfSense ISO file you downloaded earlier.
  
- **Add Network Interfaces:**

  Go to Network in VM settings.
  WAN (Bridge Mode): Select Adapter 1, attach it to Bridged Adapter to allow the VM to access the external network (your physical network).
  LAN (Internal Network): Select Adapter 2, set it to Internal Network. This network will be used for communication between the pfSense VM and any internal machines you want to add to your network.
  
- **Network Configuration (WAN and LAN):**
  
**WAN (Bridge Mode):**

The WAN interface should be connected to your physical network or the internet. In VirtualBox, this is done by setting the interface to Bridged Adapter, which makes the pfSense VM behave like a regular device on your physical network.

**LAN (Internal Network):**

The LAN interface is configured to use the Internal Network setting. This makes pfSense act as the gateway between your internal network and the outside world. Machines connected to the LAN network in VirtualBox can communicate with pfSense but won't have direct access to the host machine's network.


- **Start pfSense Installation:**

**Start the VM:**

Once the virtual machine is created and configured, click Start to boot the VM from the ISO.

Install pfSense:

Follow the on-screen prompts to install pfSense onto the virtual disk.
Select the default option for installation (usually Install pfSense).
Follow the prompts to choose disk partitions, and then let the system install pfSense.

Initial Setup:

After installation, pfSense will prompt you to configure the WAN and LAN interfaces.
Set the WAN interface to DHCP to automatically receive an IP address from your physical network.
Set up a static IP for the LAN network (e.g., 192.168.1.1/24).
Post-Installation:
Access the Web Interface:

After installation, pfSense will show you a message with the LAN IP address (e.g., 192.168.1.1).
Open a web browser and go to https://192.168.1.1 (or whatever the IP is).
Log in using the default credentials:
Username: admin
Password: pfsense
Finalize Configuration:

Configure WAN settings, DNS, and firewall rules as required for your network setup.
Once set up, pfSense will manage traffic between the WAN and LAN interfaces, and you can add internal machines to the LAN network for monitoring or testing.
