# APT-37
APT 37 Emulation plan






APT37 is a North Korea cyber group. In this project our main focus is to Emulate the plan of this group. Initially we will analyze what techniques they use and then we will see in what scenarios the attack is executed. As per the Mitre Att&ck framework we are going to analyse each stage of the attack

Initial access : APT37 uses Drive by Compromise and Phishing emails for gaining initial access. They compromise websites to send malware or phishing emails to victims. They change the phishing email contents based on the on-going issues to make it look legit. Use of torrent files also used to share the malware.

Execution phase : They use vulnerabilities in Flash player, word for executing the malware. Malwares mentioned below and the cve's as well. VB scripts are sent(related to .Net framework). IPC(Inter process communication) techniques are used such as Dynamic Data Exchange to maintain a link between the process.They use flaws in client applications like web browsers, Flash player and Microsoft office file. or Used Native API to execute code along with the local OS processes. 
// Extra ***Other techniques that can be used COm(Common object model) to execute code in local or Used Native API to execute code along with the local OS processes. 
// Extra ** .Net code inside the downloaded file is suspicious They use flaws in client applications like web browsers, Flash players and Microsoft office files. 
// Extra **Check for processes running when you boot your system

Persistence : Using registry keys and startup folder, execution of the malware takes place when the system boots. // Extra ** registry key check and analyse the processes running when system boot is suggested
