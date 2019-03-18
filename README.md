# Linux command (CentOS)
### Grep recursively subfolders and count number of lines matched
grep -r -c regex *

### Read a big size log file.
1. Use grep  
Display 100 lines before and after the matched regex.
```
zgrep -A100 -B100 2029879 catalina.out.190206*
```

2. Use grep and awk command (any part of a big file)
```
grep -n regex catalina.out
835239:2019-02-13 16:27:54 (for example)
awk 'FNR>=minLine && FNR<=maxLine' catalina.out
```
3. Use tail command (only the last part of a big file)
```
tail -f -n10000 fileName
```
### Find file name in a zip file.
```
tar tf 20180615.tar.gz | grep JIDU6T
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
### Print out disk usage (human-readable)
```
df -h
```
### Unzip tar.gz file
```
tar -zxvf filename.tar.gz
```

### See content of tar.gz file
```
tar -tf filename.tar.gz
```

### Grep inside tar.gz file
```
tar -O -xvf filename.tar.gz | grep keyword
```
