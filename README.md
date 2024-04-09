# T-Pot-Honeypot-and-Attack-Map

# What is a Honeypot?

**What is a Honeypot?**

- **Decoy System:** A honeypot is a deliberately designed computer system or network segment that appears to be a legitimate, attractive target for cyberattacks. Its purpose is not to serve real users but to lure attackers.
- **Intelligence Gathering:** The main goal of a honeypot is to observe attacker behavior, tactics, techniques, and procedures (TTPs). By closely monitoring a honeypot, security teams can gain valuable insights into how attackers operate and the types of exploits they use.

**Examples**

- **Vulnerable Web Server:** A security team might deploy a web server with known vulnerabilities (e.g., outdated software or weak configurations). Attackers scanning for those vulnerabilities would stumble upon this server, believing it's a legitimate target. The security team then observes the attack attempts, gathering data on the attacker's tools and methods.
- **Fake Financial Database:** An organization could set up a honeypot mimicking a financial database, complete with seemingly valuable records. Attempts to access or exfiltrate data from this database would immediately raise red flags, revealing potential malicious activity and the attacker's techniques.

**Memory Recall: The Bear and the Honey**

Think of a honeypot like a jar of honey strategically placed in the woods. A bear, attracted to the sweet smell, will try to get the honey. This allows you to observe the bear's behavior, its methods (how it tries to open the jar), and potentially identify the bear itself. Similarly, a honeypot lures in attackers, providing a safe space to study their actions.

## Prerequisites

- Server Provider
	- I will be using Vultr's services to minimize server cost in-result making this Honey Lab project free. (To receive $100 of credit use this referral link: https://www.vultr.com/?ref=9605787-8H)

### Step 1: Building the Cloud Computer


1. Go to https://my.vultr.com/ and click on "Product" > "Cloud Computer - Shared CPU" > Select the server location nearest to you!

2. Upload the ISO Image
   
   ISO Image Link: https://objects.githubusercontent.com/github-production-release-asset-2e65be/27275442/a9bab481-a247-4f60-bd33-8c7a590443d8?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240408%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240408T154903Z&X-Amz-Expires=300&X-Amz-Signature=9ba1fd8fe40d0b05c61c8223c28fb93a2ea5f4f2f1644f2e71de784875c6644c&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=27275442&response-content-disposition=attachment%3B%20filename%3Dtpot_amd64.iso&response-content-type=application%2Foctet-stream


3. Once you have uploaded the "tpot_amd64" iso proceed to choose your preferred cloud server specifications. ( I have chosen "Regular Cloud Computer > 160GB SSD > Disabled "Auto Backups").


4. Enter your Server Host Name & deploy the machine.





We will be using "View Console" to interact with our Honeypot Installation


### Step 3: Implementing Firewall Rules
1. Go to your Honeypot and click on Settings > Firewall > Firewall (Manage) > Add Firewall Group


Include a description for your Firewall Group

1. Protocol - TCP | Port (or Range) - 1:65535 | Source: My IP | Click "Add Firewall Rule"


2. Protocol - UDP | Port (or Range) - 1:65535 | Source: My IP | Click "Add Firewall Rule"



Click on "Firewall" and Select the Firewall Group you have just recently created and update.


### Step 3: Installing T Pot Framework



### T-Pot Framework


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

1. Click on "Attack Map"




### Step 5: Kibana: Visualization/Dashboard

---

# 10 hours later...


---

# Analyze the data


Honeypot dashboards are designed to give you insights into the types of attacks and attackers targeting your network. Here are some of the key questions you might want to ask, with a focus on what the dashboard can help you answer:

**Types of Attacks**

- **What are the most common attack vectors?** Are attackers trying to exploit web vulnerabilities, brute force SSH logins, or target other specific services?
- **Are there any new or unusual types of attacks?** Have new attack patterns recently emerged?
- **What is the overall volume of attacks?** Are attacks increasing or decreasing in intensity?


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

---
**Attacker Origins**

- **Where are attacks originating from (geographically)?** Can you identify specific countries or regions with higher concentrations of attacks?

- **Are there any repeat offenders (IP addresses)?** Can you identify individual IP addresses that are repeatedly attacking, indicating a persistent threat actor?

---


**Attack Sophistication**

- **Are the attacks mostly automated scripts or more targeted attempts?** Are you seeing simple, unsophisticated attacks, or evidence of attackers using complex tools and techniques?
- **Are there attempts to disguise the attacker's activity?** Are they using anonymization tools or proxies?

---


**Vulnerabilities**

- **Which services or ports are being targeted most frequently?** This will highlight potential weak areas in your network.
-Port 6000 & 8080

- **Are any attacks successful?** If so, it reveals an immediate need to address and patch those vulnerabilities.

---



**Typical Dashboard Features**

A good honeypot dashboard should help you visualize this information. Common features include:

- **Maps:** Showing geographic origin of attacks
- **Attack timelines:** Illustrating the frequency and intensity of attacks over time
- **Top attacked services/ports:** Listing the most frequent attack targets
- **Alerts:** Highlighting critical events or especially sophisticated attacks
- **Detailed logs:** Providing raw data for deeper analysis

**Important Considerations**

- **Interaction vs. Production Honeypots:** Is your honeypot designed primarily for research and observation, or is it supposed to simulate a real production system? The questions you ask will depend on the type of honeypot.
- **Dashboard Customization:** Can you filter and customize the views on your dashboard to focus on the most relevant data?
