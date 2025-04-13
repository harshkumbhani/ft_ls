# ft_ls
Recoding ls terminal command in C

# Usage

ft_ls [OPTION]... [FILE]...

OPTION:
-R, --recursive
      list subdirectories recursively

-l     use a long listing format

#NOTE:
for -l it shows where the link is pointing to
without it just shows the file itself

-a, --all
      do not ignore entries starting with .

-r, --reverse
      reverse order while sorting

-t     sort by time, newest first; see --time
       sorts according to last updated

## sorting
regular alphabet
lower before upper case
files before folder

## General instructions
- needs to be in C
- exe -> ft_ls
- Makefile
- libft with extra Makefile
- error handling with graceful exit codes
- no memory leaks

### allowed functions
- write
- opendir -> returns pointer to DIR stream
- readdir -> use in loop for reading directory entries in DIR
- closedir -> needed for clean up the DIR stream
- stat ->
- lstat
- getpwuid -> get username for -l option
- getgrgid -> get groupname for -l option
- listxattr
- getxattr
- time -> returns a time_t since epoch whatever (not needed?)
- ctime -> use for -l function to get day/month (year + 1900)
- readlink -> gets the pathname of the file the link is pointing to
- malloc
- free
- perror
- strerror
- exit

# bonus ufgd
-u -> with -lt: sort by, and show, access time; with -l: show access time and
sort by name; otherwise: sort by access time, newest first
-f -> same as -a -U (no idea on where to sort)
-g -> do not list owner
-d -> only lists the chosen directory

# Needs
- Parser
- Formatter
- Writer

## Parser
- parse command line arguments

## Formatter
- depends on which options are present
- no colors

## Writer
- output to stdout
