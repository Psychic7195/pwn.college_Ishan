# Learning From Documentation
In this challenge we learn how to red documentation and use commands accordingly.

## My Solve
**Flag:** pwn.college{cGmMdo1DjJirVzN4DOQyoUT_AIo.QX0ITO0wSOzEzNzEzW}

```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{cGmMdo1DjJirVzN4DOQyoUT_AIo.QX0ITO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use instructions in given documentation to use the appropriate commands.

## References 
None.


# Learning Complex usage
In this challenge we learn how to use complex commands to access files which are unaccessible otherwise.

## My Solve
**Flag:** pwn.college{U-IoUwsoJRddnGZ2nn7HS34mFI2.QX1ITO0wSOzEzNzEzW}

```
hacker@man~learning-complex-usage:~$ cd /
hacker@man~learning-complex-usage:/$ ls
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@man~learning-complex-usage:/$ /challenge/challenge --printfile /root/flag
Correct argument! Here is the /root/flag file:
cat: /root/flag: No such file or directory
hacker@man~learning-complex-usage:/$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{U-IoUwsoJRddnGZ2nn7HS34mFI2.QX1ITO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use complex commands and access files with it.

## References
None.


# Reading Manuals 
In this challenge, we read manuals provided within the system to execute certain commands.

## My Solve 
**Flag:** pwn.college{EcT_tAfmz0d18a3LjV3276SKOWk.QX0EDO0wSOzEzNzEzW

```
hacker@man~reading-manuals:~$ man yes
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --ctfmzd 018
Correct usage! Your flag: pwn.college{EcT_tAfmz0d18a3LjV3276SKOWk.QX0EDO0wSOzEzNzEzW}
```

## What I learned
I learned how to read manuals and access commands from them.

## References
None.


# Searching Manuals
In this challenge, we learn how to scroll through manuals and search them for commands and information.

## My Solve
**Flag:** pwn.college{Yb4OWXWWrhXWJYUshxPxN9sT1LJ.QX1EDO0wSOzEzNzEzW

```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --kckxgjb
Initializing...
Correct usage! Your flag: pwn.college{Yb4OWXWWrhXWJYUshxPxN9sT1LJ.QX1EDO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to scroll through and access certain commands hidden in manuals to execute.

## References
None

# Helpful Programs
In this challenge we learn how to use --help arguments to get more information.

## My Solve
**Flag:** pwn.college{QrzwNuWNJEMJxchnFmEqVZF__BN.QX3IDO0wSOzEzNzEzW}
```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 301
hacker@man~helpful-programs:~$ /challenge/challenge -g 301
Correct usage! Your flag: pwn.college{QrzwNuWNJEMJxchnFmEqVZF__BN.QX3IDO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use --help commands to get more information about a particular file or command

## References
None.


# Help For Builtins
In this challenge we find out how to use the help command to assess built in functions.

## My Solve
**Flag:** pwn.college{ICLHZRI5IekthAhRqvX-ROoosJU.QX0ETO0wSOzEzNzEzW}

```
hacker@man~help-for-builtins:~$ help 
GNU bash, version 5.2.37(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.

A star (*) next to a name means that the command is disabled.

 job_spec [&]                                                            history [-c] [-d offset] [n] or history -anrw [filename] or history >
 (( expression ))                                                        if COMMANDS; then COMMANDS; [ elif COMMANDS; then COMMANDS; ]... [ e>
 . filename [arguments]                                                  jobs [-lnprs] [jobspec ...] or jobs -x command [args]
 :                                                                       kill [-s sigspec | -n signum | -sigspec] pid | jobspec ... or kill ->
 [ arg... ]                                                              let arg [arg ...]
 [[ expression ]]                                                        local [option] name[=value] ...
 alias [-p] [name[=value] ... ]                                          logout [n]
 bg [job_spec ...]                                                       mapfile [-d delim] [-n count] [-O origin] [-s count] [-t] [-u fd] [->
 bind [-lpsvPSVX] [-m keymap] [-f filename] [-q name] [-u name] [-r ke>  popd [-n] [+N | -N]
 break [n]                                                               printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]                                       pushd [-n] [+N | -N | dir]
 caller [expr]                                                           pwd [-LP]
 case WORD in [PATTERN [| PATTERN]...) COMMANDS ;;]... esac              read [-ers] [-a array] [-d delim] [-i text] [-n nchars] [-N nchars] >
 cd [-L|[-P [-e]] [-@]] [dir]                                            readarray [-d delim] [-n count] [-O origin] [-s count] [-t] [-u fd] >
 challenge [--fortune] [--version] [--secret SECRET]                     readonly [-aAf] [name[=value] ...] or readonly -p
 command [-pVv] command [arg ...]                                        return [n]
 compgen [-abcdefgjksuv] [-o option] [-A action] [-G globpat] [-W word>  select NAME [in WORDS ... ;] do COMMANDS; done
 complete [-abcdefgjksuv] [-pr] [-DEI] [-o option] [-A action] [-G glo>  set [-abefhkmnptuvxBCEHPT] [-o option-name] [--] [-] [arg ...]
 compopt [-o|+o option] [-DEI] [name ...]                                shift [n]
 continue [n]                                                            shopt [-pqsu] [-o] [optname ...]
 coproc [NAME] command [redirections]                                    source filename [arguments]
 declare [-aAfFgiIlnrtux] [name[=value] ...] or declare -p [-aAfFilnrt>  suspend [-f]
 dirs [-clpv] [+N] [-N]                                                  test [expr]
 disown [-h] [-ar] [jobspec ... | pid ...]                               time [-p] pipeline
 echo [-neE] [arg ...]                                                   times
 enable [-a] [-dnps] [-f filename] [name ...]                            trap [-lp] [[arg] signal_spec ...]
 eval [arg ...]                                                          true
 exec [-cl] [-a name] [command [argument ...]] [redirection ...]         type [-afptP] name [name ...]
 exit [n]                                                                typeset [-aAfFgiIlnrtux] name[=value] ... or typeset -p [-aAfFilnrtu>
 export [-fn] [name[=value] ...] or export -p                            ulimit [-SHabcdefiklmnpqrstuvxPRT] [limit]
 false                                                                   umask [-p] [-S] [mode]
 fc [-e ename] [-lnr] [first] [last] or fc -s [pat=rep] [command]        unalias [-a] name [name ...]
 fg [job_spec]                                                           unset [-f] [-v] [-n] [name ...]
 for NAME [in WORDS ... ] ; do COMMANDS; done                            until COMMANDS; do COMMANDS-2; done
 for (( exp1; exp2; exp3 )); do COMMANDS; done                           variables - Names and meanings of some shell variables
 function name { COMMANDS ; } or name () { COMMANDS ; }                  wait [-fn] [-p var] [id ...]
 getopts optstring name [arg ...]                                        while COMMANDS; do COMMANDS-2; done
 hash [-lr] [-p pathname] [-dt] [name ...]                               { COMMANDS ; }
 help [-dms] [pattern ...]
hacker@man~help-for-builtins:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable. If DIR is "-", it is converted to $OLDPWD.
    
    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.
    
    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.
    
    Options:
      -L        force symbolic links to be followed: resolve symbolic
                links in DIR after processing instances of `..'
      -P        use the physical directory structure without following
                symbolic links: resolve symbolic links in DIR before
                processing instances of `..'
      -e        if the -P option is supplied, and the current working
                directory cannot be determined successfully, exit with
                a non-zero status
      -@        on systems that support it, present a file with extended
                attributes as a directory containing the file attributes
    
    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.
    
    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successfully when
    -P is used; non-zero otherwise.
hacker@man~help-for-builtins:~$ help cat
bash: help: no help topics match `cat'.  Try `help help' or `man -k cat' or `info cat'.
hacker@man~help-for-builtins:~$ help help
help: help [-dms] [pattern ...]
    Display information about builtin commands.
    
    Displays brief summaries of builtin commands.  If PATTERN is
    specified, gives detailed help on all commands matching PATTERN,
    otherwise the list of help topics is printed.
    
    Options:
      -d        output short description for each topic
      -m        display usage in pseudo-manpage format
      -s        output only a short usage synopsis for each topic matching
                PATTERN
    
    Arguments:
      PATTERN   Pattern specifying a help topic
    
    Exit Status:
    Returns success unless PATTERN is not found or an invalid option is given.
hacker@man~help-for-builtins:~$ help man
bash: help: no help topics match `man'.  Try `help help' or `man -k man' or `info man'.
hacker@man~help-for-builtins:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable. If DIR is "-", it is converted to $OLDPWD.
    
    The variable CDPATH defines the search path for the directory containing
    DIR.  Alternative directory names in CDPATH are separated by a colon (:).
    A null directory name is the same as the current directory.  If DIR begins
    with a slash (/), then CDPATH is not used.
    
    If the directory is not found, and the shell option `cdable_vars' is set,
    the word is assumed to be  a variable name.  If that variable has a value,
    its value is used for DIR.
    
    Options:
      -L        force symbolic links to be followed: resolve symbolic
                links in DIR after processing instances of `..'
      -P        use the physical directory structure without following
                symbolic links: resolve symbolic links in DIR before
                processing instances of `..'
      -e        if the -P option is supplied, and the current working
                directory cannot be determined successfully, exit with
                a non-zero status
      -@        on systems that support it, present a file with extended
                attributes as a directory containing the file attributes
    
    The default is to follow symbolic links, as if `-L' were specified.
    `..' is processed by removing the immediately previous pathname component
    back to a slash or the beginning of DIR.
    
    Exit Status:
    Returns 0 if the directory is changed, and if $PWD is set successfully when
    -P is used; non-zero otherwise.
hacker@man~help-for-builtins:~$ help touch
bash: help: no help topics match `touch'.  Try `help help' or `man -k touch' or `info touch'.
hacker@man~help-for-builtins:~$ help
GNU bash, version 5.2.37(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.

A star (*) next to a name means that the command is disabled.

 job_spec [&]                                                            history [-c] [-d offset] [n] or history -anrw [filename] or history >
 (( expression ))                                                        if COMMANDS; then COMMANDS; [ elif COMMANDS; then COMMANDS; ]... [ e>
 . filename [arguments]                                                  jobs [-lnprs] [jobspec ...] or jobs -x command [args]
 :                                                                       kill [-s sigspec | -n signum | -sigspec] pid | jobspec ... or kill ->
 [ arg... ]                                                              let arg [arg ...]
 [[ expression ]]                                                        local [option] name[=value] ...
 alias [-p] [name[=value] ... ]                                          logout [n]
 bg [job_spec ...]                                                       mapfile [-d delim] [-n count] [-O origin] [-s count] [-t] [-u fd] [->
 bind [-lpsvPSVX] [-m keymap] [-f filename] [-q name] [-u name] [-r ke>  popd [-n] [+N | -N]
 break [n]                                                               printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]                                       pushd [-n] [+N | -N | dir]
 caller [expr]                                                           pwd [-LP]
 case WORD in [PATTERN [| PATTERN]...) COMMANDS ;;]... esac              read [-ers] [-a array] [-d delim] [-i text] [-n nchars] [-N nchars] >
 cd [-L|[-P [-e]] [-@]] [dir]                                            readarray [-d delim] [-n count] [-O origin] [-s count] [-t] [-u fd] >
 challenge [--fortune] [--version] [--secret SECRET]                     readonly [-aAf] [name[=value] ...] or readonly -p
 command [-pVv] command [arg ...]                                        return [n]
 compgen [-abcdefgjksuv] [-o option] [-A action] [-G globpat] [-W word>  select NAME [in WORDS ... ;] do COMMANDS; done
 complete [-abcdefgjksuv] [-pr] [-DEI] [-o option] [-A action] [-G glo>  set [-abefhkmnptuvxBCEHPT] [-o option-name] [--] [-] [arg ...]
 compopt [-o|+o option] [-DEI] [name ...]                                shift [n]
 continue [n]                                                            shopt [-pqsu] [-o] [optname ...]
 coproc [NAME] command [redirections]                                    source filename [arguments]
 declare [-aAfFgiIlnrtux] [name[=value] ...] or declare -p [-aAfFilnrt>  suspend [-f]
 dirs [-clpv] [+N] [-N]                                                  test [expr]
 disown [-h] [-ar] [jobspec ... | pid ...]                               time [-p] pipeline
 echo [-neE] [arg ...]                                                   times
 enable [-a] [-dnps] [-f filename] [name ...]                            trap [-lp] [[arg] signal_spec ...]
 eval [arg ...]                                                          true
 exec [-cl] [-a name] [command [argument ...]] [redirection ...]         type [-afptP] name [name ...]
 exit [n]                                                                typeset [-aAfFgiIlnrtux] name[=value] ... or typeset -p [-aAfFilnrtu>
 export [-fn] [name[=value] ...] or export -p                            ulimit [-SHabcdefiklmnpqrstuvxPRT] [limit]
 false                                                                   umask [-p] [-S] [mode]
 fc [-e ename] [-lnr] [first] [last] or fc -s [pat=rep] [command]        unalias [-a] name [name ...]
 fg [job_spec]                                                           unset [-f] [-v] [-n] [name ...]
 for NAME [in WORDS ... ] ; do COMMANDS; done                            until COMMANDS; do COMMANDS-2; done
 for (( exp1; exp2; exp3 )); do COMMANDS; done                           variables - Names and meanings of some shell variables
 function name { COMMANDS ; } or name () { COMMANDS ; }                  wait [-fn] [-p var] [id ...]
 getopts optstring name [arg ...]                                        while COMMANDS; do COMMANDS-2; done
 hash [-lr] [-p pathname] [-dt] [name ...]                               { COMMANDS ; }
 help [-dms] [pattern ...]
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "ICLHZRI5".
hacker@man~help-for-builtins:~$ /challenge/challenge --secret ICLHzRI5
bash: /challenge/challenge: No such file or directory
hacker@man~help-for-builtins:~$ challenge --secret ICLHZRI5
Correct! Here is your flag!
pwn.college{ICLHZRI5IekthAhRqvX-ROoosJU.QX0ETO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use the help command to find out more about built in commands to use them to solve problems

## References
None.
