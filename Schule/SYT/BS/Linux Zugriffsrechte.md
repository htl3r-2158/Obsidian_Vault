#Linux 
#Linux-Zugriffsrechte= #Schutzcode s = #Permission

## Unix Zugriffsrechte (Permissions)
* Standard for all  UNIX-Systems (i.e. also for Linux)
* File is owned by one user and one associated group
* displayed in compact 10-character notation
* ls -l
```bash
laurin@LaurinsStudio:~$ ls -l
total 28
-rw-r--r-- 1 laurin laurin   31 Feb 26 17:35 Datei31
lrwxrwxrwx 1 laurin laurin   27 Feb 26 17:12 Link_Laurin -> UebungsVerzeichnis24_Laurin
drwxr-xr-x 4 laurin laurin 4096 Feb 26 17:01 UebungsVerzeichnis24_Laurin
drwx------ 3 laurin laurin 4096 Jan 18 16:38 snap
-rw------- 1 laurin laurin 2610 Mar  6 13:20 ue12
-rw-r--r-- 1 laurin laurin  574 Mar  6 13:20 ue12.pub
-rw-r--r-- 1 laurin laurin 1110 Apr 17 15:24 user-anlegen.sh
-rw-rw-r-- 1 laurin laurin  218 Apr 17 15:41 user-entfernen.sh
```
### Permission Exambles (regular files)

| Permissions  | Explaination                                             |
| ------------ | -------------------------------------------------------- |
| `-rwx------` | Read/write/execute for owner, No access to everyone else |
| `-rw-r--r--` | Read/write for owner, read access to everyone else       |
| `-rw-r-----` | Read/write for owner, read access to the group           |
| `-r--r--r--` | Read for everyone                                        |
| `-rwxrwxrwx` | Full access for everyone                                 |
| `-------rw-` | Read/write for everyone except the owner and the group   |

## Unix Permissions for Directories
* Permissions bits interpreted differently for directory:
	* #Read : listing names of files in directories
	* #Write : creating, renaming and deleting files within this directory
	* #Execute: entering, use within a path-name, proberties of files in the directory
### Permission Exambles (regular directories)
| Permissions  | Eplanations                                                             |
| ------------ | ----------------------------------------------------------------------- |
| `drwxr-xr-x` | Owner has full access, the group and everyone else can read and execute |
| `drwxrwx---` | Only owner and group can do everything                                  |
| `drwxrwxrwx` | Every right to everyone                                                 |
| `drwxrwx--x` | Owner and group can do everything and everyone else can execute         |
## Commands
```bash
chmod [ugoa] [+-=] [rwxst] fil

```

