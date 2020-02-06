# JeffTadashi's Quick Dockers

This is my collection of easy-to-use docker images for running simple network/security tools, without needing to hassle with manual installation, getting Python/Perl/Go dependencies installed, building, etc.

## Features 
- Easy-to-use, with full guide here (even if you've never used Linux!)
- Minimal image/download sizes
- Consistent image OS: All Alpine Linux (latest stable)
- Consistent directory structure: `/root` as clean working directory for all, `/opt/tool-name` as tool's main install folder

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
docker run --rm jefftadashi/nmap -p1-500 example.com
```
For mounting volumes to pass files to/from the your current directory, try the following:
```
[Linux/MacOS]
docker run --rm -v {pwd):/root jefftadashi/nmap -p1-500 example.com

[Windows CMD]
docker run --rm -v %cd%:/root jefftadashi/nmap -p1-500 example.com

[Windows Powershell]
docker run --rm -v {PWD):/root jefftadashi/nmap -p1-500 example.com
```

## Image List

See all the folders in this repository for the docker images that are available, and see list below:

Name | Description
--- | ---
dirsearch | Brute-force find directories in web servers
evil-winrm | Shell through WinRM services 
ldapsearch | Search LDAP directories
nikto | Scan web servers for vulnerabilities
nmap | Network port scanner (with included scripts)
smbclient | SMB protocol client
sqlmap | Find/exploit SQL injection vulnerabilities in web servers
subfinder | Find all subdomains
whatweb | Web scanner to identify running services

## Links

GitHub: https://github.com/JeffTadashi/quick-dockers  
Docker Hub: https://hub.docker.com/u/jefftadashi

## Feedback

I would appreciate any and all feedback! And I am happy to add other useful tools to this repository, just let me know.