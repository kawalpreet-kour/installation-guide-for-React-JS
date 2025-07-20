# ReactJS Installation Guide on Linux (Debian/Ubuntu)

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

---

### Step 2: Install Required Dependencies

```bash
sudo apt install curl apt-transport-https gnupg2 software-properties-common -y
```
_These tools help in securely fetching and managing external repositories._

---

### Step 3: Add Node.js Repository

```bash
curl -fsSL https://deb.nodesource.com/setup_23.x -o nodesource_setup.sh
```
_Downloads NodeSource setup script for Node.js 23.x_

---

### Step 4: Run the Setup Script

```bash
sudo bash nodesource_setup.sh
```

---

### Step 5: Install Node.js & npm

```bash
sudo apt-get install -y nodejs
```

---

### Step 6: Verify Installations

```bash
node -v && npm -v
```
_Should output the installed versions._

---

### Step 7: Upgrade npm (Recommended)

```bash
sudo npm install -g npm@latest
```

---

## Step 8: React Setup Using Vite

> Tip: Make sure you're in the directory where you want to create your project.

---

### Create a New Vite Project

```bash
npm create vite@latest
```

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
| `my-app`                         | Name of your project directory               |
| `-- --template react`             | Tells Vite to use the React JavaScript template |

---

### Navigate to Project Directory

```bash
cd <project name>
```
Replace `<project name>` with the name you chose (e.g., `Demo-reactjs`).

---

### Install Project Dependencies

```bash
npm install
```

---

### Run Development Server (Expose to Network)

```bash
npm run dev -- --host
```

You should see output like:
```
➜  Local:   http://localhost:5173/
➜  Network: http://<your-ip>:5173/
```
Open the Network URL in your browser.

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
