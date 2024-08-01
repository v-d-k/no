### 1. Explain any one linux filter.

`more`: A Linux filter that displays the content of a file one screen at a time. For example, `more file.txt` shows the content of `file.txt`, allowing you to scroll through with the spacebar or Enter key.

### 2. Forward zone on Dns. eg of forward zone.

A forward zone in DNS is used to forward queries for a specific domain to another DNS server. 

**Example**: 
In `named.conf`:

```conf
zone "example.com" {
    type forward;
    forwarders { 8.8.8.8; };
};
```

This configuration forwards all queries for `example.com` to the DNS server at `8.8.8.8`.

### 3. Assign user to sudo group.

To assign a user to the sudo group, use the following command:

```sh
sudo usermod -aG sudo username
```

Replace `username` with the actual username.

### 4. Three rules of UFW.

1. **Allow Incoming SSH**:
   
   ```sh
   sudo ufw allow ssh
   ```

2. **Deny All Incoming Traffic**:
   
   ```sh
   sudo ufw default deny incoming
   ```

3. **Allow All Outgoing Traffic**:
   
   ```sh
   sudo ufw default allow outgoing
   ```

### 5. Different between soft link and hard link.

**Soft Link (Symbolic Link)**:

- Points to the original file's path.
- Can link to directories.
- Breaks if the original file is deleted.
- Created with `ln -s target linkname`.

**Hard Link**:

- Points to the original file's inode.
- Cannot link to directories.
- Remains valid even if the original file is deleted.
- Created with `ln target linkname`.

### 6. There is example.txt owner is abc file permission are -rwx-r--r-- can administration write to this file.

No, the administrator cannot write to `example.txt`. The file permissions `-rwx-r--r--` mean that only the owner (`abc`) has write permission. The administrator would need to change the file permissions or ownership to write to it.

### 7. What are system generated group.

System-generated groups are default groups created by the operating system during installation for managing system resources and permissions. Examples include:

- `root`: Superuser group with full system access.
- `daemon`: Used for system daemons and services.
- `bin`: Used for binary executables.
- `sys`: Used for system files and administration.
- `adm`: Used for system monitoring and logs.

### 8. Difference between SUID and HUID.

### 9. Explain boot process in linux.

### 10. Explain any 3 option in rpm.

1. **`-i` (Install)**:
   
   - Installs a new RPM package. Example: `rpm -i package.rpm`.

2. **`-u` (Upgrade)**:
   
   - Upgrades an existing package to a newer version. Example: `rpm -u package.rpm`.

3. **`-e` (Erase)**:
   
   - Removes an installed package. Example: `rpm -e package_name`.

### 11. Port Forwarding.

### 12. How owner and group file can be changed.

To change the owner and group of a file, use the `chown` command:

- **Change Both Owner and Group**:
  
  ```sh
  sudo chown newowner:newgroup filename
  ```
  
  Example: `sudo chown alice:staff file.txt` changes the owner to `alice` and the group to `staff`.

### 13. Software management using apt.

**`apt`** is a command-line tool for managing software packages on Debian-based systems. Here are some common commands:

1. **Update Package List**:
   
   ```sh
   sudo apt update
   ```
   
   Fetches the latest list of available packages and their versions.

2. **Upgrade Installed Packages**:
   
   ```sh
   sudo apt upgrade
   ```
   
   Upgrades all installed packages to their latest versions.

3. **Install a Package**:
   
   ```sh
   sudo apt install package_name
   ```
   
   Installs a new package. Example: `sudo apt install vim`.

### 14. what is significance visudo command.

`visudo` safely edits the `/etc/sudoers` file and checks for syntax errors before saving changes, preventing configuration issues that could lock out sudo access.

### 15. What is inode.

An inode is a data structure on a filesystem that stores metadata about a file or directory, such as its size, owner, permissions, and location on the disk, but not its name.

### 16. What is MBR.

MBR (Master Boot Record) is a partitioning scheme used on disks, containing the bootloader code and partition table that defines how the disk is divided into partitions. It is located in the first sector of the disk.

### 17. What information is stored in passwd

The `/etc/passwd` file stores basic information about user accounts, including:

1. **Username**: The user's login name.
2. **Password**: Historically, this was the user's password, but now it typically contains a placeholder (e.g., `x` or `*`) and actual passwords are stored in `/etc/shadow`.
3. **User ID (UID)**: Numeric identifier for the user.
4. **Group ID (GID)**: Numeric identifier for the user's primary group.
5. **User Information**: Optional field for additional details about the user, such as the full name.
6. **Home Directory**: Path to the user's home directory.
7. **Shell**: Path to the user's default shell.

### 18. Difference between Nat and Natnetwork.

**NAT (Network Address Translation)**:

- Translates private IP addresses of a virtual machine (VM) to the host's public IP address.
- Allows multiple VMs to share a single public IP.
- VMs can access external networks, but external networks cannot initiate connections to the VMs directly.

**NAT Network**:

- A virtual network mode in virtualization platforms like VirtualBox that uses NAT.
- Allows multiple VMs to communicate with each other and with the external network using NAT.
- Provides isolated network segments with NAT capabilities, where VMs within the NAT Network can interact as if they are on the same subnet.

### 19.  What is host file.

The `/etc/hosts` file maps hostnames to IP addresses. It provides a way to resolve hostnames to IP addresses locally. It contains entries in the format:

```
IP_address hostname [aliases]
```

For example:

```
127.0.0.1 localhost
192.168.1.10 myserver
```

### 20. Reverse zone of dns server why it is required.

A reverse zone in a DNS server maps IP addresses back to hostnames. It is required for:

1. **Reverse DNS Lookups**: To resolve an IP address to its associated hostname, useful for applications like email servers to verify the source of incoming connections.
2. **Network Troubleshooting**: Helps diagnose network issues by providing hostname information when given an IP address.
3. **Security**: Enhances security by allowing systems to verify the identity of connecting hosts through reverse lookups.

# 5 Marks

### 1. linux based machines as a router.

### 2. Why and what partitions are used.

### 3. Configure Dhcp server for network address 192.168.128.0/24

### 4. how you can connect remotely to linux server discuss 3 ways

### 5. what hardware configuration is required for linux installation.
