---
title: Virtualization
---

# Virtualization
When dealing with content management systems, virtualization will most commonly refer to using a virtual machine (VM).
As a whole, the term refers to creating a virtual version of something, such as a document or a database, to give some examples.
![Virtualization](https://github.com/dfianuale/IS373/blob/main/graphics/cv1.png)

## What is a Virtual Machine?
A VM is an emulation of a computer, which includes its kernel and operating system (the latter is called the "guest machine"), that runs on a user's computer (referred to as the "host machine").
A VM can also hold containers inside, since they run on an operating system's kernel. One machine can also run more than one VM,
provided it has the capability to do so. Each VM is isolated from the others, which keeps things consistent and can also allow for
emulation of communication between two or more computers.

## VMs versus containers
* While containers run on top of an existing operating system's kernel, each VM has its own operating system and kernel.
* VMs are more capable than a container, but also more resource-consuming for the aforementioned reason.
* Both a VM and a container can be scaled up or down as needed, or copied (called "cloning"), or moved to other systems.
* As aforementioned, due to VMs having their own kernel, containers can run inside a VM, and this is common practice in the real world.
* Both containers and VMs run in isolation to other instances of themselves, which is convenient because it prevents unwanted interaction between instances.

## How do virtual machines work?
Virtual machines are, at the most basic level, self-contained servers that use software instead of hardware for operations. The virtual macine server includes alloted RAM, CPU, storage, and a network interface, effectively emulating a real computer. The key difference is that instead of these resources being stored on dedicated hardware like with a pre-built computer, they are borrowed from the host machine server, and can be
reallocated to other virtual machines as necessary.

## Oracle VirtualBox
There are many softwares available online that can be used to create and run a virtual machine. Such softwares are called "hypervisors", and their main purpose is to manage virtual machines and keep them isolated from one another to prevent unwanted interactions. Some examples of commonly used hypervisors are Oracle VM VirtualBox, VMWare Workstation, and Microsoft Hyper-V, among others.
This documentation will teach how to install and use Oracle VM VirtualBox. 

VirtualBox is a Type 2 hypervisor (hosted), which means the VM runs inside of a dedicated test environment on one's operating system. Some hypervisors are Type 1 (bare-metal) instead, meaning they run the VM directly on the host machine's hard drive.

Before setting up a VM, there are some prerequisites that must be met:
* Your machine must support virtualization (this can be checked from BIOS or UEFI on startup)
* You must have installed a hypervisor, which will be covered below with VirtualBox.
* You must have a raw disc image file (.iso extension) of the guest machine operating system you want to install on your VM.

### Installing and setting up VirtualBox
VirtualBox can be downloaded from <virtualbox.org> for Windows, Linux, and Mac OS. The official documentation for the program also contains installation instructions at <https://www.virtualbox.org/manual/topics/installation.html#installation> for all three platforms.
After installation, you must open the program and configure it to use your network and host machine correctly. A number of settings such as screen resolution, proxy servers, interface theme and more are also available.

### Creating a Virtual Machine
To set up a VM, first choose the option **New** to be shown to the workflow to create a VM.
* First you must give the VM a name. This name will be shown in VirtualBox Manager and the VM's files on disk, so be sure to choose a straightforward name that includes the OS of the virtual machine.
* Select the install location for the VM and your OS disc image. If your guest OS has editions, you must specify the edition as well. VirtualBox will attempt to populate as many fields as it can depending on which OS you are using, but if it does not fill a field, you must fill it in manually.
* To have the OS install automatically, you can choose an **Unattended Installation** and set the options for the OS ahead of time. You can also choose to skip this method and have the OS image mount on the virtual DVD for you to install it manually from within the VM.
* Whichever of the above you choose will be followed by setting up the virtual hardware, including base RAM, processors, EFI, and a hard disk.
**WARNING:** The amount of RAM you allocate to the VM *cannot* be used by the host machine OS when the VM is running. Set the amount carefully.

After these things are set up, you can run the virtual machine from the VirtualBox interface. While it is running, you will have access to a status bar that includes tabs for storage, networking, audio, USB, and more settings. By default, the guest OS will take control of your keyboard and mouse from the host OS. To return control of the keyboard to the host OS, you can press the designated Host key. On Windows and Linux the default host key is Right Ctrl, on Mac it is Left Command.

Additional instructions for using VirtualBox can be found at <https://www.virtualbox.org/manual/topics/Introduction.html#Introduction>.

Sources:
* https://www.virtualbox.org/manual/topics/Introduction.html#Introduction
* ChatGPT
* https://www.serverwatch.com/virtualization/virtual-machines/