# Simple Shell :V

# Description

Shell is a computer program which exposes an operating system's services to a human user or other program. This repository contains a small version of a Shell.

## Usage

You need to compile all the c files:

```bash
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
./hsh
```
hsh can work in interactive mode:

```c
$ ./hsh
>:s ls
README.md
```

##  Execution

To invoke the simple_shell, you need to write the next command:

```c
./hsh
>:s

```
After you run this command you will see the prompt: >:v. After that propmt you can put the command (extern or builtin), example:

```c
./hsh
>:s ls
README.md
>:s
```
## Command Execution

## Exit status

hsh returns Zero for success and differnt Zero for failure

## Signals

hsh ignores the Ctrl + C input, you can use Ctrl + d to exit the program.

```c
./hsh
>:s ^C
>:s ^C
>:s ^C
>:s
```
## $?

? is relplaced with return value of the las program executed

Example:

```c
>:s echo $?
>:s 0
```

## $$

In this case the second $ is replaced by the current process ID

Example:

```c
>:s echo $$
>:s 6494
```

## $$

hsh ignores all words and characters preceeded by a # character on a line

```c
>:s echo $$
>:s 13245
```
## operators

hsh can handle ; Command separator. Commands that are separeted with ; are executed sequentially.

```c
>:s echo "hello" ; echo "world"
"hello"
"world"
```
You can use ; separator with spaces or tabs or nothing between the command and the separator.

## cd

- Use cd to change current directory, if no argument is given, the command is interpeted as a cd $HOME.
- if the argument - is  given, the command is interpreted as cd $OLDPATH

Example

```c
>:s ls
README.md
>:s cd
>:s ls
simple_shell printf
>:s
```
## exit

use exit to go out of the program.

## env

Unsage: env
prints the current environment

example:

```c
>:s env
NVM_DIR=/home/...
...
```

## setenv

Usage setenv [VARIABLE][VALUE]
Create a new environment variable or modifies an existing one

## unsetenv

Usage unsetenv [VARIABLE][VALUE]
Create a new environment variable or modifies an existing one

example:

```c
>:s unsetenv PATH
>:s echo PATH

>:s
```
# AUTHORS

- Biniyam Getachew
- Kidus Efrem
