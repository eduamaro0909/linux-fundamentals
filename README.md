# 🐧 Linux Training for L2 Support

This document contains the **training syllabus** and the **hands-on labs** for Cristopher, focused on preparing him for technical interviews for an **L2 Support role with Linux**.

---

## 📘 Weekly Syllabus

### Week 1-2: Fundamentals + Users/Permissions + Processes and Services
- Basic history of Linux and differences with Windows.
- Common distributions (Ubuntu, CentOS, RedHat, Debian).
- File system structure (`/`, `/etc`, `/var`, `/home`, `/usr`).
- Kernel, shell, and processes concepts.
- User and group management.
- File permissions (`rwx`) and special permissions (SUID, SGID, sticky bit).
- Process and service management (`ps`, `top`, `kill`, `systemctl`).

### Week 3-4: Networking + Storage + Scripting
- Networking commands: `ping`, `ss`, `traceroute`, `curl`, `wget`.
- Firewall configuration (`ufw`, `iptables`).
- Disk commands: `df`, `du`, `lsblk`, `mount`.
- Partitions and file systems (ext4, xfs).
- Bash scripting basics.
- Task automation with `cron`.

### Week 5-6: Advanced Troubleshooting + Cloud
- Logs analysis (`journalctl`, `/var/log/`).
- Bottleneck diagnosis (CPU, memory, I/O).
- Troubleshooting services (Apache, Nginx, SSH).
- Managing instances in AWS/GCP.
- SSH access with key pairs.
- Basic server hardening.

### Week 7: Final Integrated Case
- Incident resolution in a Linux cloud server.
- Full troubleshooting of services, permissions, network, and storage.
- Documentation of findings and preventive measures.

---

## 🧪 Hands-on Labs

### Week 1-2: Fundamentals + Users/Permissions + Processes and Services
**Scenario:** The freshly installed Linux server has access and permissions issues.  

**Tasks:**
1. Explore the directory hierarchy: `/etc`, `/var`, `/home`.
2. Create 2 users (`dev1`, `dev2`) and one group (`developers`).
3. Set file permissions so only `dev1` can read a file in his home.
4. Install and verify the SSH service is running.
5. Simulate a frozen process with `sleep 10000` and kill it.

---

### Week 3-4: Networking + Storage + Scripting
**Scenario:** The server shows connectivity issues and reports low disk space.  

**Tasks:**
1. Check connectivity to `8.8.8.8` and `google.com` (IP vs DNS).
2. Check open ports (`ss -tulnp`).
3. Configure firewall to block and then allow port 22.
4. Mount an additional simulated disk using `dd` and `mount`.
5. Detect which folder consumes the most space in `/var`.
6. Write a Bash script to delete files larger than 50MB in `/tmp`.

---

### Week 5-6: Advanced Troubleshooting + Cloud
**Scenario:** A web service stopped working in the cloud.  

**Tasks:**
1. Install Apache/Nginx and verify access on port 80.
2. Break the DocumentRoot configuration and check logs for errors.
3. Simulate a full `/var` partition and free space.
4. Configure SSH access with key pairs instead of passwords.
5. Fix Apache not starting due to firewall blocking port 80.

---

### Week 7: Final Integrated Case
**Scenario:** A client reports their cloud-based web application is down. The server responds to ping but the app doesn’t load.  

**Simulated issues:**
1. Apache stopped.
2. Wrong file permissions (`chmod 000` on index.html).
3. Disk `/var` filled with a dummy file.
4. Firewall blocking port 80.
5. Missing cleanup script for `/tmp`.

**Evaluation Criteria:**
- Detect and fix each issue.
- Correctly use logs, network, permissions, process, and storage commands.
- Propose preventive measures to avoid recurrence.

---
