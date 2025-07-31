🧬 HTTP Packet Sniffer:

A Python script that captures HTTP requests and credentials on a local network interface. Works seamlessly with an ARP Spoofing tool to intercept and inspect web traffic.

📌 Description:

This packet sniffer monitors a network interface for HTTP traffic, extracting visited URLs and attempting to detect login credentials from raw packet data.

When used alongside an ARP Spoofer, this tool can act as a man-in-the-middle analyzer, giving you insight into plaintext network transmissions.

    ⚠️ Note: Only use this tool on networks you own or have explicit permission to test. Unauthorized interception of network traffic is illegal.

🚀 Features:

    Captures and logs HTTP request URLs

    Detects potential username/password data in HTTP payloads

    Works with ARP spoofing to intercept target traffic

    Filters and inspects only useful traffic (HTTP, not HTTPS)

🔧 Installation:

    git clone https://github.com/Nozarashi-1/packet-sniffer.git

    cd packet-sniffer

    pip install scapy

⚙️ Usage:
Run the sniffer and specify the network interface:

    sudo python packet_sniffer.py -i <interface>

🖇️ Combine with ARP Spoofing
To use this with your ARP Spoofer:

1.Start the ARP spoofing attack:

    sudo python arp_spoofer.py -t 192.168.1.5 -g 192.168.1.1

2.Then run the sniffer on the same interface:

    sudo python packet_sniffer.py -i eth0

🧪 Sample Output:

    [+] HTTP Request >> www.example.com/login
    [+] Possible username/password > b'username=admin&password=1234'

    
    
