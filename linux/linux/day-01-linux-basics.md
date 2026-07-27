# Linux Basics - Day 1

## What is an Operating System?

An operating system is system software that acts as a mediator between the user and the computer hardware.

It helps users communicate with the computer and manages system resources like CPU, memory, files, and devices.

## What is Linux?

Linux is a free and open-source operating system.

It is widely used in servers, cloud platforms, DevOps environments, containers, and enterprise systems.

## Key Points

- Linux is free and open source.
- Linux supports multiple users.
- Linux is highly secure.
- Linux is command-line based.
- Linux is community-driven.
- Linux is widely used for server and business management.

## Linux Architecture

Linux works in layers.

```text
+--------------------------------------------------+
|             Applications and Utilities           |
|   Examples: ls, pwd, man, cal, editors, tools    |
+--------------------------------------------------+
|                      Shell                       |
|   Takes commands from the user and sends them    |
|   to the kernel                                  |
+--------------------------------------------------+
|                     Kernel                       |
|   Core of Linux OS                               |
|   Manages memory, processes, files, devices      |
+--------------------------------------------------+
|                    Hardware                      |
|   CPU, RAM, Disk, Keyboard, Monitor, Network     |
+--------------------------------------------------+
```

## Shell

The shell is the outer layer of Linux.

It works as an interface between the user and the kernel.

### Shell Responsibilities

- Read user commands
- Check command syntax
- Validate the command
- Convert it into kernel-understandable form
- Pass it to the kernel

## Kernel

The kernel is the core component of Linux.

It is responsible for executing commands and interacting with hardware and system components.

### Kernel Responsibilities

- Process management
- Memory management
- Device management
- File system handling
- Command execution

## How a Linux Command Works

```text
User
  |
  v
Terminal
  |
  v
Shell
  |
  |  checks command syntax
  |  validates the command
  v
Kernel
  |
  |  performs the required action
  v
Output appears on Terminal
  |
  v
Prompt returns for next command
```

## Shell vs Kernel

```text
+---------------------------+----------------------------+
| Shell                     | Kernel                     |
+---------------------------+----------------------------+
| Outer layer               | Core of Linux              |
| Reads user commands       | Executes commands          |
| Checks syntax             | Manages hardware/resources |
| Acts as interface         | Acts as controller         |
| Sends command to kernel   | Returns result to shell     |
+---------------------------+----------------------------+
```

## Root User and Normal User

```text
Normal User
    |
    | limited permissions
    v
sudo / su
    |
    | elevated privileges
    v
Root User
```

## Command Cheat Sheet

### 1. `date`

Shows current date and time.

#### Syntax
```bash
date
date "+<format>"
```

#### Examples
```bash
date
date "+%d"
date "+%m"
date "+%y"
date "+%d/%m/%y"
date "+%a"
date "+%b"
date "+%B"
date "+%A"
```

#### Common format options
```bash
%d  Day of month
%m  Month number
%y  Two-digit year
%a  Short weekday name
%A  Full weekday name
%b  Short month name
%B  Full month name
```

#### Example output
```bash
$ date
Mon Jul 27 11:27:14 UTC 2026

$ date "+%d"
27

$ date "+%m"
07

$ date "+%y"
26

$ date "+%d/%m/%y"
27/07/26

$ date "+%a"
Mon

$ date "+%b"
Jul

$ date "+%B"
July

$ date "+%A"
Monday
```

### 2. `pwd`

Shows the present working directory.

#### Syntax
```bash
pwd
```

#### Example
```bash
$ pwd
/home/user
```

### 3. `whoami`

Shows the current logged-in user.

#### Syntax
```bash
whoami
```

#### Example
```bash
$ whoami
user
```

### 4. `cal`

Displays a calendar.

#### Syntax
```bash
cal
cal -3
cal -y
cal <month> <year>
cal <year>
```

#### Examples
```bash
cal
cal -3
cal -y
cal 7 2026
cal 2026
```

#### Common options
```bash
-3   Show previous, current, and next month
-y   Show full year calendar
```

#### Example output
```bash
$ cal
     July 2026
Su Mo Tu We Th Fr Sa
          1  2  3  4
 5  6  7  8  9 10 11
12 13 14 15 16 17 18
19 20 21 22 23 24 25
26 27 28 29 30 31
```

```bash
$ cal -3
     June 2026             July 2026            August 2026
Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa
    1  2  3  4  5  6            1  2  3  4                     1
 7  8  9 10 11 12 13   5  6  7  8  9 10 11   2  3  4  5  6  7  8
14 15 16 17 18 19 20  12 13 14 15 16 17 18   9 10 11 12 13 14 15
21 22 23 24 25 26 27  19 20 21 22 23 24 25  16 17 18 19 20 21 22
28 29 30              26 27 28 29 30 31     23 24 25 26 27 28 29
                                            30 31
```

```bash
$ cal -y
2026
... full year output ...
```

### 5. `man`

Shows the manual page of a command.

#### Syntax
```bash
man <command>
```

#### Example
```bash
man ls
```

### 6. `sudo`

Runs a command with superuser privileges.

#### Syntax
```bash
sudo <command>
```

#### Examples
```bash
sudo yum install tree
sudo yum update tree
sudo yum remove tree
```

### 7. `su`

Switches user.

#### Syntax
```bash
su
su - <username>
```

#### Examples
```bash
su
su - root
```

### 8. `yum`

Package manager used on RPM-based systems.

#### Syntax
```bash
sudo yum install <package-name>
sudo yum update <package-name>
sudo yum remove <package-name>
sudo yum search <package-name>
sudo yum list installed
```

#### Example
```bash
sudo yum install tree
```

### 9. `rpm`

Used for RPM package operations.

#### Syntax
```bash
rpm -ivh <package-file.rpm>
rpm -qa
rpm -q <package-name>
rpm -e <package-name>
```

#### Examples
```bash
rpm -ivh httpd.rpm
rpm -qa
rpm -q httpd
rpm -e httpd
```

## Quick Flow Reminder

```text
User types command
    |
    v
Shell checks command
    |
    v
Kernel executes command
    |
    v
Result shown in terminal
```

## Key Takeaways

- Linux is a free and open-source OS.
- The shell is the interface between user and kernel.
- The kernel is the core of Linux.
- Commands are case-sensitive.
- `sudo` is used for admin privileges.
- `su` is used to switch users.
- `pwd`, `date`, `cal`, `whoami`, and `man` are basic Linux commands.
- `yum` and `rpm` help manage packages.
