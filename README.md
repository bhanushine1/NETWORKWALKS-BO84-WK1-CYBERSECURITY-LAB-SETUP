# NETWORKWALKS-BO84-WK1-CYBERSECURITY-LAB-SETUP
# Cybersecurity Lab Setup — Kali Linux & VirtualBox

## 📌 Project Overview

This project documents the setup of a cybersecurity testing lab using Oracle VirtualBox and Kali Linux on a Windows 11 host machine. The lab environment is intended for learning cybersecurity fundamentals, network configuration, and ethical hacking in a controlled virtual environment.

## 🎯 Objectives

- Install and configure Oracle VirtualBox.
- Set up Kali Linux as a cybersecurity testing machine.
- Configure a NAT Network with the subnet `10.0.0.0/24`.
- Assign Kali Linux the IP address `10.0.0.2/24`.
- Enable internet connectivity for Kali Linux.
- Configure shared clipboard, drag-and-drop, and shared folders.
- Create a virtual machine snapshot for recovery.

## 🛠️ Tools and Technologies

| Tool | Purpose |
|---|---|
| Windows 11 | Host operating system |
| Oracle VirtualBox | Virtualization software |
| Kali Linux | Cybersecurity testing operating system |
| NAT Network | Virtual network configuration |

## 💻 System Requirements

Recommended specifications:

- 8 GB RAM or more
- 256 GB SSD or more
- Intel Core i3/i5 or equivalent processor
- Windows 11 host operating system
- Sufficient free disk space for the Kali Linux virtual machine

## ⚙️ Lab Configuration

| Component | Configuration |
|---|---|
| Host OS | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Guest OS | Kali Linux |
| Network Type | NAT Network |
| Network Subnet | `10.0.0.0/24` |
| Kali IP Address | `10.0.0.2/24` |
| Default Gateway | `10.0.0.1` (if applicable to the configured network) |
| Internet Access | Enabled |
| Snapshot | Created after successful configuration |

## 🚀 Installation Steps

### Step 1: Install VirtualBox

Download VirtualBox for Windows from:

https://www.virtualbox.org/wiki/Downloads

Run the installer and complete the installation.

### Step 2: Download Kali Linux

Visit the official Kali Linux website:

https://www.kali.org/get-kali/

Select the pre-built VirtualBox virtual machine image and extract the downloaded archive.

### Step 3: Import Kali Linux

1. Open VirtualBox Manager.
2. Click **Add**.
3. Browse to the extracted Kali Linux folder.
4. Select the `.vbox` file.
5. Open the virtual machine.

### Step 4: Configure the NAT Network

1. Open VirtualBox Network Manager.
2. Create a NAT Network.
3. Configure the network as `10.0.0.0/24`.
4. Save the network configuration.
5. Attach Kali Linux to this NAT Network.

### Step 5: Configure Kali Linux

Configure the network interface with the required IP address:

- IP address: `10.0.0.2`
- Network prefix: `/24`
- Gateway: `10.0.0.1`, if applicable

Verify the configuration using:

```bash
ip addr
ip route
```

### Step 6: Configure Virtual Machine Features

In VirtualBox settings:

- Enable Shared Clipboard.
- Enable Drag'n'Drop.
- Configure a shared folder pointing to the host's Downloads folder.
- Enable Auto-mount for the shared folder.

### Step 7: Test Network Connectivity

Check the IP configuration:

```bash
ip addr
```

Test DNS resolution:

```bash
ping -c 4 networkwalks.com
```

### Step 8: Create a Snapshot

After confirming that Kali Linux starts correctly and the network configuration works:

1. Open VirtualBox Manager.
2. Select the Kali Linux virtual machine.
3. Open the Snapshots section.
4. Create a snapshot named `Kali-Lab-Setup-Complete`.

## 🔐 Learning Outcomes

- Understanding virtualization and virtual machines.
- Configuring a NAT Network.
- Learning basic Linux network commands.
- Testing network and internet connectivity.
- Configuring shared folders and clipboard integration.
- Creating virtual machine snapshots for recovery.

## 🛡️ Ethical Use

This environment is intended for authorized cybersecurity education, defensive security learning, and ethical hacking practice. Conduct testing only on systems and networks you own or have explicit permission to assess.

## 📚 References

- Networkwalks Cybersecurity Lab Setup assignment
- [Oracle VirtualBox](https://www.virtualbox.org/)
- [Kali Linux](https://www.kali.org/)
