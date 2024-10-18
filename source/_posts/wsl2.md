---
title: wsl2
---

# The Windows Subsystem for Linux (WSL)
Today, some computers offer dual boot functionality, which allows a user to install more than one operating system at the same time, on the same machine. But doing this usually requires the installation of extra software or an overhead, and only one of the operating systems can be actively used at a time. The Windows Subsystem for Linux (WSL) is an alternative option that allows Windows users to install a full installation of Linux, complete with utilities, BASH commands, and application compatibility, onto an existing installation of Windows.

## Why you should use WSL2
With WSL2, users can develop programs for Linux and store files in an isolated environment, while still having the ability to communicate with the host machine as needed. Users can utilize the BASH shell and other command-line tools to run scripts and applications. WSL2 is not limited to Ubuntu either - users can select which Linux distribution to install on the host machine. 

## How it works
WSL2 runs a Linux kernel inside of a lightweight virtual machine, and the distribution of Linux (Ubuntu, Debian, etc., also called a "distro") then runs as an isolated container inside of that virtual machine. There are two versions of the Windows Subsystem for Linux: WSL1 and WSL2. Compared to WSL1, WSL2 is more capable, offering increased system performance and full system call compatibility, a system call being an entry point into the operating system from a process. When installing the subsystem, in addition to choosing which distro to install, users can specify whether that installation uses WSL1 or WSL2.

# How to install the Windows Subsystem for Linux
The only prerequisite to install WSL is the operating system on the host machine. It must be running either Windows 11, or Windows 10 version 2004 or higher. To install WSL2 from the command line, enter this command into the Command Prompt (CMD) or Powershell:

> wsl --install

By default, this command will install WSL2 and Ubuntu on the host machine. To choose a Linux distro manually, append this flag onto the above command:

> -d (distro name here)

\* Note: Running CMD or Powershell as an administrator is not required to install WSL2.

The command with the flag added can also be used to install another Linux distro after one has already be installed. After installing a distribution, the host machine must be restarted for the install to take full effect. The first time a distro starts up, a command window will open which will tell you to wait while the distro unpacks files to store on the host machine's system. Afterwards, it will prompt you to either create or log into a Unix account, Unix being the OS that Linux is built off of.

To switch the version of a Linux installation from WSL2 to WSL1 or vice versa:

> wsl --set-version (distro name here) (1/2)

Once a distro is installed and unpacked, it can be run from the Start menu by typing its name and opening the program, which will open it in a console window. You can also open it by typing its name into a Command Prompt window, which will open the distro in a separate console. To open it in the current window, type:

> wsl (distro name here)

Sources:
* https://learn.microsoft.com/en-us/windows/wsl/about
* https://learn.microsoft.com/en-us/windows/wsl/install

Additional Resources:
* https://learn.microsoft.com/en-us/windows/wsl/setup/environment
* https://learn.microsoft.com/en-us/windows/wsl/basic-commands