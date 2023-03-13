 <h1 align="center">
  <br>
<img src="https://github.com/Pandya-mayur/Reconvenger/blob/main/Image.png"></a>
</h1>
<h4 align="center">Streamline your recon and vulnerability detection process with reconvenger,
A recon and initial vulnerability detection tool built using shell script and open source tools.</h4>


<p align="center">
<a><img title="Made in INDIA" src="https://img.shields.io/badge/MADE%20IN-INDIA-SCRIPT?colorA=%23ff8100&colorB=%23017e40&colorC=%23ff0000&style=for-the-badge"></a>
</p>


<p align="center">
  <a href="#how-it-works-">How it works</a> •
  <a href="#install-reconvenger">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#modes">MODES</a> •
  <a href="#for-developers">For Developers</a> •
  <a href="#credits">Credits</a> 
</p>

---
</p>

 
Introducing reconvenger, a powerful recon and initial vulnerability detection tool for Bug Bounty Hunters. Built using a variety of open-source tools and a shell script, reconvenger allows you to quickly and efficiently run a scan on the target domain and identify potential vulnerabilities.

reconvenger begins by performing recon on the target system, collecting information such as subdomains, and running services with nuclei. It then uses this information to scan for known vulnerabilities and potential attack vectors, alerting you to any high-risk issues that may need to be addressed.

In addition, reconvenger also includes features for identifying misconfigurations and insecure default settings with nuclei templates, helping you ensure that your systems are properly configured and secure.

reconvenger is an essential tool for conducting thorough and effective recon and vulnerability assessments.
Let's Find Bugs with reconvenger

[Thanks ChatGPT for the Description]
  

  
## How it Works ?
This tool mainly performs 3 tasks
1. Effective Subdomain Enumeration from Various Tools
2. Get URLs with open HTTP and HTTPS service.
3. Run a Nuclei and other scans on previous output
So basically, this is an autmation script for your initial recon in bugbounty
  
## Install Reconvenger
   reconvenger requires different tools to run successfully. Run the following command to install the latest version with all requirments-

 ```sh
git clone https://github.com/Pandya-mayur/Reconvenger
cd reconvenger
bash installer.sh
```
  
## Usage 

```sh
reconvenger -h
```
This will display help for the tool. Here are all the switches it supports.
  
```console
[ABOUT:]
   Streamline your recon and vulnerability detection process with reconvenger,
   A recon and initial vulnerability detection tool built using shell script and open source tools.


[Usage:]
   reconvenger [MODE] [FLAGS]
   reconvenger -m EXP -d target.com -c /path/to/config.yaml


[MODES:]
    ['-m'/'--mode']
         Available Options for MODE: 
         SUB | sub | SUBDOMAIN | subdomain           Run reconvenger in SUBDOMAIN ENUMERATION mode
         URL | url                                   Run reconvenger in URL ENUMERATION mode
         EXP | exp | EXPLOIT | exploit               Run reconvenger in Full Exploitation mode


         Feature of EXPLOI mode :                    subdomain enumaration, URL Enumeration,
                                                     Vulnerability Detection with Nuclei,
                                                     and Scan for SUBDOMAINE TAKEOVER

[FLAGS:]
    [TARGET:]   -d, --domain    target domain to scan

    [CONFIG:]   -c, --config    path of your configuration file for subfinder

    [HELP:]     -h, --help      to get help menu  
      
    [UPDATE:]   -u, --update    to update tool
  
[Examples:]
     Run reconvenger in full Exploitation mode
         reconvenger -m EXP -d target.com


     Use your own CONFIG file for subfinder
         reconvenger -m EXP -d target.com -c /path/to/config.yaml


     Run reconvenger in SUBDOMAIN ENUMERATION mode
         reconvenger -m SUB -d target.com


     Run reconvenger in URL ENUMERATION mode
         reconvenger -m SUB -d target.com

```

  
## MODES 
### 1. FULL EXPLOITATION MODE <br>
Run reconvenger in FULL EXPLOITATION MODE
```sh
  reconvenger -m EXP -d target.com
```
  
FULL EXPLOITATION MODE contains following functions
- Effective Subdomain Enumeration with different services and open source tools
- Effective URL Enumeration ( HTTP and HTTPs service )
- Run Vulnerability Detection with Nuclei
- Subdomain Takeover Test on previous results
<br>
  
### 2. SUBDOMAIN ENUMERATION MODE <br>
Run reconvenger in SUBDOMAIN ENUMERATION MODE
```sh
  reconvenger -m SUB -d target.com
```
SUBDOMAIN ENUMERATION MODE contains following functions
- Effective Subdomain Enumeration with different services and open source tools
- You can use this mode if you only want to get subdomains from this tool
  or we can say Automation of Subdmain Enumeration by different tools
<br>
  
### 3. URL ENUMERATION MODE <br>
Run reconvenger in URL ENUMERATION MODE
```sh
  reconvenger -m URL -d target.com
```
URL ENUMERATION MODE contains following functions
  - Same Feature as SUBDOMAIN ENUMERATION MODE but also identifies HTTP or HTTPS service
  
Using your own CONFIG File for subfinder
```sh
  reconvenger -m EXP -d target.com -c /path/to/config.yaml
```
You can also provie your own CONDIF file with your API Keys for subdomain enumeration with subfinder
  
Updating tool to latest version
You can run following command to update tool
```sh
  reconvenger -u
```

An Example of config.yaml
```yaml
binaryedge:
  - 0bf8919b-aab9-42e4-9574-d3b639324597
  - ac244e2f-b635-4581-878a-33f4e79a2c13
censys:
  - ac244e2f-b635-4581-878a-33f4e79a2c13:dd510d6e-1b6e-4655-83f6-f347b363def9
certspotter: []
passivetotal:
  - sample-email@user.com:sample_password
securitytrails: []
shodan:
  - AAAAClP1bJJSRMEYJazgwhJKrggRwKA
github:
  - ghp_lkyJGU3jv1xmwk4SDXavrLDJ4dl2pSJMzj4X
  - ghp_gkUuhkIYdQPj13ifH4KA3cXRn8JD2lqir2d4
zoomeye:
  - zoomeye_username:zoomeye_password
```
  
## For Developers
If you have ideas for new functionality or modes that you would like to see in this tool, you can always submit a pull request (PR) to contribute your changes.
  
  
## Credits
I would like to express my gratitude to all the team members of The Linux boys and all the open source projects that have made this tool possible and have made recon tasks easier to accomplish.
