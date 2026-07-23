# Network_Blog
Technical blog for Network VA/PT 

1. Introduction
   
Today, almost every organization depends on computer networks for its day-to-day operations. Whether it's accessing internal applications, sharing files, hosting websites, or communicating with employees across different locations, networks form the backbone of modern businesses. As organizations become more connected, the chances of cyber attacks also increase. Even a small security weakness in a network can become an entry point for an attacker.

This is where Vulnerability Assessment (VA) and Penetration Testing (PT) play an important role. A Vulnerability Assessment helps identify security weaknesses such as open ports, outdated software, or misconfigured services. Penetration Testing goes a step further by safely testing whether these weaknesses can actually be exploited. Together, they help organizations understand their security posture and fix issues before they can be misused by attackers.

Instead of focusing only on theory, this report takes a practical approach to understanding Network VA/PT. A virtual lab environment is used to perform different stages of a network assessment, including host discovery, port scanning, service enumeration, network traffic analysis, and vulnerability identification. The report also includes observations from each experiment, explains why the findings matter from a security perspective, and discusses possible mitigation techniques.

The main purpose of this report is to understand how a network security assessment is carried out in practice. Along with performing hands-on experiments using commonly used security tools, the report also includes research on the identified findings to better understand their potential impact and how they can be mitigated.


2. Network Vulnerability Assessment Methodology

Before testing the security of any network, it is important to follow a structured approach. Randomly scanning systems or attempting to exploit vulnerabilities can lead to incomplete results and unnecessary risks. A well-defined methodology helps ensure that the assessment is organized, repeatable, and focused on identifying genuine security issues.

In a typical Network Vulnerability Assessment and Penetration Test (VA/PT), the process begins by identifying the systems connected to the network. Once active hosts are discovered, the next step is to identify the open ports and the services running on them. These services are then analyzed for known vulnerabilities, after which the findings are validated and documented along with recommendations for remediation.

Planning

The first step is to define what will be assessed and choose the appropriate tools. Proper planning helps ensure that the assessment is carried out safely and systematically.

Host Discovery

Host discovery is performed to identify devices that are currently active on the network. This helps create an inventory of systems that may require further security testing.

Port Scanning

Once active hosts are identified, the next step is to scan them for open ports. Open ports indicate which services are accessible from the network and therefore represent potential entry points for attackers.

Service Enumeration

After identifying open ports, the services running on those ports are examined. Information such as service names, software versions, and operating system details can help determine whether any known vulnerabilities are present.

Vulnerability Identification

The discovered services are analyzed using vulnerability scanners and public vulnerability databases to identify known security issues. At this stage, the focus is on finding weaknesses rather than exploiting them.

Analysis and Reporting

The final step is to analyze the findings, understand their security impact, and recommend appropriate mitigation measures. A good report not only lists vulnerabilities but also explains why they matter and how they can be addressed.


3. VA vs PT : https://qualysec.com/what-is-the-difference-between-va-and-pt/

| Vulnerability Assessment                                | Penetration Testing                                                                              |
| ------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| Identifies security weaknesses in a network.            | Tests whether identified weaknesses can actually be exploited.                                   |
| Mainly focuses on discovery and analysis.               | Focuses on validating the real-world impact of vulnerabilities.                                  |
| Usually relies on automated tools.                      | Involves a combination of automated tools and manual testing.                                    |
| Produces a list of vulnerabilities with their severity. | Demonstrates the practical impact and provides proof of exploitation (within the defined scope). |


4. Discovering Active Hosts in the Network using Nmap
Objective

The first step in any network security assessment is to identify which devices are currently active on the target network. This process, known as Host Discovery, helps security professionals create an inventory of live systems before performing detailed scans. Without knowing which hosts are available, it is not possible to accurately assess the network's security.

In this experiment, Nmap (Network Mapper) was used to discover active hosts within the target network.

Tool Used
Tool: Nmap
Version: (Mention the version installed on your system, e.g., 7.97)
Operating System: (Kali Linux/macOS)

Command Used: 

Understanding the Command

The command uses the -sn option, also known as a Ping Scan. Instead of scanning ports, Nmap simply checks which devices on the specified subnet are active and responding. This makes it a quick and efficient way to discover hosts before moving on to more detailed scans.

Obersvations:

The scan successfully identified three active hosts on the target network. These included the default gateway (router) and two connected devices. Since the -sn option only performs host discovery, no information about open ports or running services was collected at this stage.

The discovered hosts provide the starting point for the next phase of the assessment, where individual systems will be scanned for open ports and running services.


Real Life case study: Mirai botnet
Reference link: https://www.cisecurity.org/insights/blog/the-mirai-botnet-threats-and-mitigations
                  https://www.youtube.com/watch?v=Lo40iZDrAQQ

The Mirai Botnet, first identified in 2016, is one of the most significant examples of how attackers leverage host discovery and service enumeration to compromise networked devices at scale. Mirai primarily targeted Internet of Things (IoT) devices such as IP cameras, routers, and digital video recorders (DVRs) that were accessible over the internet.

The malware continuously scanned public IP address ranges to identify live hosts exposing remote management services, particularly Telnet (TCP Port 23) and SSH (TCP Port 22). Once a responsive device was discovered, Mirai attempted to authenticate using a predefined list of common default usernames and passwords. Devices with weak or unchanged credentials were successfully compromised and incorporated into a botnet under the attacker's control.

The compromised devices were later orchestrated to launch large-scale Distributed Denial-of-Service (DDoS) attacks. One of the most notable incidents targeted Dyn, a major DNS service provider, disrupting access to popular online platforms such as Twitter, Netflix, Reddit, GitHub, and Spotify for several hours.

Attack flow: Image

Mirai Botnet Mitigations:

Segment your network – Ensure that all IoT devices are on a separate network from systems critical for daily operations.

Update IoT devices – Always keep IoT devices up to date to ensure there is less of a chance for infection.

Use and maintain anti-virus software – Anti-virus software recognizes and protects your computer against most known viruses. It is important to keep your anti-virus software up-to-date.



5. Port Scanning and Service Enumeration 
Reference: https://nmap.org/book/port-scanning-tutorial.html
            https://www.geeksforgeeks.org/ethical-hacking/port-scanning-techniques-by-using-nmap/

Once the active hosts were identified, the next step was to determine which ports were open and what services were running on those ports. Open ports represent the entry points through which systems communicate over a network. Identifying these ports helps security professionals understand the attack surface and identify services that may require further investigation.

Objective

To identify open ports on the target host and determine the services and software versions running on those ports.

Commands Executed
1. TCP SYN Scan :






6. Vulnerability detection using nuclei

7. Research based- Vulnerability Analysis

8. APT perspective of the steps performed

9. Security recommendations & best practices

10. 
   

