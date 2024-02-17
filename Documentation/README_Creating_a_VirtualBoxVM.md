# Documentation: Creating a VirtualBox VM


## Introduction

This section provides an overview of the purpose behind documenting the VirtualBox setup process, highlighting the importance of following specific configurations for the "Born to Be Root" project.


## Requirements

## Step 1: Download and Install VirtualBox

1. **Download VirtualBox**:
   
   - Go to the [VirtualBox website](https://www.virtualbox.org/wiki/Downloads) and download the latest version for macOS.
     
2. **Install VirtualBox**:
   - Open the downloaded file and follow the installation instructions. You might need to allow the installation in your system preferences due to macOS security settings.


## Step 2: Download the Debian or Rocky ISO

- **Debian**: Visit the [Debian download page](https://www.debian.org/download) and download the latest stable ISO file. 
- **Rocky Linux**: Go to the [Rocky Linux download page](https://rockylinux.org/download) and get the latest stable ISO.

### What´s the best option?

If you're new to Linux and looking for a general-purpose operating system to get started with, especially for personal use or learning, Debian is easier and more accessible. It has a vast community and resources to help beginners. Rocky Linux, on the other hand, is more tailored for professional or enterprise server environments where RHEL compatibility is important.

## Step 3: Create a New Virtual Machine

1. **Open VirtualBox**:
   - Launch VirtualBox from your Applications folder.
2. **Create New VM**:
   - Click on "New" to start creating your virtual machine. Name your VM (e.g., "BornToBeRoot"), select the type (Linux), and version (Debian or other Linux versions depending on your ISO).
3. **Allocate RAM**:
   - Assign at least 2GB (2048 MB) if possible.
4. **Create a Virtual Hard Disk**:
   - Choose "Create a virtual hard disk now", a dynamically allocated disk, and allocate at least 10GB of space.
