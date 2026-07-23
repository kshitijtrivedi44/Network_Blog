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
