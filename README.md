# About VforC2 (repo is OUTDATED & Will not be updated)
VforC2 or v4c2 is a C2 & hacking toolkit application coded in python. It contains modules that utilize penetration testing tools that typically come pre-installed in security oriented operating systems. It is meant to be used via the command line in Kali Linux or similar OS. Enter the associated commands to call modules, enabling you to listen for incoming connections, send shell commands to one or many connected clients, run vulnerability scans, preform brute force attacks, or simply interact with the regular terminal while holding onto connections in the background. I coded it with my preferences in mind and to interact with my custom administration tool/backdoor but any reverse shell connection type will do.

Currently contains modules that call the following (usually preinstalled) tools: Nmap, dirb, ffuf, sqlmap, owasp-zap and hydra. 
Base kali may not have ffuf but it is easily downloaded with "sudo apt-get install ffuf"

Additionally it utilizes Sublist3r/subrute from https://github.com/aboul3la/Sublist3r

## Installation
```
git clone https://github.com/V1236/VforC2.git
```

## Dependencies:
Many python dependencies are utilized and can be installed using the requirements file:
```
sudo python3 -m pip install -r requirements.txt
```

## Usage
```
After installation and dependencies, navigate to the directory and isue "python3 VforC2.py" from the command line.
Begin with the "help" command and go from there. Currently it supports the following:
Command | Description
------- | -----------
help | Display this list. More commands to come in future updates.
bash | Enters a bash terminal. The script is still running. Use exit to return.
arp | Does an ARP scan to discover hosts on the local network. Needs root.
ping | Calls nmap to discover hosts using a ping scan.
scan | Calls nmap preform a scan of your choosing.
chmac | Changes your MAC address. Needs Root.
spider | Crawls the HTML of a target website for interesting endpoints such as .js.
dbust | Performs directory busting utilizing dirb to look for hidden directories on a target website.
sbust | Performs quick subdomain busting utilizing Sublist3r to look for subdomains on a target website.
sbrute | Performs subdomain busting utilizing subbrute with a wordlist to look for subdomains on a target website.
vulnweb | Calls owasp-zap for web app vulnerability scanning.
vulnport | Calls nmap vulners for port based vulnerability scanning.
login | Utilizes hydra to preform a brute force attack on a login point.
fuzz | Utilizes ffuf to quickly enumerate endpoints on a target website.
sqli | Utilizes sqlmap to attempt sql injection on a target endpoint.
listen *port* | Begin listening for incoming connections. Received connections are displayed.
sessions | Lists all incoming connections aka available sessions.
session 1-50 | Enters an interactive state with one session. Default code accepts up to 50 sessions.
sendall *shell command* | Sends a shell command to be executed on all active sessions.
background | Exits the interactive state with a session and returns to the main prompt.
exit | Ends the program. If sessions are active also use Cntrl + C.
clear | Clears the screen.

```

### Examples
* To start:
``python3 VforC2.py``
or
``sudo python3 VforC2.py``
(some modules require root)

* To return to the terminal without exiting the script:
``bash``

* To listen for incoming connections on port 4444:
``listen 4444``

* To execute the command "curl -O example.com/test.txt" on all active sessions:
``sendall curl -O example.com/test.txt``

## Version
**Current version is 4.0**

## Thanks
