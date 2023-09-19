# Networking Tools

Networking tools are used to troubleshoot network issues. They are also used to monitor network traffic and to test network connectivity. Some of the most common networking tools are:

- `traceroute` - Traces the route taken by packets over an IP network.
- `ping` - sends echo request packets to a host to test the Internet connection.
- `mtr` - Combines the functionality of traceroute and ping into a single diagnostic tool.
- `nmap` - Scans hosts for open ports.
- `netstat` - Displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
- `ufw and firewalld` - Firewall management tools.
- `iptables and nftables` - Firewall management tools.
- `tcpdump` - Dumps traffic on a network.
- `dig` - DNS lookup utility.
- `scp` - Secure copy.

## [Traceroute Command](https://linuxhint.com/run_traceroute_linux/)

`traceroute` command is a command in Linux that prints the route a network packet takes from its source (e.g. your computer) to the destination host (e.g., roadmap.sh). It is quite valuable in investigating slow network connections as it can help us spot the slow leg of the network packet journey through the internet.

## [Ping Command](https://linuxize.com/post/linux-ping-command/)

`ping` (**P** acket **In** ternet **G**roper) command is used to check the network connectivity between host and server/host. This command takes as input the IP address or the URL and sends a data packet to the specified address with the message “PING” and get a response from the server/host this time is recorded which is called latency.

## [Mtr Command](https://www.javatpoint.com/linux-mtr)

`mtr` combines the functionality of the traceroute and ping programs in a single network diagnostic tool.

## [Nmap Command](https://www.freecodecamp.org/news/what-is-nmap-and-how-to-use-it-a-tutorial-for-the-greatest-scanning-tool-of-all-time/)

NMAP stands for Network Mapper and is an open-source tool used to explore and audit the network’s security, such as checking firewalls and scanning ports.

## [Netstat Command](https://www.tutorialspoint.com/unix_commands/netstat.htm)

Netstat is a command line utility to display all the network connections on a system. It displays all the tcp, udp and unix socket connections. Apart from connected sockets it also displays listening sockets that are waiting for incoming connections.

## [Ufw Command](https://www.digitalocean.com/community/tutorials/ufw-essentials-common-firewall-rules-and-commands)

UFW, or uncomplicated firewall, is command-line based utility for managing firewall rules in Arch Linux, Debian and Ubuntu. It’s aim is to make firewall configuration as simple as possible. It is a frontend for the iptables firewalling tool.

## [IPtables Command](https://erravindrapawadia.medium.com/iptables-tutorial-beginners-to-advanced-guide-to-linux-firewall-839e10501759)

IPtables is a command-line firewall utility that uses policy chains to allow or block traffic that will be enforced by the linux kernel’s netfilter framework. Iptables packet filtering mechanism is organized into three different kinds of structures: tables, chains and targets. 

## [Tcpdump Command](https://danielmiessler.com/p/tcpdump/)

`tcpdump` is a command line tool used for analysing network traffic passing through your system. It can be used to capture and filter packets and display them in a human-readable format. The captured information can be analysed at a later date as well.

## [Dig Command](https://www.geeksforgeeks.org/dig-command-in-linux-with-examples/)

`dig` command stands for Domain Information Groper. It is used for retrieving information about DNS name servers. It is mostly used by network administrators for verifying and troubleshooting DNS problems and to perform DNS lookups. It replaces older tools such as `nslookup` and the `host`.

## [SCP Command](https://www.freecodecamp.org/news/scp-linux-command-example-how-to-ssh-file-transfer-from-remote-to-local/)

`SCP` is an acronym for Secure Copy Protocol.It is a command line utility that allows the user to securely copy files and directories between two locations usually between unix or linux systems.The protocol ensures the transmission of files is encrypted to prevent anyone with suspicious intentions from getting sensitive information.`SCP` uses encryption over an `SSH` (Secure Shell) connection, this ensures that the data being transferred is protected from suspicious attacks.
