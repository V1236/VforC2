# About V4C2
VforC2 or v4c2 is a simple Command & Control application coded in python. It contains modules that utilize popular penetration testing tools that typically come pre-installed in security oriented operated systems. It is meant to be used via the command line in Kali Linux or similar OS. You can start this tool in the terminal, issue commands enabling you to listen for incoming connections, send shell commands to one or many clients at a time, run vulnerability scans, preform brute force attacks, or simply interact with the regular terminal while holding onto those connections in the background. I coded it to interact with my custom administration tool/backdoor but it should work just fine when receiving any reverse shell connection type.

Currently contains modules that call the following (usually preinstalled) tools: Nmap, dirb, owasp-zap and hydra.
Additionally it utilizes Sublist3r/subrute from https://github.com/aboul3la/Sublist3r
```

## Installation
## Dependencies:

These dependencies can be installed using the requirements file:
```
sudo pip install -r requirements.txt
```
## Usage
### Examples
## Version
**Current version is 1.0**
