## Securing binaries
- `export PATH=/mnt/usb/bin:/mnt/usb/sbin`
- `export LD_LIBRARY_PATH=/mnt/usb/lib:/mnt/usb/lib64`
- `debsums`
	- `-e --config` config files
	- `-c --changed` only output changed files
## Forensics
- `ls -l` mtime (modify timestamp)
- `ls -lc` ctime (change timestamp) metadeta/filename/permissions
- `ls -la` atime (access timestamp)
### Find
- `find / -type f -executable 2> /dev/null`
## Good files to check
- `~/.bash_history`
- `cat /var/log/auth.log | grep useradd`
- `/etc/systemd/system`
- `/var/log/syslog`

# User config
---
## Config files
- `/etc/passwd`
	- `cat /etc/passwd | cut -d: -f1,3 | grep ':0$'`
- `/etc/group`
### Groups
- `/etc/group`
- `groups [USER]`
- `getent group adm`
- `getent group 27`
# Process snooping
---
- `lsof`
	- `-i` Network connections
	- `-P` display port numbers
	- `-n` show ips instead of resolving hostnames
	- `-p` PID
## Network
- `osqueryi`
	- `SELECT pid, fd, socket, local_address, remote_address FROM process_open_sockets WHERE pid = 267490;`

## Processes
- `ps aux`
	- `a` all users
	- `u` user oriented (user and start time)
	- `x` Include processes not attached to a terminal
- `ps -eFH`
	- `-e` select all processes
	- `-F` extra full mode
	- `-H` process hierarchy (forest)
- `pstree [PID]`
	- `-p` list PID
	- `-s` list child processes parents
- `top`
	- `-d [seconds]` refresh rate
	- `-c` display full command paths
	- `-u [user]` only show a specific user's processes
# Log Analysis
---
### `grep`
- `grep [SEARCH TERM] file.txt`
### `wc`
- -c --bytes
- -m --chars
- -l --lines (newlines)
- -w --words
# Snooping
## Shells
- `echo $SHELL`
- `cat /etc/shells`
- `chsh -s /usr/bin/zsh`
- `history`
# System stuff
---
## Systemd
- `/etc/systemd/system`
## Cron
 - `/var/spool/cron/crontabs/[username]`
- `/etc/crontab` main cron file
	- `/etc/cron*/`  Contains system cron jobs
## Other persistance
- `~/.config/autostart/`