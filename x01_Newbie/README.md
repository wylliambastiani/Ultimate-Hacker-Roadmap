# The Newbie's Handbook - Level 2
So you've looked over the laundry list of technological concepts in the `Clueless` folder and said, _"Yeah! I know all of this stuff."_  

Odds are you are probably working in a Technical Support role already and making upwards around $40,000 / year.  Your current job is boring the crap out of you and you were always super interested in Penetration Testing but have no idea how to get a job without a Computer Science Degree, etc.

Great!  I'm here to finally level up your skills and get you out that boring IT Support role--no longer are you forced to deal with angry old men over the phone who can't access their email.  But, don't quit your day job just yet.  Breaking the barrier between IT Support Specialist and Penetration Tester took me nearly 5 years to accomplish.  I went through a lot of ups and downs personally.  However, I didn't have a curated list of topics that I needed to master beforehand.  So hopefully, I can get you up to speed quickly!

-------
## What you should focus on:
If you want to become an Associate Penetration Tester then you should put 80% of your effort into **Web Application Hacking**.  Right now, the majority of work that security firms are contracted to test are Web Applications.  Esspecually applications that are deployed to the cloud, such as AWS, GCP, and Azure.  You'll need to have very indepth knowledge of these technologies if you expect to claw your way into an Associate position at a security firm that hires penetration testers.

## The Framework of Understanding a Vulnerability
IMPORTANT!!! Before you can move on to learning another vulnerability, you must be able to answer these 4 questions about the vulnerability you are currently researching:
 * **Find**
   * How do you Enumerate the vulnerability?
 * **Exploit**
   * How do you Exploit the vulnerability?
 * **Fix**
   * What are the modern and recommended fixes for the vulnerability?
 * **Bypass**
   * What protections don't work, and how can you bypass weak mitigations that lazy developers implement?
 
 -------
# Table of Contents

## Popular Penetration Testing Tools
 * **Popular Penetration Testing Distros**
    * Kali Linux
    * Parrot
    * BackBox
    * BlackArch
 * **Web Applications Tools**
   * BurpSuite
   * Nikto
   * Directory Busters
     * Dirb
     * Dirbuster
   * SQLmap
   * WPscan
   * w3af
   * CeWL
   * testssl.sh
      * **Less-Used Web App Tools...*
         * Aquatone
         * EyeWitness
         * Hydra
 * **Network-Based Tools**
   * nmap
   * Netcat
   * Wireshark
   * curl
      * **DNS Tools**
      * dig
      * dnsenum
      * dnsrecon
 * **Password Cracking Tools**
   * Hashcat
   * John the Ripper
 * **WiFi Hacking Tools**
   * airmon-ng
   * airodump-ng
   * aircrack-ng
   * naive-hashcat
 * **Reverse Engineering Tools**
   * **Linux-Based:**
     * gdb
     * Radare2
     * Hopper _($)_
     * file
     * strings
     * strace
     * ltrace
     * objdump
   * **Windows-Based:**
     * OllyDBG
     * WinDGB
     * IAP Pro _($)_
     * Windows SysInternals
       * ListDLLs
       * Procmon
       * Portmon
       * ProcDump
     * API Monitor
 * **Programming Tools**
   * Visual Studio
   * Visual Studio Code
   * Pycharm
   * Git
   * Git BASH
 * **Misc Tools**
   * MetaSploit Framework
   * **Top Browser Extensions**
      * Wappalyzer
      * Link Redirect Trace
      * JWT Debugger
      * JSONView
   

