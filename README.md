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

### Step 2: Install Node.js (Required by React)

ReactJS requires Node.js and npm to work. We'll install Node.js v18.

#### ➤ 2.1 Download Node.js Setup Script

```bash
curl -sL https://deb.nodesource.com/setup_18.x -o nodesource_setup.sh
```

 *Explanation*: Downloads the Node.js installation script for version 18.

📸 _[Insert screenshot]_

#### ➤ 2.2 Run the Setup Script

```bash
sudo bash nodesource_setup.sh
```

 *Explanation*: Adds the Node.js package source to your system.

📸 _[Insert screenshot]_

#### ➤ 2.3 Install Node.js

```bash
sudo apt-get install -y nodejs
```

 *Explanation*: Installs Node.js and npm (Node Package Manager).

📸 _[Insert screenshot after installation]_

---

### Step 3: Verify Node.js and npm Installation

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

### Step 4: (Optional) Update npm

```bash
sudo npm install -g npm@latest
```

 *Explanation*: Updates npm to the latest version.

📸 _[Insert screenshot after update]_

---

### Step 5: Install React CLI Globally

```bash
sudo npm install -g create-react-app
```

 *Explanation*: Installs the React command-line interface globally.

📸 _[Insert screenshot after installation]_

#### ➤ Check CLI Version

```bash
create-react-app --version
```

 *Explanation*: Verifies that the React CLI is installed.

📸 _[Insert screenshot showing version]_

---

### Step 6: Create a React Application

```bash
npx create-react-app my-react-app
```

 *Explanation*: Creates a new React application in a folder named `my-react-app`.

📸 _[Insert screenshot of app creation process]_

---

### Step 7: Run the React Application

```bash
cd my-react-app
npm start
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
