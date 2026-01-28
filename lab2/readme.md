# Lab Report: Network Diagnostics and Troubleshooting CLI Tools

## 1. Experiment Objectives
The primary purpose of this lab was to familiarize ourselves with essential command-line interface (CLI) utilities available in the Windows operating system. The specific goals included:
* Gaining proficiency in executing standard network commands via the Command Prompt.
* Analyzing the output of various diagnostic tools to understand network behavior.
* Learning to identify, isolate, and resolve common connectivity issues.
* Verifying local network configurations and ensuring proper communication between devices.

## 2. Theoretical Background
Network administration relies heavily on the ability to diagnose issues quickly and accurately. While distinct graphical user interfaces exist, command-line tools offer granular control and immediate feedback regarding the state of the network. These commands operate at different layers of the OSI model to:
* Verify physical and logical connectivity.
* Inspect IP addressing and MAC layer details.
* Trace the path of data packets across the internet.
* Monitor active ports and sessions for security and performance.

All commands in this lab were executed using the Windows Command Prompt (cmd.exe).

## 3. Procedure
1.  The Windows Command Prompt was launched with administrative privileges where necessary.
2.  A series of standard diagnostic commands were executed sequentially.
3.  The output of each command was observed and analyzed to understand the current network state.
4.  Results were compared against expected theoretical outputs.

## 4. Command Analysis and Usage
The following table summarizes the commands tested during the session, including their syntax and primary function.

| Command | Syntax / Usage | Technical Description |
| :--- | :--- | :--- |
| **ping** | `ping <target_ip_or_domain>` | Sends ICMP Echo Request packets to a target to verify reachability and measure round-trip time (latency). |
| **tracert** | `tracert <target>` | Maps the route packets take to a destination, listing every router (hop) along the path. |
| **ipconfig** | `ipconfig /all` | Displays full TCP/IP configuration for all adapters, including IP address, Subnet Mask, Gateway, and DNS servers. |
| **nslookup** | `nslookup <domain>` | Queries the configured DNS server to resolve a hostname into an IP address or vice versa. |
| **netstat** | `netstat -a` | Lists all active TCP and UDP connections and the ports on which the computer is listening. |
| **pathping** | `pathping <target>` | Combines the features of ping and tracert to locate packet loss at specific hops over a period of time. |
| **route** | `route print` | Displays the local IP routing table, showing how the system decides where to send traffic. |
| **arp** | `arp -a` | Displays the ARP cache, which maps logical IP addresses to physical MAC addresses on the local network. |
| **hostname** | `hostname` | Returns the NetBIOS name of the local machine. |
| **getmac** | `getmac` | Retrieves the physical Media Access Control (MAC) address for all network interface cards. |
| **nbtstat** | `nbtstat -n` | Displays NetBIOS protocol statistics, specifically the local name table and current sessions. |

## 5. Discussion of Results
By executing these commands, we were able to validate several aspects of network communication:
* **Connectivity Verification:** Using `ping` and `tracert` allowed us to confirm that the host could reach external servers and visualize the path taken.
* **Configuration Auditing:** The `ipconfig /all` command provided essential details about the local interface, confirming that the DHCP server had assigned a valid IP and Gateway.
* **Name Resolution:** `nslookup` verified that the DNS server was functioning correctly by resolving domain names to IP addresses.
* **Security Monitoring:** `netstat` provided insight into which applications were communicating with the network, a critical step in identifying unauthorized connections.

## 6. Conclusion
This laboratory session successfully demonstrated the practical application of Windows network commands. We concluded that mastering these CLI tools is fundamental for any network administrator. They provide the most direct method for diagnosing connectivity failures, inspecting routing logic, and verifying hardware addresses, forming the basis of effective network troubleshooting.