## Web Application Fundamentals
  * **HTML**
    * MetaTags
    * Forms
    * Attributes
    * iFrames
  * **CSS**
    * **CSS Frameworks:**
      * Bootstrap
      * Google Material
      * Purple
    * Stylesheet Subresource Integrity
  * **XML**
    * SVG Images
    * SAML _(Basic Familiarity)_
  * **JavaScript**
    * JavaScript Syntax Fundamentals
      * Function Prototyping
      * XMLHttpRequest()
      * JSON _(Data Serialization)_
    * jQuery _(Basic Familiarity)_
    * JavaScript Frameworks _(Basic Familiarity)_
      * Angular
      * Angular2
      * React
      * Vue
    * JavaScript Subresource Integrity
  * **Same-Origin Policy _(SOP)_**
  * **CORS**
    * Preflight Requests
  * **Content Deliver Networks _(CDNs)_**
  * **MVC Design Pattern**
    * Models
    * Views
    * Controllers
  * **HTTP Headers**
    * User-Agent
    * Host
    * Cookie
    * Authorization
    * Content-Type _(MIME Types)_
    * Transfer-Encoding
    * Accept-Encoding
    * Upgrade
    * **CORS Headers**
      * Origin
      * Access-Control-Allow-Origin
      * Access-Control-Allow-Credentials
      * Access-Control-Request-Method
      * Access-Control-Request-Headers
    * **HTTP Security Headers**
      * Strict-Transport-Security
      * Content-Security-Policy
      * X-XSS-Protection
      * X-Frame-Options
      * X-Content-Type-Options
    * X-Csrf-Token
  * **HTTP Requests**
    * GET
    * POST
    * PUT
    * DELETE
    * OPTIONS
  * **Session Management**
    * **Cookies**
      * Cookie Flags / Cookie Prefixes
        * HttpOnly
        * HostOnly
        * Secure
        * Same-Site
        * Expires
    * **JSON Web Tokens _(JWT)_**
      * JWS vs. JWE
        * JWT Header
          * alg:
          * typ:
        * JWT Payload
        * JWT Signature
      * Claims
 * **Database Essentials**
   * **SQL:**
     * **SQL DBMS:** _(Basic Familiarity)_
       * MySQL
       * SQLite
       * Microsoft SQL
       * PostgreSQL
       * Oracle DB
     * **SQL Syntax Basics:**
       * USE
       * SELECT
         * WHERE
         * LIKE
       * INSERT
       * UPDATE
       * DROP
       * DELETE
   * **NoSQL:**
     * **NoSQL DBMS:** _(Basic Familiarity)_
       * Redis
       * MongoDB
       * Apache CouchDB
        * Cloud Variants
          * AWS DynomoDB
          * GCP DataStore
          * Azure CosmosDB
     * **NoSQL Syntax Basics:**
      * ...
   * **Content Management Systems** _(CMS)_
      * WordPress
      * Drupal
      * Joomla
      * Django

## Web Application Reconnaissance
  * **Top 10 To-Do List**
      * Spidering with BurpSuite
        * Take notes of any attack vectors
          * Forms, File Uploads, etc.
      * Check robots.txt
      * nikto
      * dig
      * Google Dorks
      * Checking HTTP Responses for sensitive information
      * Forced Browsing
      * Enumerate subdomains
      * Check for HTML Comments
      * View custom JavaScript
      * /.well-known/security.txt
      * Vhost Bruteforcing
        * Accessing unresolved DNS via Host Header
  * **More Checklists**
      * ...
      
      
## Web Application Vulnerabilities
  * **OWASP Top 10:**
    * **Injection**
      * **SQL Injection:**
        * Error-Based
        * UNION-Based
        * Blind
        * Second-Order SQL Injection
      * **NoSQL Injection**
        * JavaScript Injection
      * **CMD Injection**
      * **LDAP Injection**
    * **Broken Authentication**
    * **Sensitive Data Exposure**
    * **XXE**
      * XXE-OOB
    * **Broken Access Controls**
    * **Security Misconfigurations**
    * **XSS**
      * Reflected
      * Stored
      * DOM-XSS
    * **Insecure Deserialization**
      * Java
      * PHP
      * .NET
    * **Using Components with Known Vulnerabilities**
    * **Insufficient Logging & Monitoring**
  * **Modern Application Attacks:**
    * HTTP Response Splitting
    * HTTP Request Smuggling
    * Cache Posioning
    * CORS Misconfigurations
    * Server-Side Template Injection 
    * OAuth2 Attacks
      * Open Redirect Token Theft
    * JSON Web Token CVEs
    * Web Sockets
    * Prototype Pollution
  * **Other Attacks:**
    * Directory Traversal
    * Local File Inclusion
      * Log Poisoning


