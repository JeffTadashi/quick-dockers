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
