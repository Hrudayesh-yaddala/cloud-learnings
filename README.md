Introduction to User Management in Linux

Linux is a multi-user operating system, allowing multiple users to access and work on the system simultaneously.
User management is crucial for:

Security

Controlled access

System integrity

🛠️ Setup Linux Environment (Windows / macOS)
Prerequisites

Install Docker Desktop
👉 https://docs.docker.com/desktop/setup/install/windows-install/

Install WSL (Windows users only)

wsl --install

📦 Run Ubuntu Linux Container (Persistent Setup)

Create a folder named ubuntu-data anywhere (example: D:/cloudlearning/ubuntu-cont)

Run the below command in PowerShell (update your path):

docker run -dit `
  --name ubuntu-container `
  --hostname ubuntu-dev `
  --restart unless-stopped `
  --cpus="2" `
  --memory="4g" `
  --mount type=bind,source="D:/cloudlearning/ubuntu-cont",target=/data `
  -v /var/run/docker.sock:/var/run/docker.sock `
  -p 2222:22 `
  -p 8080:80 `
  --env TZ=Asia/Kolkata `
  --env LANG=en_US.UTF-8 `
  ubuntu:latest /bin/bash

📁 Important System Directories
Directory	Description
/boot	Bootloader files (not relevant inside containers)
/usr	Installed applications & libraries
/var	Logs, cache, variable data
/etc	System configuration files
👤 User & Application-Specific Directories
Directory	Description
/home	Home directories for users
/opt	Third-party application installation path
/srv	Service-specific data
/root	Root user’s home directory
📘 Authentication & Account Information Files
File	Purpose
/etc/passwd	Stores basic user info
/etc/shadow	Stores encrypted passwords
/etc/group	Stores group info
/etc/gshadow	Secure group details
👥 User Management Commands
⭐ Create a User
adduser username

⭐ Switch to Another User
su - username

⭐ Set or Change Password
passwd username

⭐ Modify User

Change username

usermod -l new_username old_username

⭐ Delete User (without removing home directory)
userdel username
