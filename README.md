# # T-Pot-Honeypot-and-Attack-Map

![AttackMap](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/vivaldi_dWaAODVwOG.png?raw=true)

## Objective

My aim is to enhance my proficiency in cybersecurity threat analysis utilizing the Kibana platform. I will develop the ability to interpret data visualizations within Kibana, analyze global attack trends using real-time mapping, and leverage Kibana to pinpoint attack vectors directed toward my network. This practical experience will strengthen my skills in constructing custom Kibana dashboards, empowering me to derive actionable insights regarding potential vulnerabilities within my infrastructure.

### Skills Learned
- **Installation and Configuration**: Setting up and configuring the Teapot honeypot platform.
- **Firewall Configuration**: Modifying firewall rules to allow inbound access to the Honeypot.
- **Web Portal Access**: Accessing and navigating the web portal of the Honeypot platform.
- **Cybersecurity Analysis**: Analyzing real-time attack data using tools like the Attack Map and Kibana dashboard.
- **Querying Data**: Practicing querying skills in Kibana to extract relevant information.
- **Data Visualization**: Interpreting and understanding visualizations such as attack maps, heat maps, and IP reputation data.
- **Security Monitoring**: Monitoring and analyzing incoming attacks and their sources.
- **IP Reputation Analysis**: Checking the reputation of source IPs involved in attacks.
- **Hands-on Experience**: Gaining practical experience with Honeypot deployment, monitoring, and analysis.
### Tools Used
- **Teapot**: All-in-one multi-Honeypot platform
- **GitHub**: Documentation and resources access
- **Elasticsearch**: Data querying and storage
- **Kibana**: Web GUI for Elasticsearch, data querying, and visualization
- **SpiderFoot**: Collection of OSINT tools for gathering information
- **Firewall Management Tool**: Configuration of firewall rules for inbound access control

I will be using Vultr's services to minimize server cost in-result making this Honey Lab project free. 
Registration link to recieve $100 of credit: https://www.vultr.com/?ref=9605787-8H

These tools are essential for deploying, monitoring, analyzing, and visualizing data related to cyber threats and attacks, providing a comprehensive suite for cybersecurity analysis and defense.

## Honeypot

**What is a Honeypot?**

- **Decoy System:** A honeypot is a deliberately designed computer system or network segment that appears to be a legitimate, attractive target for cyberattacks. Its purpose is not to serve real users but to lure attackers.
- **Intelligence Gathering:** The main goal of a honeypot is to observe attacker behavior, tactics, techniques, and procedures (TTPs). By closely monitoring a honeypot, security teams can gain valuable insights into how attackers operate and the types of exploits they use.

**Examples**

- **Vulnerable Web Server:** A security team might deploy a web server with known vulnerabilities (e.g., outdated software or weak configurations). Attackers scanning for those vulnerabilities would stumble upon this server, believing it's a legitimate target. The security team then observes the attack attempts, gathering data on the attacker's tools and methods.
- **Fake Financial Database:** An organization could set up a honeypot mimicking a financial database, complete with seemingly valuable records. Attempts to access or exfiltrate data from this database would immediately raise red flags, revealing potential malicious activity and the attacker's techniques.

**Memory Recall: The Bear and the Honey**

Think of a honeypot like a jar of honey strategically placed in the woods. A bear, attracted to the sweet smell, will try to get the honey. This allows you to observe the bear's behavior, its methods (how it tries to open the jar), and potentially identify the bear itself. Similarly, a honeypot lures in attackers, providing a safe space to study their actions.

## Steps

### Step 1: Deploying New Instance

![Deploy1](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy1.png?raw=true)
**1. Go to https://my.vultr.com/ and click on "Product" > "Cloud Computer - Shared CPU" > Select the server location nearest to you!**


![Deploy2](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy2.png?raw=true)
**2. Upload and select "tpot_amd64.iso" as the image.**


![Deploy3](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy3.png?raw=true)
**3. Choose the "Regular Cloud Compute Plan" > 160GB SSD**


![Deploy4](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy4.png?raw=true)
**4. Disable Both Auto Backups & IPv6***


![Deploy5](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy5.png?raw=true)
**5. Insert your Honeypot Server Hostname & Deploy**


![Deploy6](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy6.png?raw=true)
**6. Click on your Honeypot once the status displays "Running"

![Deploy7](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy7.png?raw=true)

![Deploy8](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy8.png?raw=true)
**7. Settings > Firewall > (Manage) > Add Firewall Group > Enter Firewall Group Description**

![Deploy9](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Deploy9.png?raw=true)

**8. Once you have created these Firewall Rules > Select "Compute" > Setting > Firewall > Select the Honeypot Firewall you have created**
### Step 3: Installing T Pot Framework

![InstallingFirewall1](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212721.jpg?raw=true)

![InstallingFirewall2](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212732.jpg?raw=true)

![InstallingFirewall3](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212743.jpg?raw=true)

![InstallingFirewall4](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212753.jpg?raw=true)

![InstallingFirewall5](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212807.jpg?raw=true)

![InstallingFirewall6](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212819.jpg?raw=true)

![InstallingFirewall7](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212829.jpg?raw=true)

![InstallingFirewall8](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212839.jpg?raw=true)

![InstallingFirewall9](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212850.jpg?raw=true)

![InstallingFirewall10](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212913.jpg?raw=true)

![InstallingFirewall11](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408212921.jpg?raw=true)




### T-Pot Framework

![TPotFramework](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408213405.jpg?raw=true)


**Core Concepts**

