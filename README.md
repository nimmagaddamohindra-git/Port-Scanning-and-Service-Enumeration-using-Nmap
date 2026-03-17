# Port-Scanning-and-Service-Enumeration-using-Nmap
This project demonstrates the use of Nmap to perform port scanning and service enumeration on a local system. It focuses on identifying open ports, analyzing running services, and understanding system exposure from a cybersecurity perspective.

## Objective
The objective of this project is to:
- Identify open ports on a system
- Detect running services on those ports
- Understand potential security risks
- Learn how attackers discover exposed services
  
## Tools Used
- Nmap (Network Scanner)
- Windows Command Prompt
- Netstat (Port Verification)
- Tasklist (Process Mapping)

## Methodology

### 1. Initial Port Scan
Executed the following command to scan top ports:

nmap 127.0.0.1


### 2. Full Port Scan
Performed full scan to identify all open ports:

nmap -p- 127.0.0.1

### 3. Service Detection
Identified service versions:

nmap -sV 127.0.0.1

### 4. Port Verification
Verified active ports using:

netstat -ano | findstr LISTENING

### 5. Process Identification
Mapped ports to processes:

tasklist | findstr 

## Results

The following open ports were identified:

| Port | Service | Description |
|------|--------|------------|
| 135  | MSRPC  | Windows Remote Procedure Call |
| 445  | SMB    | File sharing service |
| 3306 | MySQL  | Database service |

Additional Findings:
- Majority of scanned ports were closed
- System services and database were actively running
- MySQL port was listening on all interfaces (0.0.0.0)

##  Analysis

- Port 135 is used for internal Windows communication
- Port 445 (SMB) can be a security risk if exposed externally
- Port 3306 indicates a running MySQL database and may be vulnerable if not secured
- Open ports represent potential attack surfaces
- Closed ports reduce exposure

## Screenshots
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3fe7882f-65f7-41e8-8a8f-6604b054398d" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/be87bb5f-a137-46e8-b83b-65742e6bdadd" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e0388c17-294b-46c6-8a2f-cdb5f62571ea" />




## Key Learnings

- Understanding of port scanning techniques
- Identification of open ports and services
- Mapping ports to running processes
- Awareness of potential security risks
- Basics of system exposure analysis

## Conclusion

This project provided hands-on experience in identifying open ports and analyzing system services using Nmap. It highlights how exposed services can be detected and assessed for potential security risks.
