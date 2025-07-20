# ReactJS Installation Guide on Linux 

A comprehensive, step-by-step guide for installing ReactJS on Debian/Ubuntu-based Linux systems.

---

| Authors           | Created on    | Version | Last updated by | Last edited on |
|-------------------|--------------|---------|-----------------|---------------|
| Kawalpreet Kour   | 19 July 2025 | v1      | -               | -             |

---

## Table of Contents

- [Objective](#objective)
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Step-by-Step Installation Guide](#step-by-step-installation-guide)
  - [Step 1: Update Your Packages](#step-1-update-your-packages)
  - [Step 2: Install Required Dependencies](#step-2-install-required-dependencies)
  - [Step 3: Add Node.js Repository](#step-3-add-nodejs-repository)
  - [Step 4: Run the Setup Script](#step-4-run-the-setup-script)
  - [Step 5: Install Node.js & npm](#step-5-install-nodejs--npm)
  - [Step 6: Verify Installations](#step-6-verify-installations)
  - [Step 7: Upgrade npm](#step-7-upgrade-npm)
  - [Step 8: React Setup Using Vite](#step-8-react-setup-using-vite)
    - [Create a New Vite Project](#create-a-new-vite-project)
    - [Navigate to Project Directory](#navigate-to-project-directory)
    - [Install Project Dependencies](#install-project-dependencies)
    - [Run Development Server](#run-development-server)
- [Troubleshooting](#troubleshooting)
- [Notes](#notes)
- [Contact](#contact)
- [References](#references)

---

## Objective

Set up ReactJS on a local Ubuntu machine using **Vite**, a modern and faster alternative to `create-react-app`.

---

## Introduction

ReactJS is a JavaScript library for building interactive user interfaces. It is maintained by Meta and a community of developers. This guide will walk you through the ReactJS setup on Ubuntu 22.04 using Vite.

---

## Prerequisites

| Requirement         | Description                                  |
|---------------------|----------------------------------------------|
| Operating System    | Ubuntu 22.04 LTS or compatible               |
| Access Privileges   | Root or sudo-enabled user                    |
| Internet Connection | Required                                     |
| Memory Requirement  | Minimum 2 GB RAM (Recommended for React)     |

---

## Step-by-Step Installation Guide

### Step 1: Update Your Packages

```bash
sudo apt update && sudo apt upgrade -y
```
_Updates the package list and upgrades outdated software._

<img width="813" height="584" alt="Screenshot from 2025-07-20 16-33-58" src="https://github.com/user-attachments/assets/fe3f8d8b-ea13-4393-94ce-280963ce78e6" />

---

### Step 2: Install Required Dependencies

```bash
sudo apt install curl apt-transport-https gnupg2 software-properties-common -y
```
_These tools help in securely fetching and managing external repositories._

<img width="1057" height="481" alt="Screenshot from 2025-07-20 16-35-08" src="https://github.com/user-attachments/assets/507ca4e0-d983-4281-aace-3d0d2d05e9fb" />

---

### Step 3: Add Node.js Repository

```bash
curl -fsSL https://deb.nodesource.com/setup_23.x -o nodesource_setup.sh
```
_Downloads NodeSource setup script for Node.js 23.x_

<img width="812" height="80" alt="Screenshot from 2025-07-20 22-50-38" src="https://github.com/user-attachments/assets/9b464ace-7756-4210-b7bc-38efc9300fe4" />

---

### Step 4: Run the Setup Script

```bash
sudo bash nodesource_setup.sh
```
<img width="746" height="653" alt="Screenshot from 2025-07-20 22-53-26" src="https://github.com/user-attachments/assets/20a74d47-1f47-4365-b455-275e03186c70" />

---

### Step 5: Install Node.js & npm

```bash
sudo apt-get install -y nodejs
```
<img width="858" height="391" alt="Screenshot from 2025-07-20 23-00-03" src="https://github.com/user-attachments/assets/92387b38-898d-455a-a9d7-37057a8ce1c1" />

---

### Step 6: Verify Installations

```bash
node -v 
```
<img width="495" height="67" alt="Screenshot from 2025-07-20 23-00-53" src="https://github.com/user-attachments/assets/d3c812d8-0c93-4832-a5a1-9baf4ae86936" />

```bash

npm -v
```
<img width="495" height="67" alt="Screenshot from 2025-07-20 23-06-06" src="https://github.com/user-attachments/assets/1a087526-a18a-4f41-86b3-65234b98f00a" />

_Should output the installed versions._

---

### Step 7: Upgrade npm (Recommended)

```bash
sudo npm install -g npm@latest
```

<img width="681" height="94" alt="Screenshot from 2025-07-21 00-36-12" src="https://github.com/user-attachments/assets/7d4c59cd-f18a-457e-b45d-bbfe89dc59a0" />

---

## Step 8: React Setup Using Vite

> Tip: Make sure you're in the directory where you want to create your project.

---

### Create a New Vite Project

```bash
npm create vite@latest
```
<img width="661" height="589" alt="Screenshot from 2025-07-20 23-19-11" src="https://github.com/user-attachments/assets/6bbe65ff-92e6-43e7-8702-e14ac23becd4" />

You'll be prompted:

- **Project name** → `Demo-reactjs` (or your choice)
- **Framework** → `React`
- **Variant** → `JavaScript`

Alternatively, you can run:
```bash
npm create vite@latest my-app -- --template react
```
Where `my-app` is your desired project name.

| Command                          | Description                                  |
|-----------------------------------|----------------------------------------------|
| `npm create vite@latest`          | Runs the latest Vite setup tool              |
|  `<project name>` `eg. my-app`                         | Name of your project directory               |
| `-- --template react`             | Tells Vite to use the React JavaScript template |

---

### Navigate to Project Directory

```bash
cd <project name>
```
<img width="672" height="30" alt="Screenshot from 2025-07-21 00-41-35" src="https://github.com/user-attachments/assets/a7e3a3f5-3e7b-4a7f-ad66-fa89c941e7db" />

Replace `<project name>` with the name you chose (e.g., `Demo-reactjs`).

---

### Install Project Dependencies

```bash
npm install
```
<img width="626" height="146" alt="Screenshot from 2025-07-21 00-41-46" src="https://github.com/user-attachments/assets/4d0f1147-674e-4d35-aff0-b5de62452841" />

---

### Run Development Server (Expose to Network)

```bash
npm run dev 
```
<img width="624" height="207" alt="Screenshot from 2025-07-21 00-41-58" src="https://github.com/user-attachments/assets/4019e1b7-c872-4cd7-b5d4-1206f240e788" />

You should see output like:
```
➜  Local:   http://localhost:5173/
➜  Network: http://<your-ip>:5173/ > (in case you're installing on EC2)
```
Open the Network URL in your browser.

<img width="1296" height="600" alt="Screenshot from 2025-07-20 23-21-39" src="https://github.com/user-attachments/assets/e028781f-d3f1-453c-96ba-e30c45878b01" />

---

## Troubleshooting

| Issue                                      | Cause                                 | Solution                                   |
|---------------------------------------------|---------------------------------------|--------------------------------------------|
| `create-react-app` deprecated               | Not actively maintained               | Use Vite instead                           |
| Permission denied writing to /usr/lib       | Global install without `sudo`         | Use `sudo npm install`                     |
| Port not opening on browser                 | Server not exposed                    | Use `--host` flag in `npm run dev`         |
| App not loading on public IP                | EC2 Firewall blocking port            | Add custom TCP rule for port `5173`        |

---

## Notes

- Port `5173` is used by **Vite** (default).
- Always prefer **Vite** for new React projects (faster, more modern).
- If using cloud VMs (e.g., AWS EC2), open port `5173` in the security group/firewall.

---

## Contact

| Name             | Email                                       |
|------------------|---------------------------------------------|
| Kawalpreet Kour  | Kawalpreet.kour.snaatak@mygurukulam.co      |

---

## References

- [Reference Video – React.js Vite Setup](https://youtu.be/h2PXfwaI8DA?si=E5u1TBsJF-_aZdQD)
- [Official React Documentation by GeeksForGeeks](https://www.geeksforgeeks.org/reactjs/react/)

---
