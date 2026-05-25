# Network Traffic Analysis and Intrusion Detection

## Objective
Capture and analyze network traffic using Wireshark, tcpdump, and Snort to identify suspicious activities.

## Tools Used
- Wireshark
- tcpdump
- Snort
- Nmap
- Kali Linux

## Features
- Packet Capture
- Traffic Analysis
- Threat Detection
- Intrusion Detection
# Network Traffic Analysis and Intrusion Detection

## Objective
The objective of this project is to capture, monitor, and analyze network traffic to identify suspicious activities and potential attacks using Wireshark, tcpdump, Snort, and Nmap.

---

## Tools Used
- Wireshark
- tcpdump
- Snort IDS
- Nmap
- Kali Linux

---

## Features
- Live packet capture
- TCP/IP traffic analysis
- DNS and HTTP traffic monitoring
- SYN scan detection
- Suspicious traffic identification
- Intrusion Detection System (IDS) monitoring

---

## Project Structure

Network-Traffic-Analysis/
│
├── captured_packets/
├── screenshots/
├── logs/
├── snort_rules/
├── reports/
└── README.md

---

- Installed Wireshark, tcpdump, Snort, and Nmap
- Captured live network traffic using tcpdump
- Analyzed packets in Wireshark
- Applied filters for DNS, TCP, HTTP, and ICMP traffic
- Created project folder structure

---

### Attack Simulation
Simulated suspicious network activity using Nmap SYN scan:

bash
nmap -sS localhost


# Network Traffic Analysis and Intrusion Detection

## Objective
The objective of this project is to capture, monitor, and analyze network traffic to identify suspicious activities and potential attacks using Wireshark, tcpdump, Snort, and Nmap.

---

## Tools Used
- Wireshark (Network packet analysis)
- tcpdump (Packet capture)
- Snort IDS (Intrusion detection)
- Nmap (Network scanning)
- Kali Linux

---

## Features
- Live packet capture using tcpdump  
- Packet-level analysis using Wireshark  
- Detection of suspicious TCP SYN scan activity  
- Intrusion detection using Snort IDS  
- Analysis of DNS, TCP, HTTP, and ICMP traffic  
- Identification of reconnaissance behavior  

---

## Project Structure

Network-Traffic-Analysis/  
│  
├── captured_packets/  
├── screenshots/  
├── logs/  
├── snort_rules/  
├── reports/  
└── README.md  

---

## Methodology

### Packet Capture
Network traffic was captured using tcpdump and saved as `.pcap` files for further analysis.

bash
sudo tcpdump -i any -w captured_packets/traffic.pcap

## Traffic Analysis using Wireshark
Captured packets were analyzed using Wireshark by applying filters such as:

tcp
dns
http
icmp
tcp.flags.syn == 1
tcp.flags.syn == 1 && tcp.flags.ack == 0
Wireshark helped identify:

# Source and destination IP addresses

## Protocol types

Suspicious packet behavior

TCP handshake patterns

Attack Simulation using Nmap
A SYN scan was performed to simulate suspicious network activity:

nmap -sS localhost
This generated multiple SYN packets targeting different ports.

Intrusion Detection using Snort
Snort IDS was configured to monitor network traffic and detect suspicious activity.

### Custom rule used:

alert tcp any any -> any any (msg:"Possible Port Scan Detected"; flags:S; sid:1000001; rev:1;)
Snort was executed using:

sudo snort -R /etc/snort/rules/local.rules -i eth0 -A fast
Snort monitored traffic and processed TCP scan activity.

## Findings

- Multiple TCP SYN packets were observed targeting different ports
- Repeated connection attempts indicated port scanning behavior
- Suspicious reconnaissance activity was identified
- Wireshark successfully visualized packet-level traffic
- Snort IDS monitored and analyzed network traffic

## Important Wireshark Filters

- Filter	Purpose
- tcp	Show TCP traffic
- dns	Show DNS packets
- http	Show HTTP traffic
- icmp	Show ICMP packets
- tcp.flags.syn == 1	Show SYN packets
- tcp.flags.syn == 1 && tcp.flags.ack == 0	Detect SYN scan


## Skills Learned

- Network Traffic Analysis
- Packet Inspection
- TCP/IP Fundamentals
- Intrusion Detection Systems
- Port Scan Detection
- Cybersecurity Monitoring
- Wireshark Analysis
