- `chkrootkit`
- `rkhunter -c -sk`
- `sudo bash -c 'for user in $(cut -f1 -d: /etc/passwd); do entries=$(crontab -u $user -l 2>/dev/null | grep -v "^#"); if [ -n "$entries" ]; then echo "$user: Crontab entry found!"; echo "$entries"; echo; fi; done'`
- `ps -eFH`
-
# Tools
- dumpzilla