# JeffTadashi's Quick Dockers

This is my collection of easy-to-use docker images for running simple network/security tools, without needing to hassle with manual installation, getting Python/Perl/Go dependencies installed, building, etc.

## Features 
Some features include:
- Minimal image/download sizes
- Consistenty in usage across all tools (same working directories, base OS, etc)

## Usage
Simply install docker on your machine, then you can run the tools like the following example:
```
docker run --rm jefftadashi/nmap example.com
```
See all the folders in this repository for the docker images that are available. Also check out my docker hub directly at:
- https://hub.docker.com/u/jefftadashi

## Image List

Name | Description
--- | ---
dirsearch | Brute-force find directories in web servers
ldapsearch | Search LDAP directories
nikto | Scan web servers for vulnerabilities
nmap | Network port scanner (with included scripts)
smbclient | SMB protocol client
sqlmap | Find/exploit SQL injection vulnerabilities in web servers
subfinder | Find all subdomains
whatweb | Web scanner to identify running services
