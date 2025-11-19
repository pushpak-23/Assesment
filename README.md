# Linux-Style Command Utilities in Python

This repository contains two lightweight command-line tools implemented in Python:

| Script    | Purpose                                                          |
|-----------|------------------------------------------------------------------|
| `mini-df` | Shows filesystem disk usage similar to the Linux `df` command    |
| `mini-ls` | Lists files and directories similar to the Linux `ls -l` command |

Both scripts work without external dependencies and run on any Linux system with Python 3.

---

## 📁 1. mini-df — Disk Space Viewer

`` `mini-df` is a simple alternative to the `df` command. It reads mounted filesystems from `/proc/self/mounts` and prints total and free space.

```bash
# Make executable
chmod +x mini-df mini-ls

# Use instantly
./mini-df -h
./mini-ls -r .
```

### 🔹 Usage
```bash
 ./mini-df
Filesystem                  Total         Free Mounted on
none                   4119871488   4119871488 /usr/lib/modules/5.15.153.1-microsoft-standard-WSL2
none                   4119871488   4119867392 /mnt/wsl
/dev/sdc             1081101176832 1068346138624 /
```
it will give output in Byte's

Human-readable outputhttps://app.codingrooms.com/w/4Mtidd0JN8mG
```bash
./mini-df -h
Filesystem                  Total         Free Mounted on
none                         3.8G         3.8G /usr/lib/modules/5.15.153.1-microsoft-standard-WSL2
none                         3.8G         3.8G /mnt/wsl
/dev/sdc                  1006.9G       995.0G /
```

```bash
./mini-ls -r
-rwxr-xr-x  sentinel Nov 19 17:34 mini-df
-rwxr-xr-x  sentinel Nov 19 17:36 mini-ls


./mini-ls mini-df
-rwxr-xr-x  sentinel Nov 19 17:34 mini-df
```
