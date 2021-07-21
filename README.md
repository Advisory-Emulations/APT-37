APT37 is a North Korea cyber group. North Korean Cyber Espionage group known to target vicitims from South Korea, Japanm Russia, India, Nepal, etc. In this project our main focus is to Emulate the plan of this group. Initially we will analyze what techniques they use and then we will see in what scenarios the attack is executed. As per the Mitre Att&ck framework we are going to analyse each stage of the attack.

Also Known as
 1. ScarCruft
 2. Reaper
 3. Group123
 4. TEMP.Reaper

Famous Operations/Campaigns
1. Operation Daybreak
2. Operation Erebus
3. Golden Time
4. Evil New Year

This folder has emulation plans for APT37 as threat actor, and a simulation playbook along with detection tactics and analysis of malwares and exploitations used APT37.

Initial access : APT37 uses Drive by Compromise and Phishing emails for gaining initial access. They compromise websites to send malware or phishing emails to victims. They change the phishing email contents based on the on-going issues to make it look legit. Use of torrent files also used to share the malware.

Execution phase : They use vulnerabilities in Flash player, word for executing the malware. Malwares mentioned below and the cve's as well. VB scripts are sent(related to .Net framework). IPC(Inter process communication) techniques are used such as Dynamic Data Exchange to maintain a link between the process.They use flaws in client applications like web browsers, Flash player and Microsoft office file. or Used Native API to execute code along with the local OS processes. APT37 has used Flash Player (CVE-2016-4117, CVE-2018-4878) and Word (CVE-2017-0199) exploits for execution. 
Links : 
cve-2016-4117 : https://www.fireeye.com/blog/threat-research/2016/05/cve-2016-4117-flash-zero-day.html
// Extra ***Other techniques that can be used COm(Common object model) to execute code in local or Used Native API to execute code along with the local OS processes. // Extra ** .Net code inside the downloaded file is suspicious They use flaws in client applications like web browsers, Flash players and Microsoft office files. // Extra **Check for processes running when you boot your system

Persistence : Using registry keys and startup folder, execution of the malware takes place when the system boots.They has added persistence via the Registry key HKCU\Software\Microsoft\CurrentVersion\Run\ // Extra ** registry key check and analyse the processes running when system boot is suggested. 

4. Privilege Escalation: They inject malware varient ROKRAT into cmd.exe or explorer.exe. They use Windows User Account Control (UAC) allows a program to elevate its privileges.
Link 
ROKRAT: https://research.nccgroup.com/2018/11/08/rokrat-analysis/
UAC : https://github.com/hfiref0x/UACME
5. Defense Evasion : They used has signed its malware with an invalid digital certificates listed as "Tencent Technology (Shenzhen) Company Limited to evade the dettection from tools and from analysts. they use  uses steganography to send images to users that are embedded with shellcode.
6. Credential access : They use has used a credential stealer known as ZUMKONG that can harvest usernames and passwords stored in browsers.
7. Discovery : They has a has a Bluetooth device harvester, which uses Windows Bluetooth APIs to find information on connected Bluetooth devices for peripheral process discovery. They use Freenki malware lists running processes using the Microsoft Windows API(process discovery). they collect the computer name, the BIOS model, and execution path and also identifies the victim username
Bluetooth Harvester : https://securelist.com/scarcruft-continues-to-evolve-introduces-bluetooth-harvester/90729/
8. Lateral Movement : N/A
10. Collection : 
11. Command and control
12. Exfilteration
13. Impact


Relate to Mitre matrix
Cyber kill chain process :
1. Reconnaissance: Intruder selects target, researches it, and attempts to identify vulnerabilities in the target network.
Weaponization: Intruder creates remote access malware weapon, such as a virus or worm, tailored to one or more vulnerabilities.
Delivery: Intruder transmits weapon to target (e.g., via e-mail attachments, websites or USB drives)
Exploitation: Malware weapon's program code triggers, which takes action on target network to exploit vulnerability.
Installation: Malware weapon installs access point (e.g., "backdoor") usable by intruder.
Command and Control: Malware enables intruder to have "hands on the keyboard" persistent access to target network.
Actions on Objective: Intruder takes action to achieve their goals, such as data exfiltration, data destruction, or encryption for ransom.

Malware Analysis :
1. How they exploit the client applications and stay persistent
2. analyze the code ( try to undertand)
3. Payload modiication( a try)
4. IOC's 

Attack Scenario :



Malware Used
CORALDECK - Exfiltration tool
DOGCALL - Backdoor tool
GELCAPSULE - Downloader for additional malware
HAPPYWORK - Downloader for additional malware, exfiltration tool
KARAE - Backdoor tool
MILKDROP - Set registry to gain persistence, launches backdoor
POORAIM - Backdoor and exfiltration tool
RICECURRY - Browser profiler used to decide what malware to deliver
RUHAPPY - Disk wiper
SHUTTERSPEED - Backdoor and exfiltration tool
SLOWDRIFT - Downloader for additional malware
SOUNDWAVE - Audio capture utility
WINERACK - Backdoor
ZUMKONG - Credential stealer

Vulnerabilities Exploited
 CVE-2013-4979 - Buffer overflow in EPS Viewer
 CVE-2014-8439 - Adobe Flash execution of arbitrary code
 CVE-2015-2387 - Windows Adobe Type Manager Font Driver elevation of privileges
 CVE-2015-2419 - JScript 9 in Internet Explore 10 and 11 execution of arbitrary code
 CVE-2015-2545 - Microsoft Office execution of arbitrary code
 CVE-2015-3105 - Adobe Flash execution of arbitrary code
 CVE-2015-5119 - Adobe Flash execution of arbitrary code
 CVE-2015-5122 - Adobe Flash execution of arbitrary code
 CVE-2015-7645 - Adobe Flash execution of arbitrary code
 CVE-2016-1019 - Adobe Flash execution of arbitrary code
 CVE-2016-4117 - Adobe Flash execution of arbitrary code
 CVE-2017-0199 - Microsoft Office / WordPad execution of arbitrary code
 CVE-2018-0802 - Equation Editor in Microsoft Office execution of arbitrary code
 CVE-2018-4878 - Adobe Flash execution of arbitrary code
 
 
 Good Questions :
 What is PEB ?
 How Windows User Account Control (UAC) allows a program to elevate its privileges ?
 WHat is ZUMKONG how it works ?
