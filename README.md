<div align="center">
  <h1>Semaphore Trusted Setup Ceremony</h1>

  <p>Semaphore is a zero-knowledge protocol for anonymous signaling on Ethereum, enabling users to prove membership in a group and broadcast signals. Such as votes, endorsements, or messages. Without revealing their identity.</p>

  <img width="680" height="358" alt="image" src="https://github.com/user-attachments/assets/07d6bfd6-7139-4737-8e4a-4d6c002166c2" />


  <p>The latest ceremony’s running until August 18th 2025.</p>
</div>

## Contribute
You can contribute to the ceremony using either a web browser or the command-line interface (CLI).  
* **Web-browser**: Simply connect your github in [ceremoy.pse.dev](https://ceremony.pse.dev/projects/Semaphore%20Binary%20Merkle%20Root%20Fix), press on **Contribute** and wait for your contribution to finish.
* **CLI**: Follow the below guide to install and participate the ceremony in a terminal using command-line. _This method is way more stable than the web version._

---

## Requirements
### Operating System
You need one of these to join the ceremony:
* Linux
* MacOS system
* [WSL (linux) on Windows](https://github.com/0xmoei/Install-Linux-on-Windows)
* [VPS with Ubuntu OS ](https://github.com/0xmoei/Linux_Node_Guide)

### GitHub Account
Your GitHub account must meet the following criteria:
* At least a month old.
* At least one public repository.
* At least following 5 GitHub accounts and have at least 1 follower.
* Must allow the ceremony tools to read and write GitHub Gists on your account.

### Internet Connection
You need a stable internet connection on your local system or a VPS to stay in the ceremony queue for hours, waiting for your turn.

---

## Install Dependecies
1. Packages:
```
sudo apt-get update && sudo apt-get upgrade -y

sudo apt install curl screen iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev ca-certificates  -y
```

2. Install NVM
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source .bashrc
```

3. Install Node.js 18
```bash
nvm install 18 
nvm use 18
```
```
source ~/.bashrc
```

---

## Install Ceremony
### Step 1. Create a directory in your home folder to run the ceremony from:
```
mkdir ~/trusted-setup && cd ~/trusted-setup
```

### Step 2: Install CLI:
```
npm install -g @p0tion/phase2cli
```

### Step 3: Authenticate with GitHub:
To contribute to the ceremony, you’ll need a legit GitHub account.

Run this command in your terminal:
```
phase2cli auth
```
* This will prompt you to open a browser and visit [https://github.com/login/device](https://github.com/login/device)
* Copy the provided auth code in terminal and paste in the auth page . Click "Authorize" to continue.

---

## Contribute Ceremony
### Open a screen
Open a screen so the ceremony keeps going in the background—might take hours before it’s your turn.
* Screen is useful for VPS, not WSL. If you close the terminal in WSL, your screen session is killed
```
screen -S ceremony
```

### Contribute to the ceremony
```
phase2cli contribute -c semaphore-binary-merkle-root-fix
```
* You can either hit enter for randomly, or pick manually and type any letter or number yourself.

<img width="689" height="302" alt="image" src="https://github.com/user-attachments/assets/8830a33c-8e97-4cd1-8b6e-9ca0d7312dd7" />

### Screen commands
* Minimize screen: `Ctrl`+`A`+`D`
* Return to screen: `screen -r ceremony`
* Kill ceremony when inside screen: `Ctrl`+`C`
* Kill screen when inside screen: `Ctrl`+`D`
* Kill screen when outside screen: `screen -XS ceremony quit`
* screens list: `screen -ls`

---

## Notes:
* Contributing may take some time, depending on the number of circuits (**32 in this run**) and the queue of contributors.
* If your connection is interrupted or an error occurs, simply re-run the same command — it will pick up from where it left off.

### After completing your contribution, you will be invited to share a message on X or your preferred social platform! 🎉

---

## Cleanup & Logout
After completing your contribution to the ceremony, it’s recommended to clean up your local files and revoke GitHub authorization for security:
```
phase2cli clean
```
```
phase2cli logout
```
Delete the ceremony folder too if you don’t need it:
```
rm -rf ~/trusted-setup
```

---

## FAQs
Q: I received the message “Your contribution took longer than the estimated time and you were removed as the current contributor.” What should I do?
<img width="1600" height="71" alt="image" src="https://github.com/user-attachments/assets/bea707ab-05fd-4154-bbc3-4a27e2ec7933" />

A: If your connection is slow, some contribution steps may take longer than expected, which can lead to a timeout, often during file download and upload. When this happens, you are automatically removed as the current contributor. You will need to wait for the predefined timeout period to expire before you can rejoin and continue your contribution. Once the timeout has passed, you may restart from the same circuit. To avoid repeated timeouts, we recommend switching to a machine with a faster and more stable internet connection before attempting to try again.

Here are some timeout examples:

<img width="1600" height="202" alt="image" src="https://github.com/user-attachments/assets/26e44210-1351-4475-a2ef-5bd4ce5c0c93" />

<img width="1600" height="522" alt="image" src="https://github.com/user-attachments/assets/c8471cc9-f32c-4e45-8487-73a899393c2d" />

#

Q: I received the message “The waiting time (timeout) to retry the contribution has not yet expired.” What should I do?

<img width="1534" height="400" alt="image" src="https://github.com/user-attachments/assets/ae7fad2f-0bd5-4092-aca2-c617d15e8130" />

A: After a timeout occurs—usually due to a slow or unstable connection, or disk availability issues—you must wait for the predefined timeout period to expire before you can retry your contribution. Attempting to rejoin before this period ends will result in this message. Please wait until the timeout has fully passed, then try again. To improve your chances of a successful contribution, we recommend switching to a machine with a faster and more stable internet connection and ensuring there is sufficient free disk space for the process to complete successfully.

