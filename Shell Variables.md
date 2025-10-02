# Printing Variables
In this challenge, we learn how to use and print variables 

## My Solve
**Flag:** pwn.college{MhonFtr9P-LzTqOFwaVq7v_40Tx.QX3UTN0wSOzEzNzEzW}

```
hacker@variables~printing-variables:~$ echo FLAG
FLAG
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{MhonFtr9P-LzTqOFwaVq7v_40Tx.QX3UTN0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use variables and print them using echo and the $ sign before the variable name to define a variable.

## References
None.


# Setting Variables
In this challenge, we learn how to set values of variables

## My Solve
**Flag:** pwn.college{ksv-zQCldf9mrjjQKPOvgRDfeNg.QX5UTN0wSOzEzNzEzW}

```
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{ksv-zQCldf9mrjjQKPOvgRDfeNg.QX5UTN0wSOzEzNzEzW}
```

## What I learnt 
I learnt how to assign values of variables by using the "=" sign without spaces

## References 
None.


# Multi-word Variables
In this challenge we learn how to assign multiple words to a variable.

## My Solve
**Flag:** pwn.college{8LTkqc-WcC6lM_MRKcOvIGrmWc_.QXwYTN0wSOzEzNzEzW}

```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8LTkqc-WcC6lM_MRKcOvIGrmWc_.QXwYTN0wSOzEzNzEzW}
```

## What I learnt
I learnt how to assign multiple words to a single variable, using quotes ""

## References 
None.


# Exporting Variables
In this challenge, we learn how to export variables to children (shells)

## My Solve
**Flag:** pwn.college{IWJ71QFuu_s7khTK9AebeRJs-R1.QXyYTN0wSOzEzNzEzW}

```
hacker@variables~exporting-variables:~$ PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{IWJ71QFuu_s7khTK9AebeRJs-R1.QXyYTN0wSOzEzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

## What I learnt
I learnt how to export variables to children shells using the export command, as well as the scope of each variable.

## References 
None.


# Printing Exported Variables
In this challenge, we learn how to access exported variables in bash

## My Solve
**Flag:** FLAG=pwn.college{YbByh3MI2TUS_BEfF2HVUUeTLJs.QX4UTN0wSOzEzNzEzW}

```
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=1121ad813b54543fffb96d8bb4bd47fc93e414121dd5b6e60c62a71e4a2a436d
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{YbByh3MI2TUS_BEfF2HVUUeTLJs.QX4UTN0wSOzEzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

## What I learnt
I learnt how to access all the variables which have been exported using the env command.

## References
None.


# Storing Command Output
In this module, we learn how to assign outputs of commands directly to variables.

## My Solve
**Flag:** pwn.college{kzpq9Oi6Bz00osYZXy66yh3s7Tt.QX1cDN1wSOzEzNzEzW}

```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{kzpq9Oi6Bz00osYZXy66yh3s7Tt.QX1cDN1wSOzEzNzEzW}
```

## What I learnt
I learnt how to directly assign outputs of commands as the value of a variable using {varname}=$({command})

## References
None.


# Reading Input
In this challenge, we use the read command to read input from the user to assign to a variable.

## My Solve
**Flag:** pwn.college{oZXlAwuvrhhuXSKmsiejm1gYQtJ.QX4cTN0wSOzEzNzEzW}

```
pwn.college{oZXlAwuvrhhuXSKmsiejm1gYQtJ.QX4cTN0wSOzEzNzEzW}
```

## What I learnt
I learnt how to input the value of a variable from the user's end by using the read variable with the -p argument, forcing a prompt.

## References 
None.


# Reading Files
In this challenge, we use the read command to directly read files without the cat command.

## My Solve
**Flag:** pwn.college{0KKgYar6aX-nTkin9U1M61e09qT.QXwIDO0wSOzEzNzEzW}

```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{0KKgYar6aX-nTkin9U1M61e09qT.QXwIDO0wSOzEzNzEzW}
```


## What I learnt
I learnt how to read files using the read command, where we use the file path as the input. The contents are uploaded to a variable.

## References
None.
