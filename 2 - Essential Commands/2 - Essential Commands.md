## 📁 Navigation

### `pwd`

##### - Print current working directory

Output:
- Absolute path of the current directory

Examples:
```sh
pwd
```
***
### `ls`

##### - List directory contents

Parameters:
- `-l` → long listing (permissions, owner, size, date)
- `-a` → include hidden files (`.`)
- `-h` → human-readable sizes (KB, MB, GB)
- `-lah` → common combination (`-l -a -h`)

Examples:
```sh
ls
ls -l
ls -a
ls -lh
ls -lah
```
***
### `cd`

##### - Change current directory

Usage:
- `/etc` → absolute path
- `..` → parent directory
- `~` → user home directory
- `-` → previous directory

Examples:
```sh
cd /etc
cd ..
cd ~
cd -
```
***
## 📄 Files and Directories

### `touch`

##### - Create empty files

Notes:
- Creates an empty file
- If the file exists, updates the timestamp

Examples:
```sh
touch file.txt
```
***
### `mkdir`

##### - Create directories

Parameters:
- `-p` → create parent directories if needed

Examples:
```sh
mkdir folder
mkdir -p project/src/main
```
***
### `cp`

##### - Copy files and directories

Parameters:
- `-r` → recursive (required for directories)

Examples:
```sh
cp file.txt copy.txt
cp -r folder/ backup/
```
***
### `mv`

##### - Move or rename files

Notes:
- Same command for moving and renaming
- Works for files and directories without flags

Examples:
```sh
mv file.txt newname.txt
mv file.txt folder/
```
***
### `rm`

##### - Remove files and directories

Parameters:
- `-r` → recursive removal
- `-f` → force removal (no confirmation)

⚠️ No trash in terminal — deletion is permanent.

Examples:
```sh
rm file.txt
rm -r folder/
rm -rf folder/
```
***
## 👀 File Visualization

### `cat`

##### - Display entire file content

Notes:
- Prints the whole file
- Not recommended for large files

Examples:
```sh
cat file.txt
```
***
### `less`

##### - Paginated file viewer

Controls:
- `q` → quit
- `/text` → search
- `n` → next match

Examples:
```sh
less file.txt
```
***
### `head`

##### - Display first lines of a file

Parameters:
- `-n X` → number of lines

Examples:
```sh
head file.txt
head -n 20 file.txt
```
***
### `tail`

##### - Display last lines or follow file changes

Parameters:
- `-f` → follow file in real time (logs)
- `-n X` → last X lines

Examples:
```sh
tail file.txt
tail -f log.txt
```
***
## 🔍 Search

### `find`

##### - Search files in directories

Parameters:
- `.` → current directory
- `-name` → file name
- `-type f` → regular files
- `-type d` → directories

Examples:
```sh
find . -name file.txt
find /var -type f -name "*.log"
```
***
### `grep`

##### - Search text inside files

Parameters:
- `-i` → ignore case
- `-r` → recursive search

Examples:
```sh
grep "error" file.txt
grep -i "error" log.txt
grep -r "password" /etc
```
***
## 🔗 Pipes and Redirection

### `|`

##### - Pipe command output to another command

Notes:
- Output of the left command becomes input of the right command

Examples:
```sh
ls -l | grep ".txt"
```
***
### `>`

##### - Redirect output to a file (overwrite)

Notes:
- Overwrites the file if it exists

Examples:
```sh
echo "hello" > file.txt
```
***
### `>>`

##### - Redirect output to a file (append)

Notes:
- Appends content to the end of the file

Examples:
```sh
echo "new line" >> file.txt
```
***
### `2>`

##### - Redirect error output

Notes:
- Redirects only error output (stderr)

Examples:
```sh
command 2> error.log
```
***
## 🧠 Help

### `man`

##### - Command manual pages

Notes:
- Full command documentation
- Use `/` to search inside the manual

Examples:
```sh
man ls
```
***
### `--help`

##### - Show command help

Notes:
- Quick summary of command options

Examples:
```sh
ls --help
```
***
