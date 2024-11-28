# NGFW-Wazuh-Integration
This project focuses on configuring a Next-Generation Firewall (NGFW) and integrating it with Wazuh, a security monitoring and management platform.

<img src="/assets/intro.webp" width="800"/>

The primary objective is to establish a secure network environment by:

- **Configuring an NGFW to manage and secure network traffic.**
- **Adding a client machine under the NGFW's protection.**
- **Monitoring both the NGFW and the client machine using Wazuh to ensure network visibility, detect threats, and respond effectively.**

The project provides a hands-on implementation of modern cybersecurity practices, suitable for network security enthusiasts and learners.

**Key Features:**

**NGFW Setup:**

- Deploy and configure a firewall with IDS/IPS capabilities (e.g., pfSense or a commercial NGFW).
- Define and enforce firewall policies to secure the network.

**Monitoring with Wazuh:**

- Collect and analyze NGFW logs through Syslog integration with Wazuh.
- Install and configure the Wazuh agent on the client machine for in-depth system monitoring.
    
**Security Analysis:**

- Centralize and correlate logs for both the NGFW and the client machine.
- Enable real-time alerting for network intrusions, suspicious activity, and system vulnerabilities.


# Pfsense
Is an open-source firewall and router software distribution based on FreeBSD. It is widely used for securing networks, managing traffic, and monitoring connections. It can be configured to act as a Next-Generation Firewall (NGFW) when combined with additional features like Intrusion Detection Systems (IDS), Intrusion Prevention Systems (IPS), and traffic monitoring tools.

<img src="/assets/PfSense.png" width="800"/>

**Key Features of pfSense:**

**- Firewall Capabilities:**
Stateful packet filtering, NAT, VLAN support, and web filtering (Squid proxy, SquidGuard).

**- VPN Support:**
IPsec and OpenVPN for secure remote and site-to-site VPN connections.

**- IDS/IPS (Snort/Suricata):**
Real-time threat detection and prevention, blocking malicious traffic.

**- Traffic Shaping & QoS:**
Prioritize critical traffic and manage bandwidth for non-essential services.

**- User Authentication:**
Local or external authentication (LDAP, RADIUS).

**- Web Interface & Dashboard:**
Easy-to-use GUI for configuration, monitoring, and real-time traffic analysis.

**- High Availability (HA):**
Failover with CARP for continuous network availability.

**- Traffic Logging:**
Log forwarding to external systems like Wazuh, Splunk, or Graylog for centralized monitoring.

[Installation and Configuration](pfsense_installation.md)
