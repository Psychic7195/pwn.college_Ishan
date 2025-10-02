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
