## 🔐 Permissions

### `ls -l`

##### - List files with permissions, owner and group

Output:
- File type
- Permissions (owner, group, others)
- Owner and group
- File name

Examples:
```sh
ls -l
```

Output example:
```sh
-rwxr-xr--  davi  developers  script.sh
```

Notes:
- First character → file type (`-`, `d`, `l`)
- Next 9 characters → permissions
***
## Permission Types

##### - Read, Write and Execute

| Symbol | Name | File | Directory |
|------|------|------|-----------|
| r | read | read file | list contents |
| w | write | modify file | create/delete files |
| x | execute | run file | enter directory (`cd`) |

⚠️ Directories require `x` to be accessed, even if files inside have `r`.
***
## Permission Groups

##### - Who the permissions apply to

| Symbol | Meaning |
|------|--------|
| u | user (owner) |
| g | group |
| o | others |
| a | all |

Permissions are always evaluated in this order:
- owner → group → others

***
## ✏️ `chmod`

##### - Change file or directory permissions

Modes:
- Symbolic
- Numeric (octal)
### `chmod (symbolic mode)`

##### - Add or remove permissions using letters

Operators:
- `+` → add
- `-` → remove
- `=` → set exactly

Examples:
```sh
chmod u+x script.sh
chmod g-w file.txt
chmod o+r file.txt
chmod a+r file.txt
```

Notes:
- Good for small adjustments
- Less common in automation
***
### `chmod (numeric mode)`

##### - Set permissions using numbers

Values:
- r = 4
- w = 2
- x = 1

| Number | Permission |
| ------ | ---------- |
| 7      | rwx        |
| 6      | rw-        |
| 5      | r-x        |
| 4      | r--        |
| 3      | -wx        |
| 2      | -w-        |
| 1      | --x        |
| 0      | ---        |

Examples:
```sh
chmod 755 script.sh
chmod 644 file.txt
```

Meaning (`755`):
- owner → rwx
- group → r-x
- others → r-x
***
## 👑 `chown`

##### - Change file owner and group

Notes:
- `chown` = change owner
- Controls who owns the file
- Usually requires `sudo`
##### - Assign a new owner to a file

Examples:
```sh
chown user file.txt
sudo chown root file.txt
```

Notes:
- Only root can change ownership
##### - Assign owner and group at the same time

Examples:
```sh
chown user:group file.txt
sudo chown www-data:www-data index.html
```

Common in web servers.
##### - Keep owner, change group

Examples:
```sh
chown :developers project/
```
***
##### - Apply ownership to directories and contents

Parameters:
- `-R` → recursive

Examples:
```sh
sudo chown -R user:group folder/
sudo chown -R davi:developers project/
```

⚠️ Use `-R` carefully — affects everything inside.
***
## ⚠️ Common Errors

##### - Permission and ownership mistakes

Examples:
```sh
Permission denied
Operation not permitted
```

Causes:
- Missing `x` permission on directory
- Wrong owner or group
- Trying `chown` without `sudo`

Fix example:
```sh
sudo chown -R $USER:$USER folder/
```
***
## 🧠 Key Rules

##### - Important concepts to remember

- chmod → controls what can be done
- chown → controls who can do it
- Directories need `x` to be accessed
- Only root can change ownership
