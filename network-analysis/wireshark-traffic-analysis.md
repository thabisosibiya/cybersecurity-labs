# Network Traffic Analysis with Wireshark

## Objective
The goal of this lab was to install and use Wireshark to capture and analyse network traffic. This included setting up permissions, launching the tool, generating traffic, and inspecting packets.

---

## Installing Wireshark

Before using Wireshark, I needed to install it using the apt package manager.

### Update Package List

```
sudo apt update
```
This ensures the system has the latest package information.

## 1. Install Wireshark
```
sudo apt install wireshark -y
```
The -y flag skips confirmation prompts.

## 2. Verify Installation
```
wireshark --version
```
This confirms that Wireshark is installed correctly.

## 3. Configuring Wireshark Permissions
By default, capturing packets requires root privileges. To avoid running Wireshark as root, I configured permissions for a normal user.

Check if Wireshark group exists
```
getent group wireshark
```

Create group (if needed)
```
sudo groupadd wireshark
```

Assign permissions to dumpcap
```
sudo chgrp wireshark /usr/bin/dumpcap
```

```
sudo chmod 4755 /usr/bin/dumpcap
```

## 4. Add user to Wireshark group
```
sudo gpasswd -a $USER wireshark
```

## 5. Apply changes
```
newgrp wireshark
```

## 6. Verify group membership
```
groups
```

## 7. Launching Wireshark 
Wireshark can be launched either from the GUI or terminal.

Launch via terminal
```
wireshark
```

## 8. Understanding the Interface

The interface consists of:
1. Packet List Pane - shows captured packets
2. Packet Details Pane - shows protocol breakdown
3. Packet Bytes Pane - raw data of packets

## 9. Capturing Network Traffic
To capture traffic, I selected a network interface (eth0) and started capturing.

## 10. Generating Traffic

To generate traffic for analysis, I used:
```
ping -c 5 google.com
```
This sends ICMP packets which can then be analysed in Wireshark.

## 11. Stopping the Capture
Capture can be stopped using the stop button in Wireshark.

## 12. Filtering Traffic

To focus on ICMP packets, I applied a filter:
icmp
This displays only ping-related traffic.

## 13. Inspecting Packets

By selecting a packet, I was able to analyse:
1. Frame details
2. Ethernet layer
3. IP layer
4. ICMP protocol

This helped me understand how packets are structured and transmitted.

## What I learned

1. How to install and configure Wireshark
2. How to safely capture packets without root
3. How to generate and analyse network traffic
4. How to filter and inspect specific protocols
5. How packet data is structured across layers

## Real-World Application 
Wireshark is used by network engineers and security professionals to analyse traffic, troubleshoot issues, and detect suspicious activity on a network.

---

# Conclusion

This lab gave me a strong introduction to network traffic analysis. I learned how to capture packets, filter traffic, and inspect protocol-level data, which is essential for both networking and cybersecurity.
