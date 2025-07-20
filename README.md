# ReactJS Installation Guide on Linux systems

A comprehensive, step-by-step guide for installing ReactJS on Debian/Ubuntu-based Linux systems.

---

| Authors           | Created on    | Version | Last updated by | Last edited on |
|-------------------|--------------|---------|-----------------|---------------|
| Kawalpreet Kour   | 19 July 2025 | v1      | -               | -             |

---

## Table of Contents

1. [Introduction](#introduction)
2. [Scope](#scope)
3. [Prerequisites](#prerequisites)
4. [Procedure](#procedure)
    - [Step 1: Update the System](#step-1-update-the-system)
    - [Step 2: Install Node.js (Required by React)](#step-2-install-nodejs-required-by-react)
    - [Step 3: Verify Node.js and npm Installation](#step-3-verify-nodejs-and-npm-installation)
    - [Step 4: (Optional) Update npm](#step-4-optional-update-npm)
    - [Step 5: Install React CLI Globally](#step-5-install-react-cli-globally)
    - [Step 6: Create a React Application](#step-6-create-a-react-application)
    - [Step 7: Run the React Application](#step-7-run-the-react-application)
5. [Notes](#notes)
6. [Conclusion](#conclusion)
7. [Contact](#contact)
8. [References](#references)

---

## Introduction

ReactJS is a JavaScript library for building interactive user interfaces. It is maintained by Meta and a community of developers. This guide will walk you through the ReactJS setup on Ubuntu 22.04.

---

## Scope

- OS: Ubuntu 22.04 LTS
- Tool: ReactJS using `create-react-app`
- Target Audience: Developers, Students, Engineers setting up local React dev environment

---

## Prerequisites

| Requirement         | Description                                  |
|---------------------|----------------------------------------------|
| Operating System    | Ubuntu 22.04 LTS                             |
| Access Privileges   | Root or sudo-enabled user                    |
| Internet Connection | Required                                     |
| Memory Requirement  | Minimum 2 GB RAM (Recommended for React)     |



---

##  Procedure

### Step 1: Update the System

```bash
sudo apt-get update -y && sudo apt-get upgrade -y
```

 *Explanation*: Updates all system packages for compatibility and security.

📸 _[Insert screenshot after update finishes]_

---

### Step 2: Install Required Dependencies
```bash
sudo apt install curl apt-transport-https gnupg2 software-properties-common -y
```
These tools help in securely fetching and managing external repositories.

#### ➤ 3: Add Node.js Repository

```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo bash -
```
📸 _[Insert screenshot]_

#### ➤ 4: Install Node.js & npm

```bash
sudo apt-get install -y nodejs
```
📸 _[Insert screenshot]_

#### ➤ 5: Upgrade npm (Optional but Recommended)

```bash
sudo npm install -g npm@latest
```
📸 _[Insert screenshot after installation]_

---

#### ➤ Check Node.js version

```bash
node -v
```

 *Explanation*: Confirms that Node.js is installed correctly.

📸 _[Insert screenshot showing version output]_

#### ➤ Check npm version

```bash
npm -v
```

*Explanation*: Verifies the installation of npm.

📸 _[Insert screenshot showing version output]_

---
### Step 6: Create a React Application
Once Node.js and npm are installed, you're ready to create your first React project. The recommended tool for this is Vite, which provides a fast and optimized setup. create-react-app is now officially deprecated (as of 2024).

Using Vite (Recommended)
Vite is a modern build tool that offers lightning-fast startup, minimal configuration, and a better development experience.

```bash
npm create vite@latest my-app -- --template react
```

 *Explanation*: Creates a new React project using Vite’s fast bundler..

📸 _[Insert screenshot of app creation process]_

---
### 7. Move into project directory
```bash
cd my-app
```

---

### 8. Install dependencies
```bash
sudo npm install
```

---

### 9. Run the React app (with network support)
```bash
sudo npm run dev -- --host
```
📖 *Starts Vite development server on default port (usually 5173).*

💡 *Check output URL like:*  
`➜  Network:  http://<your-ip>:5173/`

```
*Explanation*: Starts the development server. App will run on [http://localhost:3000](http://localhost:3000).

📸 _[Insert screenshot of browser showing running React app]_

---

## Notes

- Ensure you have a stable internet connection during the installation process.
- The `create-react-app` is suitable for beginners and small projects.
- For advanced configuration, consider using Vite or manually configuring Webpack/Babel.

---

## Conclusion

You have successfully:

- Installed Node.js and npm  
- Installed React CLI  
- Created and ran your first ReactJS application  

Your development environment is now ready for building React-based web applications.

---

## Contact

| Name             | Email                                       |
|------------------|---------------------------------------------|
| Kawalpreet Kour  | Kawalpreet.kour.snaatak@mygurukulam.co     |

---

## References

- [React Official Docs](https://reactjs.org)
- [Node.js Downloads](https://nodejs.org)
- [Ubuntu Documentation](https://help.ubuntu.com)
