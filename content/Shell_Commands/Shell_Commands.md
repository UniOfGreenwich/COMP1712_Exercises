# Shell Commands

As said in the lecture shell commands.... 

To successfully make use of a terminal and to become competent, knowing the commonly used posix and gnu-core-utils packages are paramount. It is a tall order to learn every package, out there, for instance the nixos package manager has over 80,000 packages! 

So below is a sample of useful packages to become familar with. 

---

## 1. Navigating the File System

### 1.1 `pwd` (Print Working Directory)
**Description**: Displays the current directory.
```bash
pwd
```
**Example**:  
1. Open your terminal.
2. Type `pwd` and press Enter.
3. You will see the full path of the directory you’re currently in, like `/home/user`.

---

### 1.2 `cd` (Change Directory)
**Description**: Changes the working directory.
```bash
cd [directory]
```
**Examples**:
1. To move to the `/home` directory:
   ```bash
   cd /home
   ```
2. To go back to the previous directory:
   ```bash
   cd -
   ```

---

### 1.3 `ls` (List Directory Contents)
**Description**: Lists files and directories.
```bash
ls [options] [directory]
```
**Examples**:
1. List all files in the current directory:
   ```bash
   ls
   ```
2. List hidden files:
   ```bash
   ls -a
   ```
3. Show detailed information (file size, permissions, etc.):
   ```bash
   ls -l
   ```

---

## 2. File Operations

### 2.1 `cp` (Copy Files)
**Description**: Copies files or directories.
```bash
cp [source] [destination]
```
**Examples**:
1. Copy a file:
   ```bash
   cp file.txt /backup/file.txt
   ```
2. Copy a directory:
   ```bash
   cp -r /source/dir /backup/dir
   ```

---

### 2.2 `mv` (Move/Rename Files)
**Description**: Moves or renames files.
```bash
mv [source] [destination]
```
**Examples**:
1. Move a file:
   ```bash
   mv file.txt /backup/file.txt
   ```
2. Rename a file:
   ```bash
   mv oldname.txt newname.txt
   ```

---

### 2.3 `rm` (Remove Files)
**Description**: Deletes files or directories.
```bash
rm [options] [file/directory]
```
**Examples**:
1. Remove a file:
   ```bash
   rm file.txt
   ```
2. Remove a directory:
   ```bash
   rm -r /path/to/directory
   ```

---

## 3. File Permissions

### 3.1 `chmod` (Change File Permissions)
**Description**: Changes permissions of a file or directory.
```bash
chmod [options] [permissions] [file/directory]
```
**Examples**:
1. Make a file executable:
   ```bash
   chmod +x script.sh
   ```
2. Set specific permissions (e.g., read-write for owner, read for others):
   ```bash
   chmod 644 file.txt
   ```

---

### 3.2 `chown` (Change File Ownership)
**Description**: Changes the owner of a file or directory.
```bash
chown [owner][:group] [file/directory]
```
**Examples**:
1. Change owner:
   ```bash
   chown newuser file.txt
   ```
2. Change owner and group:
   ```bash
   chown newuser:newgroup file.txt
   ```

---

## 4. Searching and Finding Files

### 4.1 `find` (Search for Files)
**Description**: Searches for files in a directory hierarchy.
```bash
find [path] [options]
```
**Examples**:
1. Find all `.txt` files in the current directory:
   ```bash
   find . -name "*.txt"
   ```
2. Find files modified in the last 7 days:
   ```bash
   find /path -mtime -7
   ```

---

### 4.2 `grep` (Search Text in Files)
**Description**: Searches for a pattern in files.
```bash
grep [options] [pattern] [file]
```
**Examples**:
1. Search for "hello" in a file:
   ```bash
   grep "hello" file.txt
   ```
2. Search recursively in a directory:
   ```bash
   grep -r "hello" /path/to/directory
   ```

---

## 5. Disk Usage

### 5.1 `df` (Disk Free)
**Description**: Displays disk space usage.
```bash
df [options]
```
**Example**:  
1. Check disk usage in human-readable format:
   ```bash
   df -h
   ```

