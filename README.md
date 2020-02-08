# JeffTadashi's Quick Dockers

This is my collection of easy-to-use docker images for running simple network/security tools, without needing to hassle with manual installation, getting Python/Perl/Go dependencies installed, building, etc.

## Features 
- Easy-to-use, with full guide here (even if you've never used Linux!)
- Minimal image/download sizes
- Multiple architecture support (x86-64, x86, ARM, ARM64, IBM Z, and PowerPC)
    - (That means it will run on Raspberry Pi!)
- Consistent image OS: All Alpine Linux (latest stable)
- Consistent directory structure: `/vol` as volume/working directory, `/opt/tool-name` as tool's main install folder

## Install Docker (for Newbies)
Install docker on your machine, and start its services. For Windows/OSX, use Docker Desktop:
- https://www.docker.com/products/docker-desktop  

For Linux hosts, you can install and auto-start services like the following Ubuntu example:
```
sudo apt install docker.io
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker your-local-username-here
```

## Usage
From your command line or terminal, you can run the following (just substitute "nmap" with whatever image is available in the list, and specify whatever parameters afterwards)
```
docker run -it --rm jefftadashi/nmap -p1-500 example.com
```
For mounting volumes to pass files to/from your current directory, try the following:
```
[Linux/MacOS/Powershell]
docker run -it --rm -v $(pwd):/vol jefftadashi/nmap -p1-500 example.com
docker run -it --rm -v ${PWD}:/vol jefftadashi/nmap -p1-500 example.com

[Windows CMD]
docker run -it --rm -v %cd%:/vol jefftadashi/nmap -p1-500 example.com
```

## Image List

See all the folders in this repository for the docker images that are available, and see list below:

Name | Description
--- | ---
altdns | Find subdomains based on patterns
dirsearch | Brute-force find directories in web servers
evil-winrm | Shell through WinRM services 
hash-identifier | Identity passcode hash types
ldapsearch | Search LDAP directories
nikto | Scan web servers for vulnerabilities
nmap | Network port scanner (with included scripts)
smbclient | SMB protocol client
sqlmap | Find/exploit SQL injection vulnerabilities in web servers
subfinder | Find subdomains based on external sources
whatweb | Web scanner to identify running services

## Links

GitHub: https://github.com/JeffTadashi/quick-dockers  
Docker Hub: https://hub.docker.com/u/jefftadashi

## Feedback

I would appreciate any and all feedback! And I am happy to add other useful tools to this repository, just let me know.