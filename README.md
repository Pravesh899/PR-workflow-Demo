# Frontend POC
This document provides Proof-of-Concept (POC) of frontend in detail.

| **Author** | **Created on** | **Version** | **Last updated by** | **Last edited on** | **L0 reviewer** | **L1 reviewer** | **L2 reviewer** |
|------------|----------------|-------------|----------------------|---------------------|---------------|-----------------|-----------------|
| Kaustubh Battul       | 12-11-24      | 1   | Kaustubh Battul    | 13-11-24     |  Aakash Tripathi ,Khushi Malhotra      |   Deepak Nishad               |                 |

---

## Table of Contents

- [Introduction](https://github.com/MyGurukulam-p11/Documentation-P11/blob/Kaustubh_Scrum-9/OT-MS-understanding/Frontend/Setup_and_run_the_APP_for_POC/README.md#introduction)
- [System Requirement](https://github.com/MyGurukulam-p11/Documentation-P11/blob/Kaustubh_Scrum-9/OT-MS-understanding/Frontend/Setup_and_run_the_APP_for_POC/README.md#system-requirements)
- [Pre-Requisites](https://github.com/MyGurukulam-p11/Documentation-P11/blob/Kaustubh_Scrum-9/OT-MS-understanding/Frontend/Setup_and_run_the_APP_for_POC/README.md#pre-requisites)
- [Walkthrough_of_Frontend](https://github.com/MyGurukulam-p11/Documentation-P11/blob/Kaustubh_Scrum-9/OT-MS-understanding/Frontend/Setup_and_run_the_APP_for_POC/README.md#walkthrough-of-frontend)
- [Contact](https://github.com/MyGurukulam-p11/Documentation-P11/blob/Kaustubh_Scrum-9/OT-MS-understanding/Frontend/Setup_and_run_the_APP_for_POC/README.md#contact)

---

## Introduction

The frontend application is based on REACTJS which main ui of [OT-Microservices](https://github.com/OT-MICROSERVICES) stack. This application is cross-platform, meaning it can run on different operating systems as long as a JavaScript runtime environment is available. A ReactJS-based web framework that powers the application's entire web page functionalities.

---

## System Requirements

| System requirement | Minimum Requirement  |
|:-----------------------:|:--------------------:|
| Disk space            | 8 GB    |
| RAM                 | 2 GB|
| Instance Type        | t2.small|

---

## Pre-Requisites
### Build-time Dependencies
| Name          |  Description                      | Version      |
|---------------|-----------------------------------|--------------|
| Node.js       |  JavaScript runtime               |    16.x      |
| npm           |  Node package manager             | v7 or higher |

---

## Important Ports
| Inbound Traffic | Description                           |
|-----------------|---------------------------------------|
| 3000            | Used by the frontend development server |

---

## Walkthrough of Frontend
To get started with the attendance API POC, follow these steps:

1. **Clone the Repository:**
```sh
    git clone https://github.com/OT-MICROSERVICES/frontend.git
    cd frontend
```
The first command clones the frontend repository on your machine. while the second command is to change the directory to frontend.

![Screenshot from 2024-11-11 14-06-33](https://github.com/user-attachments/assets/46374ed6-19ec-4466-adfa-ac21497c15e7)


2. **Edit the package.json file:**
Here, in `package.json` file, change the ip-address with your public ip-address in the proxy with valid port.

![Screenshot from 2024-11-11 14-11-07](https://github.com/user-attachments/assets/405c93ce-70e9-408c-be37-02762b769db9)

3.**Add the NodeSource repository:**
To install Node.js 16, add the NodeSource PPA (personal package archive) for Node.js 16
```sh
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
```
This command adds the Node.js repository (NodeSource) to the system's package sources and configures it for Node.js version 16.x.

![image](https://github.com/user-attachments/assets/7207dfc2-7a8a-401b-b230-2d3af469ca27)


4. **Install nodejs:**
```sh 
    sudo apt update
    sudo apt install nodejs -y
```
The first command updates the package index of the local APT package repository, ensuring that the latest versions of packages are available for installation.
Installs Node.js on the system. The '-y' flag automatically confirms any prompts during the installation process, allowing it to proceed without user intervention.

![Screenshot from 2024-11-11 14-24-57](https://github.com/user-attachments/assets/d434936a-9f83-47b7-b8d1-fdc99e71012b)


5. **Building the application:**
For building the application. we can use make command from the Makefile. The command is as follows. But before that we to install make command if not there.
```sh
    sudo apt install make
    make build
```
The first command is used to install make, which is used to build automation tool. The second command is the make build which indirectly runs npm install command through it.

![Screenshot from 2024-11-11 14-43-29](https://github.com/user-attachments/assets/90637463-04b1-46fb-b0a3-048b675ccfb7)


6. **For Running the application:**
The command for running the application the command is as follows.
```sh
    npm start
```
Executes the "start" script defined in the package.json file. This typically starts the development server or runs the application in a development environment.

![Screenshot from 2024-11-11 15-45-38](https://github.com/user-attachments/assets/7231bd8b-0b8b-431a-b9bc-69843879deb9)

7. Now,go to the browser and hit your public ip address with port 3000 to see the frontend user interface.
```sh
    http://<Public-ip-address>:3000
```

8. **Output:**
Finally the output from running the above Command is given below 

![Screenshot from 2024-11-11 15-40-20](https://github.com/user-attachments/assets/a4e6d3af-73e9-4867-a3fb-5f04ceb47737)

---

##  Reference Links

| Links | Description      |
|-----  |--------------------------|
| https://nodejs.org/en/download/package-manager/all | For nodejs installation |
| https://github.com/MyGurukulam-p11/Documentation-P11/tree/Kaustubh_Scrum-10/OT-MS-understanding/Frontend/Detailed_documentation#frontend-application-documentation | Frontend Documentation |

---

## Contact

| Name          | Email Address       |
|---------------|---------------------|
| Kaustubh Battul |  kaustubh.battul.snaatak@mygurukulam.co|

---
