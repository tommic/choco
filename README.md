# Chocolatey and Git Setup

This project helps you quickly set up your preferred software using Chocolatey and Git.

## Installing Chocolatey

First, you need to download and install Chocolatey. This can be done with the following (long) command:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.SecurityProtocolType]::Tls12; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

### Installing Git

Next, you need to install your first tool with Chocolatey.  
**Git** is a distributed version control system primarily used for managing source code. It helps developers track changes, work on multiple features simultaneously, and collaborate easily in teams.

Install Git with the following command:

```powershell
choco install git -y
```

> **Note:** After the installation, close and reopen your terminal so that Windows recognizes that Git is installed.

## Cloning the Package Lists

Navigate to your user directory and clone the repository containing the package lists:

```powershell
cd ~
git clone https://github.com/tommic/choco_pack.git
```

Now all the software packages are available in the `choco_pack` directory in your user folder.

## Installing the Package Lists

To install the package list, run the following command:

```powershell
choco install basic.config -y
```

> The `-y` option ensures that you don’t have to manually confirm each package during the installation.
