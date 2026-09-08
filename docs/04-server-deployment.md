# Server Deployment

This section documents the initial deployment and configuration of the Windows Server 2025 virtual machine that will become the domain controller.

## Step 1 — Create the Windows Server Virtual Machine

### Purpose

Create a Windows Server 2025 virtual machine that will become the domain controller.

### Procedure

1. Create a new virtual machine in VMware Workstation Pro.
2. Mount the Windows Server 2025 ISO.
3. Assign hardware resources.
4. Configure NAT networking.
5. Boot the virtual machine.

### Verification

The virtual machine boots successfully into the Windows Server installation.

### Evidence

![Virtual Machine Created](../screenshots/01%20-%20Virtual%20Machine%20Created.png)

---

## Step 2 — Install Windows Server 2025

### Purpose

Install Windows Server 2025 and complete the initial operating system configuration.

### Procedure

1. Complete the Windows installation wizard.
2. Configure the local Administrator account.
3. Sign in and verify Server Manager opens.

### Verification

Windows Server is installed successfully.

### Evidence

![Server Manager - Local Server](../screenshots/02%20-%20Server%20Manager%20-%20Local%20Server.png)

---

## Step 3 — Rename the Server

### Purpose

Prepare the server for Active Directory deployment by assigning it the hostname `DC01`.

### Procedure

1. Open the server properties.
2. Rename the server to `DC01`.
3. Restart the server.

### Verification

The server is successfully renamed to `DC01`.

### Evidence

![Server Renamed to DC01](../screenshots/03%20-%20Server%20Renamed%20to%20DC01.png)

---

## Step 4 — Rename the Network Adapter

### Purpose

Rename the default network adapter to improve administration and readability.

### Procedure

1. Open Network Connections.
2. Rename the default Ethernet adapter to `LAN`.
3. Verify the new adapter name is displayed.

### Verification

The server network adapter is clearly identified as `LAN`.

### Evidence

![Network Adapter Renamed to LAN](../screenshots/04%20-%20Network%20Adapter%20Renamed%20to%20LAN.png)

---

## Step 5 — Configure a Static IPv4 Address

### Purpose

Assign a static IP address to the domain controller before installing Active Directory.

### Procedure

1. Open IPv4 properties.
2. Assign `192.168.79.10/24`.
3. Configure the default gateway as `192.168.79.2`.
4. Set the Preferred DNS Server to `192.168.79.10`.
5. Verify connectivity.

### Verification

DC01 has a permanent IPv4 configuration suitable for Active Directory.

### Evidence

![Static IPv4 Configuration](../screenshots/05%20-%20Static%20IPv4%20Configuration.png)

---

## Step 6 — Create a VMware Snapshot

### Purpose

Create a recovery point before making major configuration changes.

### Procedure

1. Open Snapshot Manager.
2. Create a snapshot named `Fresh Windows Server Installation`.
3. Record an appropriate description.

### Verification

A restore point exists for rapid recovery if later configuration fails.

### Evidence

![VMware Snapshot Created](../screenshots/06%20-%20VMware%20Snapshot%20Created.png)

---

## Deployment Notes

This deployment follows enterprise administration practices by assigning a static IP address before installing Active Directory, using a dedicated DNS server, creating a restore point before major changes and validating each stage before progressing to the next.

These practices reduce troubleshooting time and reflect common procedures used in Windows Server environments.

---

[← Previous: Solution Architecture](03-solution-architecture.md) | [Next: Active Directory Deployment →](05-active-directory-deployment.md)
