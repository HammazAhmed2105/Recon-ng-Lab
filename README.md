# Recon-ng-Lab
<h2>Lab Summary (What to expect) </h2>
In this lab, we will be utilizing Recon-ng on Kali Linux to automate the retrieval of WHOIS information for a target domain, using the example domain "facebook.com." The walkthrough includes creating a dedicated workspace, installing and configuring WHOIS search modules, and discovering valuable details such as location, contact information, and registration data. Additionally, readers will learn to leverage the HackerTarget.com API to identify subdomains associated with the target domain, providing insights into potential vulnerabilities for further exploration.

<h2>What is recon-ng </h2>
Recon-ng is an open-source web reconnaissance framework used for automating information gathering in penetration testing and ethical hacking.

<h2>Lab Objective </h2>
Finding whois information on a target domain using recon-ng.

<h2>Lab Purpose</h2>
WHOIS details encompass location, registration and expiration dates, contact particulars (email, phone numbers, etc.), and additional data related to domain names. This lab aims to employ recon-ng for the automated exploration and retrieval of such information.

<h2>Lab Tool</h2>
Kali Linux

<h2>TASK 1</h2>

- <b> Fire up your kali linux as root. (Use sudo -I in the terminal).</b>
- <b> Type in recon-ng as shown below. </b>
<img src="https://i.imgur.com/uMpPYPV.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<h2>TASK 2</h2>
- <b> We can create our own lab and workspace using recon-ng based on our project needs. Use the command “workspaces create whois _recon”</b>
<img src="https://i.imgur.com/f8BEDqM.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<h2>TASK 3</h2>

- <b>We will begin by gathering WHOIS information about a domain. WHOIS is publicly available hence we can perform it on any domain.</b>
- <b> First thing we need to do is install modules from the market place. Use the command “marketplace search whois”</b>
<img src="https://i.imgur.com/JFuddRt.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

- <b> We want to install the fourth option, which is “recon/domains-contacts/whois_pocs”. To do this, type “marketplace install recon/domains-contacts/whois_pocs” </b>
- <b>Then we load the module by using  “modules load recon/domains-contacts/whois_pocs” </b>
- <b> To begin searching using this module use the command “options set SOURCE facebook.com”. <b/>
<img src="https://i.imgur.com/arXffAB.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

- <b>To begin the search we simply need to write “run” and hit enter. This will display WHOIS information regarding the chosen domain(Facebook.com in this case).</b>
<img src="https://i.imgur.com/TxZMmZF.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

<h2>TASK 4</h2>
- <b>Our next step is to search for any domains using ip address of facebook. We will be importing Hackertarget.com API’s module for that.</b>

- <b>Type back, hit enter to quit out of whois_pocs module. Use the command “marketplace search hackertarget”. We only have one module that is recon/domains-hosts/hackertarget.</b>

- <b>To install it use “marketplace install recon/domains-hosts/hackertarget” and navigate to the module using “modules load  econ/domains-hosts/hackertarget”.</b>

<img src="https://i.imgur.com/m4wGQPr.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

- <b>Lastly all we need to do is type “run” and hit enter. You will notice several domains from facebook.com appears.</b>
<img src="https://i.imgur.com/fJhI8tj.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

This information can be useful for an attacker who may be targeting Facebook. They can use this information to attack the various subdomains and their IP addresses associated with Facebook, as they may not all be equally secure, to find a way through their security.
