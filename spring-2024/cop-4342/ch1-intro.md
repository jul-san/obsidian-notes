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
| process | the activation of a program; 
