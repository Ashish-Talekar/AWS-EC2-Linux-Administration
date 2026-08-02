# AWS EC2 Linux Server Administration - Commands

## 1. Verify Operating System

```bash
hostnamectl
```

```bash
cat /etc/os-release
```

---

## 2. Update System

```bash
sudo yum update -y
```

---

## 3. Install Apache HTTP Server

```bash
sudo yum install httpd -y
```

---

## 4. Start Apache Service

```bash
sudo systemctl start httpd
```

---

## 5. Enable Apache on Boot

```bash
sudo systemctl enable httpd
```

---

## 6. Check Apache Status

```bash
sudo systemctl status httpd
```

---

## 7. Navigate to Web Directory

```bash
cd /var/www/html
```

---

## 8. Create Website

```bash
sudo vi index.html
```

---

## 9. Verify Website Content

```bash
cat index.html
```

---

## 10. Create Linux User

```bash
sudo useradd clouduser
```

---

## 11. Verify User

```bash
tail -n 1 /etc/passwd
```

---

## 12. Create Linux Group

```bash
sudo groupadd developers
```

---

## 13. Verify Group

```bash
tail -n 1 /etc/group
```

---

## 14. Add User to Group

```bash
sudo usermod -aG developers clouduser
```

---

## 15. Verify User Membership

```bash
id clouduser
```

---

## 16. Create Test File

```bash
sudo touch file1
```

---

## 17. Change File Permission

```bash
sudo chmod 777 file1
```

---

## 18. Change File Ownership

```bash
sudo chown clouduser file1
```

---

## 19. Verify File Permission

```bash
ls -l
```

---

## 20. Check Available Storage

```bash
lsblk
```

---

## 21. Format Amazon EBS Volume

```bash
sudo mkfs -t xfs /dev/nvme1n1
```

---

## 22. Verify File System Type

```bash
sudo file -s /dev/nvme1n1
```

---

## 23. Create Mount Directory

```bash
sudo mkdir /data
```

---

## 24. Mount EBS Volume

```bash
sudo mount /dev/nvme1n1 /data
```

---

## 25. Verify Mounted Storage

```bash
df -h
```