- **Security Information and Event Management (SIEM):** A system that helps centralize and analyze security logs/events from different sources. This is important for gaining visibility into potential threats.
- **Open Source Intelligence (OSINT):** The practice of gathering and analyzing publicly available information to gain insights.

**Specific Tools**

- **Attack Map:** A visual representation of cyberattacks occurring globally and potentially against your own infrastructure. It can show:
    
    - Attack types (DoS, Malware, etc.)
    - Attack origin and target countries
    - Trends in attack activity
- **Cockpit:** Serves as your administrative control panel for the "teapot" system (the name might be specific to their setup). This is where you'd likely:
    
    - Configure settings
    - Monitor system resources
    - Add or remove tools
- **CyberChef:** A versatile web-based utility for performing all sorts of data manipulations. Think of it as a powerhouse for:
    
    - Encryption and decryption
    - Encoding and decoding (like Base64)
    - Data format conversions
    - Compression/decompression
- **Elastic View:** A web-based frontend (i.e., a graphical user interface) designed to work specifically with Elasticsearch. Elasticsearch is a powerful search and analytics engine, and is commonly used within SIEM systems.
    
- **Kibana:** The official visualization and data exploration tool designed to work with Elasticsearch. You use it to:
    
    - Query the data stored in Elasticsearch
    - Build dashboards and charts to get insights from the data
- **SpiderFoot:** An extensive OSINT tool with many modules to collect data about a target. It can:
    
    - Scan for email addresses, usernames, and domains associated with your target
    - Map web server relationships
    - Identify technologies in use on websites

### Step 4: Expose Our Machine to the World

Change the existing Firewall Rule to match the following:
![ExposeMachine1](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/ExposeMachine1.png?raw=true)



### Step 5: Kibana: Visualization/Dashboard

![Kibana1](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408214503.jpg?raw=true)
![Kibana2](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/Pasted%20image%2020240408214615.jpg?raw=true)

---

# 12+ hours later...
![After](https://github.com/CySAJohnseun/T-Pot-Honeypot-and-Attack-Map/blob/main/images/After.png?raw=true)

---

# Data Interpretation

## Favorable Attacks by Destination Ports: 6000 & 8080

#### Port 6000: The default port used for communication by the X Window System (X11 or Xorg). What is X11? A graphical display system common on Unix-based operating systems. It allows users to run applications with graphical interfaces on a remote server, displaying those interfaces on their local machine.

- **Open by Default:** The X Window System (X11 or Xorg) uses port 6000 by default. This means that if X11 is installed and running, there's a high chance that port 6000 will be open and listening for connections.
- **Historically Insecure Configurations:** Older versions of X11 often had very permissive default security settings. They might allow connections from any remote system with little to no authentication in place.
- **Remote Access Functionality:** The core purpose of X11 is to allow remote access to graphical interfaces. This means it's designed to accept connections from outside the local machine, potentially exposing it to the entire internet.
- **Prevalence:** X11 has been a common graphical environment for Unix-based systems for a long time, making it a widely deployed service on many machines.
- **Potential Vulnerabilities:** Like any software, X11 might have vulnerabilities that attackers can exploit. If port 6000 is open and X11 is running an older or insecure version, it increases the risk of compromise.

**How Attackers Exploit This:**

1. **Scanning:** Attackers frequently scan the internet for machines with port 6000 open. This indicates systems potentially running X11.
2. **Version Identification:** If the service responds, attackers may try to determine the X11 version to see if they can find known vulnerabilities to exploit.
3. **Unauthorized Access:** If the X11 security configuration is weak, attackers might gain remote access to the machine's graphical interface.
4. **Privilege Escalation:** Once an attacker has access to the graphical environment, they may be able to exploit other software or system vulnerabilities to gain higher privileges and full control.

#### Port 8080: A common alternative port for web servers using the HTTP (Hypertext Transfer Protocol). This is the protocol that powers your web browsing.
- **Common Alternative for HTTP:** Port 8080 is a popular alternative port for web servers that use the HTTP protocol. Attackers know many less-sophisticated setups use it in place of the standard port 80.
- **Potential Vulnerabilities in Web Applications:** Often, web servers running on port 8080 host web applications. These applications may have vulnerabilities (like SQL injection or cross-site scripting) that attackers hope to exploit. If successful, they might gain unauthorized access, steal data, or inject malicious code.
- **Proxy Servers:** Port 8080 is sometimes used for HTTP proxy servers. Attackers might target these to disguise their own activity, launch attacks from the compromised proxy, or disrupt proxy services.
- **Weaker Security Assumptions:** Since port 8080 is non-standard, system administrators might wrongly assume it's less targeted than port 80. This can lead to less rigorous security measures being applied to services running on port 8080.
- **Automated Scans:** Many attacks are carried out by automated scripts and bots that systematically scan the internet for open ports. They often try a range of common ports, including 8080, regardless of the specific service running on them.

**Important Note:** While attackers frequently target port 8080, the reasons outlined above mean that _any_ web-facing service on _any_ port can be a target. Simply using a non-standard port does not make it magically more secure.
## Attacker Origins

- **Where are attacks originating from (geographically)?** Can you identify specific countries or regions with higher concentrations of attacks?

- **Are there any repeat offenders (IP addresses)?** Can you identify individual IP addresses that are repeatedly attacking, indicating a persistent threat actor?


## Vulnerabilities

- **Which services or ports are being targeted most frequently?** This will highlight potential weak areas in your network.
-Port 6000 & 8080

- **Are any attacks successful?** If so, it reveals an immediate need to address and patch those vulnerabilities