## Advanced Networking Essentials
  * SYN Scanning
  * SSL/TLS In-Depth Understanding
    * Let's Encrypt
    * HSTS
    * x509
    * Digital Signatures
      * Certificate Authorities
        * Root CA
        * Intermediate CA
        * Server Certificates
        * Chain of Trust
    * Diffie-Hellman Key Exchange
  * Active Directory Services
    * LDAP
    * Single-Sign-On _(SSO)_
    * Kerberos
  * iptables
    * ipTable Chains:
      * Input
      * Forward
      * Output
    * ipTable Connection Responses:
      * Accept
      * Drop
      * Reject
    

## Fundamental Network-Based Vulnerabilities
  * Man-In-The-Middle Attack
    * ARP Poisoning
    * Promiscuous Mode
  * WiFi Hacking / Security
    * Pre-Shared Keys
    * EAP
    * Promiscuous Detection
    * Cracking WEP
    * Cracking WPA/WPA2
        * 4-Way Handshakes
          * Pre-Wise Master Keys
          * Authenticator Nonce
          * Supplicant Nonce
        * DeAuth
    * WPA Enterprise
    * Bruteforcing WPS
    * Evil Twin Attack
    * Windows Active Directory Attacks
      * DCSync
      * Single-Sign-On Attacks
        * NTLM Hashes
        * Pass-The-Hash
      * Kerberos Attacks:
        * Pass-The-Ticket Attack
        * Golden Ticket Attack
        * Silver Ticket Attack

## Linux Essentials
  * Linux Distributions:
    * Debian vs. RedHat
    * Debian-Based Distros
      * Ubuntu
      * Kali Linux
      * ParrotOS
    * RedHat
      * RHEL _($)_
      * CentOS
      * Fedora
  * Linux CLI Essentials
    * System Management
    * Installing Software
      * apt _(Debian)_
        * .deb
        * dpkg
      * yum _(RedHat)_
        * .rpm
      * /usr/bin
      * /opt/
    * Networking
      * nmcli
      * nmtui
      * /etc/sysconfig/network-scripts/
    * Inspecting Logs
      * journelctl
      * /var/log
    * Environment Variables
      * env
  * Linux Data Exfilration _(Post exploitation)_
    * /tmp
    * /home
    * /var/log
    * ~/.bash_history
    * Check Environment Variables
      * env
      * printenv
    * /etc/passwd
    * /etc/shadow
    * ~/.ssh/id_rsa
    * /etc/cron.d
    * /var/www
    
## Memory / Binary Fundamentals
  * **Binary**
    * Bit vs. Nyble vs. Byte
    * 8-Bit Binary Translation
    * Base8 vs. Base10
    * Hexadecimal _(Base16)_
  * **The Kernel**
    * Physical Memory vs. Virtual Memory
    * SYSCALLs
    * System Interrupts
    * Modules

## BASH Scripting


## Local Privilage Exculation
 * Windows
 * Linux
    * LinPEAS
    * Leveraging running processes running as root
        * ps -ef
        * ps -aux
    * Searching for outdated vulnerable software
        * dpkg -l _(Debian)_
        * rpm -qa _(CentOS)_


## Python Essentials
  * Understanding the Basics
    * Reading / Writing Files
      * open()
    * Issuing OS Commands
      * os Module
        * os.chdir()
        * os.mkdir
        * os.remove()
        * os.rename()
        * os.listdir()
        * os.mkdir()
        * os.rmdir()
        * os.chmod()
        * os.path.exists()
        * os.path.isabs()
        * os.path.isdir()
        * os.path.isfile()
        * os.path.getsize()


## Popular CVEs



## Recommended Certifications
 * CompTIA PenTest+
 * CompTIA Linux+
 * CCNA
 * CEH
 * AWS Certified Solutions Architect - Associate

---------------------------------------------