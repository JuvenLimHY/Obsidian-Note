# nmap 

```

```

# ftp login

cred: ftp : ftp

```
┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.110]
└─$ ftp 192.168.114.110
Connected to 192.168.114.110.
220 (vsFTPd 3.0.5)
Name (192.168.114.110:kali): ftp
331 Please specify the password.
Password: 
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
229 Entering Extended Passive Mode (|||38458|)


```


change to PASSIVE mode 
cd ..
ls to see a backup file 
```
ftp> ls
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
-rw-r--r--    1 1001     1002          220 Jan 06  2022 .bash_logout
-rw-r--r--    1 1001     1002         3771 Jan 06  2022 .bashrc
-rw-r--r--    1 1001     1002          807 Jan 06  2022 .profile
dr-xr-xr-x    2 1001     1002         4096 Apr 06  2023 backup
226 Directory send OK.
ftp> pwd
Remote directory: /home/ftp

```

i have 2 users, clay and lisa 
```bash 
226 Directory send OK.
ftp> pwd
Remote directory: /home
ftp> ls -alr
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
drwxrwxrwx    4 1000     1000         4096 Apr 06  2023 lisa
drwxr-x---    3 1001     1002         4096 Apr 06  2023 ftp
drwxr-x---    2 1002     1003         4096 Jul 09  2024 clay
drwxr-xr-x   19 0        0            4096 Apr 06  2023 ..
drwxr-xr-x    5 0        0            4096 Apr 06  2023 .
226 Directory send OK.
ftp> 

```

cant cd to clay but can go into lisa

```
ftp> cd clay
550 Failed to change directory.
ftp> cd lisa
250 Directory successfully changed.
ftp> 

```


lisa got some nice stuff 

```
ftp> ls -alr
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
-rw-r--r--    1 1000     1000           33 Jun 09 02:09 local.txt
drwx------    2 1000     1000         4096 Apr 06  2023 .ssh
-rw-r--r--    1 1000     1000          807 Jan 06  2022 .profile
lrwxrwxrwx    1 0        0               9 Apr 06  2023 .mysql_history -> /dev/null
drwx------    2 1000     1000         4096 Apr 06  2023 .cache
-rw-r--r--    1 1000     1000         3771 Jan 06  2022 .bashrc
-rw-r--r--    1 1000     1000          220 Jan 06  2022 .bash_logout
lrwxrwxrwx    1 0        0               9 Apr 06  2023 .bash_history -> /dev/null
drwxr-xr-x    5 0        0            4096 Apr 06  2023 ..
drwxrwxrwx    4 1000     1000         4096 Apr 06  2023 .
226 Directory send OK.
ftp> pwd
Remote directory: /home/lisa                                                                                        
ftp>                                                                                                                
                                                       
```



```

┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.110]
└─$ ftp -v 192.168.114.110
Connected to 192.168.114.110.
220 (vsFTPd 3.0.5)
Name (192.168.114.110:kali): ftp
331 Please specify the password.
Password: 
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
229 Entering Extended Passive Mode (|||40037|)
exit
^C
receive aborted. Waiting for remote to finish abort.
ftp> passive
Passive mode: off; fallback to active mode: off.
ftp> ls
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
226 Directory send OK.
ftp> ls
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
226 Directory send OK.
ftp> ls -al
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
dr-xr-xr-x    2 1001     1002         4096 Apr 06  2023 .
drwxr-x---    3 1001     1002         4096 Apr 06  2023 ..
226 Directory send OK.
ftp> ls -al ..
output to local-file: .. [anpqy?]? 
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
ftp: Can't open `..': Is a directory
226 Directory send OK.
225 No transfer to ABOR.
ftp> cd ..
250 Directory successfully changed.
ftp> ls -al
200 EPRT command successful. Consider using EPSV.
150 Here comes the directory listing.
drwxr-x---    3 1001     1002         4096 Apr 06  2023 .
drwxr-xr-x    5 0        0            4096 Apr 06  2023 ..
-rw-r--r--    1 1001     1002          220 Jan 06  2022 .bash_logout
-rw-r--r--    1 1001     1002         3771 Jan 06  2022 .bashrc
-rw-r--r--    1 1001     1002          807 Jan 06  2022 .profile
dr-xr-xr-x    2 1001     1002         4096 Apr 06  2023 backup
226 Directory send OK.
ftp> 

```


# bashrc

```
                                                                                                                    
┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.110]
└─$ cat .bashrc 
# ~/.bashrc: executed by bash(1) for non-login shells.
# see /usr/share/doc/bash/examples/startup-files (in the package bash-doc)
# for examples

