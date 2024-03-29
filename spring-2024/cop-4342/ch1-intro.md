# Chapter 1 - Introduction

## Help In the Unix World
- "**man**" program has been the primary means for local documentation
    - "**man man**": find out more
    - "**man -k KEYWORD**": search for a keyword in man pages
- In most Unix/Linux distros, the man pages are generally directories
- "**info**" program is useful, but it's nice be skillful with Emacs alongside it

## Linux
- Been around for 30 years
- The leading platform for operating system development
- Mint is apparently the most popular distro, but it's arguable that Ubuntu is

## Unix In Depth
- Can view operating system presentation in layers
    - The kernel is both virtual and physical 
    - System calls, which allows us to access and modify resources
- More layers:
    - Libraries, which provide more digestible access to system calls
    - Processes, which take advantage of libraries

## Working with These Layers
- How do we create and manipulate these various layers?
    - Processes:
        - fork(2), exec(2), wait(2), exit(2); clone(2)
    - Filesystems:
        - mount(2), getdents(2), stat(2), statfs(2)
    - I/O
        - open(2), read(2), write(2), close(2)
        - socket(2) et all

## Definitions
| Word | Definition |
|------|------------|
| executable | a file that can be execute an existing process |
| static executable | standalone program that does not need any other runtime support |
| dynamically linked executable | dynamically loads shared libraries; requires the service of a runtime linked |
| script | an executable which requires a seperate interpreter |
| process | the activation of a program |
| daemon | a process that generally provides a service of some sort; either self persistent or a child of a persistent process |
| user shell | provides an environment that accepts keyboard input and provides output to execute programs |
| built-in | command in a shell that does not cause the execution of a new process |
| alias | string that is expected to be expanded into another command | 
| variable | a way to reference a state in a shell |
| flag | a method to specify options in a command line |

## Filtering
- A "**filter**" should be read from stdin and should write to stdout
    - Any should should be written to stderr
- Filters should not read configuration files
- Should take their options from command line indicators like **flags**
- Output of one filter should be easily readable by another filter

## Unix File Characteristics
- Files normally follow the paradigm of a "byte-system"
- Filenames may consist of most Unicode UTF-8 characters except:
    - NUL
    - "/"
- Filenames are case sensitive by default
- Filenames with a period are generally not displayed (an example would be .git)

## Filename Action
- "**Globbing**" is a wildcard system for matching file and directory names
- An asterisk "*" can match any number of characters in path name
- A question mark "?" matches and single character
- Square brackets "[]" lets you specify a character class

## Filesystems
- Directories are tree-structures, and begin with an "/"
- "**cwd**" is the current working directory

## Filesystem Paths
- Use **/** to distinguish elements in a path
- Absolute paths begin with **/**
- Relative paths begin with any other character

## More on Paths
| Character | Definition |
|-----------|------------|
|.          |Points at the current directory.|
|..         |Points at the parent directory.|
|~/         |Referring to home directory of the current user |
|~username/ |Home directory of "username" |

## Shortcutting Path Information
- It's tedious to type full path names
- To alleviate:
    - Specify environment variable "PATH"

## Listing Files
| Options | Output |
|---------|--------|
| -l      | Shows a detailed listing, using one line per file |
|-a       | Includes the dot files |
| “/bin/ls -d DIRNAME” | Shows information about the directory rather than its contents |

## File Permissions and User Classes

### File Permissions
| Character | Permission |
|-----------|------------|
|r          |Read|
|w          |Write|
|x          |Execute|

### User Classes
| Class     | Description |
|-----------|-------------|
| owner     | User Identifier |
| group     | Group Identifier |
| other     | All users who are not the owner or in the same group |

## Changing Permissions with "chmod"
- **chmod** accepts octal notation
    - chmod 755 /bin/ls
- also accepts symbolic notation
    - chmod og+w /etc/hosts

## Unlinking and Removing Files and Directories
- Single file can have many links in a given filesystem
- Process can use system call **unlink(2)** to remove a file, but not a directory
- Process can use system call **rmdir(2)** to remove any empty directory

### Command Table
| Command | Function |
|---------|----------|
| rm      | Removes a file |
| rmdir   | Removes an **empty** directory |
| rm -r   | Recursively remove directories |
| rm - i  | Queries the user whether or not to remove a link |
| rm -f   | Don't complain about non-existent items |