---

### 5.2 `du` (Disk Usage)
**Description**: Shows the size of files and directories.
```bash
du [options] [file/directory]
```
**Example**:  
1. Check the size of a directory:
   ```bash
   du -sh /path/to/directory
   ```

---

## 6. Process Management

### 6.1 `ps` (Process Status)
**Description**: Shows information about active processes.
```bash
ps [options]
```
**Example**:  
1. Show all running processes:
   ```bash
   ps aux
   ```

---

### 6.2 `kill` (Terminate Processes)
**Description**: Sends a signal to a process (usually to terminate it).
```bash
kill [options] [process_id]
```
**Example**:  
1. Kill a process with PID 1234:
   ```bash
   kill 1234
   ```

---

## 7. Networking

### 7.1 `ping` (Check Network Connectivity)
**Description**: Sends ICMP echo requests to test network connectivity.
```bash
ping [host]
```
**Example**:  
1. Ping Google to check internet connectivity:
   ```bash
   ping google.com
   ```

---

### 7.2 `ifconfig` / `ip` (Network Interface Configuration)
**Description**: Displays or configures network interfaces.
```bash
ifconfig [interface]
```
or
```bash
ip a
```
**Example**:  
1. Check the network interface configuration:
   ```bash
   ifconfig
   ```
or
   ```bash
   ip a
   ```

---

## 8. Archiving and Compression

### 8.1 `tar` (Create and Extract Archives)
**Description**: Creates or extracts archives.
```bash
tar [options] [archive] [file/directory]
```
**Examples**:
1. Create a `.tar.gz` archive:
   ```bash
   tar -czvf archive.tar.gz /path/to/directory
   ```
2. Extract a `.tar.gz` archive:
   ```bash
   tar -xzvf archive.tar.gz
   ```

---

### 8.2 `gzip` / `gunzip` (Compress/Decompress Files)
**Description**: Compresses or decompresses files using gzip.
```bash
gzip [file]
```
```bash
gunzip [file.gz]
```
**Examples**:
1. Compress a file:
   ```bash
   gzip file.txt
   ```
2. Decompress a file:
   ```bash
   gunzip file.txt.gz
   ```

---

## 9. Text Processing

### 9.1 `cat` (Concatenate and Display Files)
**Description**: Displays file contents.
```bash
cat [file]
```
**Example**:  
1. Display the contents of a file:
   ```bash
   cat file.txt
   ```

---

### 9.2 `head` / `tail` (View Beginning or End of Files)
**Description**: Displays the first or last lines of a file.
```bash
head [file]
```
```bash
tail [file]
```
**Example**:  
1. Display the first 10 lines of a file:
   ```bash
   head file.txt
   ```
2. Display the last 10 lines of a file:
   ```bash
   tail file.txt
   ```

---


## 10. Dates

1. First run the `date` command in the terminal.

   ```sh
   $ date
   ```
   **Output:** will be something like this...

   ```sh
   Mon 27 Feb 13:58:41 GMT 2023
   ```
2. So how do we get different formats?

   Well if in doubt you can check the `man` pages or use the commands `--help` flag

   ```sh
   $ date --help
   ```

3. Looking at the output workout how to produce this format:

   ```sh
   > 20230227
   ```

   <details>
   <summary>Answer</summary>

   ```sh
   date +"%Y%m%d"
   ```

   </details>


4. Now modify this output to display:

   ```sh
   > Year: 2023, Month: 02, Day: 27
   ```

   <details>
   <summary>Answer</summary>

   ```sh
   date +"Year: %Y, Month: %m, Day: %d"
   ```

   </details>

5. The most common formatting characters:
   - `%D` – Display date as mm/dd/yy
   - `%Y` – Year (e.g., 2020)
   - `%m` – Month (01-12)
   - `%B` – Long month name (e.g., November)
   - `%b` – Short month name (e.g., Nov)
   - `%d` – Day of month (e.g., 01)
   - `%j` – Day of year (001-366)
   - `%u` – Day of week (1-7)
   - `%A` – Full weekday name (e.g., Friday)
   - `%a` – Short weekday name (e.g., Fri)
   - `%H` – Hour (00-23)
   - `%I` – Hour (01-12)
   - `%M` – Minute (00-59)
   - `%S` – Second (00-60)

