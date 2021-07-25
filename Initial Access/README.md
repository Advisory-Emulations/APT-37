# Initial Access

## Drive-by Compromise

```Markdown
ATTACK ID - T1189

```

Drive-by Compromise: when a user visits a website as part of a regular browsing session. With this technique, the user's web browser is targeted and exploited simply by visiting the compromised website.

One of the techinique used by APT37 to gain initial access was be Drive-by Compromise, where they lure thier target to open a website that has JavaScript based profiler called RICECURRY that identifies Vicitim's browser and feliver malicious code.

Software/tools used: A potential alternative of PluginDetect RICECURRY profiler is used in compromised web servers.

Capabilites: Using RICECURRY, advasaries fingerprint the victims web browser used, version, Adobe flash player version and Operating System used. Then it delivers the malware according to the fingerprint.

Detection: FireEye - Exploit.APT.RICECURRY