# If not running interactively, don't do anything
case $- in
    *i*) ;;
      *) return;;
esac

# don't put duplicate lines or lines starting with space in the history.
# See bash(1) for more options
HISTCONTROL=ignoreboth

# append to the history file, don't overwrite it
shopt -s histappend

# for setting history length see HISTSIZE and HISTFILESIZE in bash(1)
HISTSIZE=1000
HISTFILESIZE=2000

# check the window size after each command and, if necessary,
# update the values of LINES and COLUMNS.
shopt -s checkwinsize

# If set, the pattern "**" used in a pathname expansion context will
# match all files and zero or more directories and subdirectories.
#shopt -s globstar

# make less more friendly for non-text input files, see lesspipe(1)
[ -x /usr/bin/lesspipe ] && eval "$(SHELL=/bin/sh lesspipe)"

# set variable identifying the chroot you work in (used in the prompt below)
if [ -z "${debian_chroot:-}" ] && [ -r /etc/debian_chroot ]; then
    debian_chroot=$(cat /etc/debian_chroot)
fi

# set a fancy prompt (non-color, unless we know we "want" color)
case "$TERM" in
    xterm-color|*-256color) color_prompt=yes;;
esac

# uncomment for a colored prompt, if the terminal has the capability; turned
# off by default to not distract the user: the focus in a terminal window
# should be on the output of commands, not on the prompt
#force_color_prompt=yes

if [ -n "$force_color_prompt" ]; then
    if [ -x /usr/bin/tput ] && tput setaf 1 >&/dev/null; then
        # We have color support; assume it's compliant with Ecma-48
        # (ISO/IEC-6429). (Lack of such support is extremely rare, and such
        # a case would tend to support setf rather than setaf.)
        color_prompt=yes
    else
        color_prompt=
    fi
fi

if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
fi
unset color_prompt force_color_prompt

# If this is an xterm set the title to user@host:dir
case "$TERM" in
xterm*|rxvt*)
    PS1="\[\e]0;${debian_chroot:+($debian_chroot)}\u@\h: \w\a\]$PS1"
    ;;
*)
    ;;
esac

# enable color support of ls and also add handy aliases
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    #alias dir='dir --color=auto'
    #alias vdir='vdir --color=auto'

    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi

# colored GCC warnings and errors
#export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01'

# some more ls aliases
alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'

# Add an "alert" alias for long running commands.  Use like so:
#   sleep 10; alert
alias alert='notify-send --urgency=low -i "$([ $? = 0 ] && echo terminal || echo error)" "$(history|tail -n1|sed -e '\''s/^\s*[0-9]\+\s*//;s/[;&|]\s*alert$//'\'')"'

# Alias definitions.
# You may want to put all your additions into a separate file like
# ~/.bash_aliases, instead of adding them here directly.
# See /usr/share/doc/bash-doc/examples in the bash-doc package.

if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi

# enable programmable completion features (you don't need to enable
# this, if it's already enabled in /etc/bash.bashrc and /etc/profile
# sources /etc/bash.bashrc).
if ! shopt -oq posix; then
  if [ -f /usr/share/bash-completion/bash_completion ]; then
    . /usr/share/bash-completion/bash_completion
  elif [ -f /etc/bash_completion ]; then
    . /etc/bash_completion
  fi
fi
                                                      
```

# .profile 

```
┌──(kali㉿kali)-[~/OSCP/Exam/192.168.114.110]
└─$ cat .profile 
# ~/.profile: executed by the command interpreter for login shells.
# This file is not read by bash(1), if ~/.bash_profile or ~/.bash_login
# exists.
# see /usr/share/doc/bash/examples/startup-files for examples.
# the files are located in the bash-doc package.

# the default umask is set in /etc/profile; for setting the umask
# for ssh logins, install and configure the libpam-umask package.
#umask 022

# if running bash
if [ -n "$BASH_VERSION" ]; then
    # include .bashrc if it exists
    if [ -f "$HOME/.bashrc" ]; then
        . "$HOME/.bashrc"
    fi
fi

# set PATH so it includes user's private bin if it exists
if [ -d "$HOME/bin" ] ; then
    PATH="$HOME/bin:$PATH"
fi

# set PATH so it includes user's private bin if it exists
if [ -d "$HOME/.local/bin" ] ; then
    PATH="$HOME/.local/bin:$PATH"
fi

```
# screenshots

![[{52191968-40D0-4ACD-920D-B56216F507C2}.png]]

![[{BA410FE9-89BF-48F9-B0F2-05FB6BAEC50E}.png]]

