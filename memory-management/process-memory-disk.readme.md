# Process Management in Linux

## Introduction

Process management in Linux involves monitoring, scheduling, and controlling running programs (processes). The Linux kernel assigns each process a unique **Process ID (PID)** and provides commands to:

* View running processes
* Stop, resume, or terminate processes
* Change process priority

In this section, we will **focus only on three core segments**:

1. Viewing processes
2. Killing / stopping / resuming processes
3. Prioritizing and deprioritizing processes

---

## 1. Viewing Processes

### View all running processes

```bash
ps aux
```

### View processes of a specific user

```bash
ps -u username
```

### View process by name

```bash
ps -C processname
```

### Interactive process viewer

```bash
top
```

>  `top` provides real-time CPU and memory usage.

### User-friendly interactive viewer (optional)

```bash
htop
```

> Requires installation.

---

## 2️. Managing Processes (Kill / Stop / Resume)

### Kill a process using PID

```bash
kill PID
```

### Kill a process using name

```bash
pkill processname
```

### Force kill a process

```bash
kill -9 PID
```

### Force kill all instances of a process

```bash
pkill -9 processname
```

### Stop a running process

```bash
kill -STOP PID
```

### Resume a stopped process

```bash
kill -CONT PID
```

### List background jobs

```bash
jobs
```

---

## 3️. Prioritizing & Deprioritizing Processes

Linux allows you to control how much CPU time a process gets using **priority (nice value)**.

* Priority range: **-20 (highest)** to **19 (lowest)**

### Start a process with priority

```bash
nice -n 10 command
```

### Change priority of a running process

```bash
renice 5 -p PID
```

---

# Linux System Monitoring

## CPU & Memory Monitoring

```bash
top
```

```bash
htop
```

```bash
vmstat
```

```bash
free -m
```

---

## Disk Monitoring

### Check disk space usage

```bash
df -h
```

### Check directory size

```bash
du -sh /path
```

```bash
iostat
```

---

# Disk & Storage Management in Linux

## Introduction

Disk management in Linux includes partitioning disks, creating filesystems, mounting them, and monitoring usage. Linux provides flexible tools for efficient storage management.

---

## Viewing Disk Information

### List all block devices

```bash
lsblk
```

### View partition details

```bash
fdisk -l
```

### Show UUIDs of devices

```bash
blkid
```

### Check available disk space

```bash
df -h
```

### Check size of a directory

```bash
du -sh /var/log
```

---

## Partition Management

### Create or manage partitions

```bash
fdisk /dev/sdX
```

> Be careful while working with disks — wrong commands can lead to data loss.

---

✅ This README is designed for **quick revision and hands-on practice**.
