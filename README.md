# Linux command (CentOS)
### Method to read big size log file.
```
grep -n regex catalina.out
835239:2019-02-13 16:27:54 (for example)
awk 'FNR>=minLine && FNR<=maxLine' catalina.out
```

### List out files with file zize human-readable
```
ls -lh
```

## List out all processes
```
ps auxw
```

### List out all ports
```
netstat -anp
```

### Kill process
```
kill pid
```
### Print content of text (tar.gz) to terminal
```
zcat filename
```

### Find a file (recursive sub directories)
```
syntax:  find path -name filename_pattern
example: find . -name "*filename*"
```

### Search text in tar.gz files
```
syntax:  zgrep regex_pattern filename_pattern
example: zgrep "2019-01-01 " "*filename*"
```
### Copy file from ssh
```
sftp username@servername
get filename
```
