# Initial Access

## Drive-by Compromise

```Markdown
ATTACK ID - T1189

```

Drive-by Compromise: when a user visits a website as part of a regular browsing session. With this technique, the user's web browser is targeted and exploited simply by visiting the compromised website.

One of the techinique used by APT37 to gain initial access was be Drive-by Compromise, where they lure thier target to open a website that has JavaScript based profiler called RICECURRY that identifies Vicitim's browser and feliver malicious code.

Software/tools used:

1. A potential alternative of PluginDetect RICECURRY profiler is used in compromised web servers.

2. KARAE - A backdoor in the disguse of a video player

Capabilites:

1. RICECURRY - Using RICECURRY, advasaries fingerprint the victims web browser used, version, Adobe flash player version and Operating System used. Then it delivers the malware according to the fingerprint.

2. KARAE - Collect system information such as computer name, system, manufacturer and the environment type as in debugger and execution path.

Detection:

1. RICECURRY - FireEye - Exploit.APT.RICECURRY

2. KARAE - FE_APT_Backdoor_karae_enc, FE_APT_Backdoor_karae, Backdoor.APT,Karae
