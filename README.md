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

Execution phase : They use vulnerabilities in Flash player, word for executing the malware. Malwares mentioned below and the cve's as well. VB scripts are sent(related to .Net framework). IPC(Inter process communication) techniques are used such as Dynamic Data Exchange to maintain a link between the process.They use flaws in client applications like web browsers, Flash player and Microsoft office file. or Used Native API to execute code along with the local OS processes. // Extra ***Other techniques that can be used COm(Common object model) to execute code in local or Used Native API to execute code along with the local OS processes. // Extra ** .Net code inside the downloaded file is suspicious They use flaws in client applications like web browsers, Flash players and Microsoft office files. // Extra **Check for processes running when you boot your system

Persistence : Using registry keys and startup folder, execution of the malware takes place when the system boots. // Extra ** registry key check and analyse the processes running when system boot is suggested

4. Privilege Escalation
5. Defense Evasion
6. Credential access
7. Discovery
8. Lateral Movement
9. Collection
10. Command and control
11. Exfilteration
12. Impact


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