6. Using the above information and what previous steps reproduce the ISO 8601 standard for datetime. 

   ```sh
   > 2023-02-27T12:08:45Z
   ```

   <details>
   <summary>Answer</summary>

   ```sh
   $ date +"%Y-%m-%dT%H:%M:%S:%NZ"
   ```

   - `%Y` – Year (e.g., 2020)
   - `%m` – Month (01-12)
   - `%d` – Day of month (e.g., 01)
   - `T` – self delimeter
   - `%H` – Hour (00-23)
   - `:` – self delimeter
   - `%M` – Minute (00-59)
   - `:` – self delimeter
   - `%S` – Second (00-60)
   - `Z` – self delimeter
   </details>

7. Amend the last command so that after seconds you get nano seconds.
   
   ```sh
   > 2023-02-27T12:14:03:281999558Z
   ```

   <details>
   <summary>Answer</summary>
   
   ```sh
   $ date +"%Y-%m-%dT%H:%M:%S:%NZ"
   ```

   - `%Y` – Year (e.g., 2020)
   - `%m` – Month (01-12)
   - `%d` – Day of month (e.g., 01)
   - `T` – self delimeter
   - `%H` – Hour (00-23)
   - `:` – self delimeter
   - `%M` – Minute (00-59)
   - `:` – self delimeter
   - `%S` – Second (00-60)
   - `:` – self delimeter
   - `%N` – nanoseconds (000000000..999999999)
   - `Z` – self delimeter
   </details>

----- 

## 11 Manipulating inputs and outputs

   1. working with the previous command lets strip out the `T`,`:`s and `Z` so that we are left with only numnbers.
   
   2. Using `awk` we can manipulate the output by piping `|` the output of `date` into awk
    - first run this command
      ```sh
      $ date +"%Y-%m-%dT%H:%M:%S:%NZ" | awk "{print $1}" 
      > 2023-02-27T12:20:40:005619503Z   
      ``` 
      - `awk` with the argument `print $1` will print the first argument... ie the output of `date`
   3. Now lets remove the `T`
      ```sh
      $ date +"%Y-%m-%dT%H:%M:%S:%NZ" | awk -F 'T' '{print $1}'
      > 2023-02-27
      ```
   4. What happens when you do $2 on the same command as above?
      <details>
      <summary>Answer</summary>

      ```sh
      > 12:50:48:341942600Z
      ``` 
      This is because the input has been split and now 
      - $1 = 2023-02-27
      - $2 = 12:20:40:005619503Z

      </details>

   5. Change the delimeter `-F 'T'` to `-F ':'` and repeat both steps as before:
      <details>
      <summary>Answer</details>
      
      ```sh
      $  date +"%Y-%m-%dT%H:%M:%S:%NZ" | awk -F ':' '{print $1}'
      >  2023-02-27T12
      ```

      ```sh
      $ date +"%Y-%m-%dT%H:%M:%S:%NZ" | awk -F ':' '{print $2}'
        55
      $ date +"%Y-%m-%dT%H:%M:%S:%NZ" | awk -F ':' '{print $3}'
        32
      $ date +"%Y-%m-%dT%H:%M:%S:%NZ" | awk -F ':' '{print $4}'
        473072761Z
      ```
      </details>

   6. You can put these together using the print {$2$3$4$}, try.
     ```sh
     date +"%Y-%m-%dT%H:%M:%S:%NZ" | awk -F ':' '{print $2$3$4}'
     5719707652042Z
     ```
  7. Experiment with this and consider piping with awk to see if you can get:
 
     ```sh
     20230227130026355420256
     ```
     
     <details>
     <summary>Answer</summary>
     
     ```sh
     $ date +"%Y-%m-%dT%H:%M:%S:%NZ" | awk -F '[-T:Z]' '{print $1$2$3$4$5$6$7$8$9}'
     20230227130026355420256
     ``` 
     
     </details>