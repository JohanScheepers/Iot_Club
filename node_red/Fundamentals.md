# Fundamentals

## 1.  Introduction to Node-RED

Node-Red had its birth at IBM early 2013 when they wanted to visualize MQTT topics. The main developers at that stage were Nick O'Leary and Dave Conway-Jones.

In September 2013 it were open-sourced and made available to the public. And by October 2016 became one of the founding projects of the JavaScrip Foundation (JS Foundation). Later in March 2019 the JS Foundation merged with Node.js Foundation to form the OpenJS Foundation.

Today it has moved on to be a Ubiquitous Low-Code Tool, Node-Red has as moved far beyond just IoT. It is now used globally for: industrial automation (IIoT), home automation, API creation, ETL/data flow pipelines, and rapid prototyping, all powered by its simple, visual, flow-based programming model running on Node.js.

## 2. Installation and Setup

Setting up Node-RED is surprisingly straightforward, considering the power it unlocks. The most critical thing to remember is that Node-RED runs on top of Node.js, so that's your essential first step.

### 2.1 🛠️ Installation & Setup: The Two-Step Process
The standard, most flexible way to install Node-RED on Windows, macOS, or Linux is via its package manager, npm.

#### Step 1: Install Node.js
Node-RED is a Node.js application, so you must install the Node.js runtime first.

To install Node.js, follow these steps, which are generally applicable across Windows, macOS, and Linux, with slight variations depending on the operating system:

- **1.1. Download**:
    - [Visit the official Node.js website.](https://nodejs.org/en/download/)
    - Download the appropriate installer for your operating system and architecture (32-bit or 64-bit). The LTS (Long Term Support) version is recommended for most users due to its stability.

- **1.2. Install:**
    - Locate the downloaded installer file (e.g., a .msi file on Windows, a .pkg on macOS, or a package for Linux).
    - Double-click the installer to begin the setup wizard.
    - Follow the prompts in the wizard, accepting the license agreement and using the default settings for installation unless you have specific reasons to change them. This typically includes installing the Node.js runtime and the npm package manager.

- **1.3. Complete the Setup:**
    - The installer may offer to install additional tools like Python and Visual Studio Build Tools, which are necessary for compiling some native Node.js modules. Choose to install these if prompted.
    - Click "Install" to begin the installation process.
    - Once the installation is complete, click "Finish" to close the wizard.

- **1.4. Verify:** 
    - Open your terminal or command prompt.
    - Run the following commands to check the installed versions of Node.js and npm:

    ```
    node -v
    npm -v
    ```
You should see version numbers for both node and npm (Node Package Manager). If you do, you're good to go!
    ![](./images/nodejs_v.PNG)

#### Step 2: Install and Run Node-RED
With Node.js and npm in place, installing Node-RED is a single command.

- **2.1. Install Node-RED (Globally)**
Run the following command in your terminal/command line:

    ```
    # This command installs Node-RED globally, allowing you to run it from any directory
    npm install -g --unsafe-perm node-red
    ```
    💡 Note on --unsafe-perm: This option is often needed to correctly install dependencies that require compiling native code (especially on Linux/Mac). It ensures smooth installation. On Windows, the sudo prefix is not used.

#### 2. Run Node-RED
Once the installation is complete, you can start the Node-RED server with a simple command:
```
node-red
```

  ![](./images/node_red_start.PNG)

- **Access the Editor**
When Node-RED starts, you will see a bunch of log messages, including a line that tells you the server is running.
    - Look for the line that says: Server now running at http://127.0.0.1:1880/ (or http://localhost:1880/

     - Open your web browser and navigate to that address.
     ![](./images/node_red_ui.PNG)


Congratulations! You are now looking at the Node-RED flow editor, ready to start dragging, dropping, and wiring up your first automation flow.

---

## 3.Raspberry Pi

We are going to use a Raspberry PI for this course, and the following on course. It will be good at this point to get you Pi up and running.


### 3.1 🛠️ Installation & Setup PI:
The Raspberry Pi has a dedicated installation script that handles the Node.js install, Node-RED install, and sets it up as a system service for easy management and automatic startup.

```
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
```

This script is the recommended (and easiest) way to get it running on any Debian-based system like Raspberry Pi OS.

### 3.1 Running locally

Open the terminal and run the command
```
node-red
```
You can stop Node-Red with the command by pressing Ctrl-C or by closing the terminal window.

Due to limited memory on you Raspberry PI we need start Node_red with the following command.
```
node-red-pi --max-old-space-size=256
```
This will tell the underling Node.js process to free up some additional unused memory.

### 3.2 Autostart at boot
If you want Node-RED to start automatically when the system boots or on re-boot. You can enable the service to autostart with the following command.
```
sudo systemctl enable nodered.service
```
To disable the service on the next boot, run the command
```
sudo systemctl disable nodered.service
```

### 3.3 Opening the Editor
Once Node-Red is running, you can open it in the browser.

You can navigate to http://localhost:1880 or http://127.0.0.1:1880/ or you can navigate to the Raspberry PI IP address and use port 1880.

You can find the PI IP by running the command in the terminal.
```
hostname -I
```

In this case my IP is 10.0.0.4

![](./images/node_red_10_0_0_4.PNG)