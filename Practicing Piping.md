# Redirecting Output
In this challenge, we learn to redirect output of a particular command to a file.

## My Solve
**Flag:** pwn.college{Y5GmmwJ2CfaPXm-kb-61riIPP2X.QX0YTN0wSOzEzNzEzW}

```
hacker@piping~redirecting-output:~$ PWN > COLLEGE
bash: PWN: command not found
You have created the COLLEGE file, but you didn't write the correct value to 
it. Make sure to write PWN to the COLLEGE file.
hacker@piping~redirecting-output:~$ PWN > COLLEGE
bash: PWN: command not found
You have created the COLLEGE file, but you didn't write the correct value to 
it. Make sure to write PWN to the COLLEGE file.
hacker@piping~redirecting-output:~$ ls
COLLEGE  Desktop  Downloads  a  core
You have created the COLLEGE file, but you didn't write the correct value to 
it. Make sure to write PWN to the COLLEGE file.
hacker@piping~redirecting-output:~$ cat PWN > COLLEGE
cat: PWN: No such file or directory
You have created the COLLEGE file, but you didn't write the correct value to 
it. Make sure to write PWN to the COLLEGE file.
hacker@piping~redirecting-output:~$ COLLEGE > PWN
bash: COLLEGE: command not found
You have created the COLLEGE file, but you didn't write the correct value to 
it. Make sure to write PWN to the COLLEGE file.
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{Y5GmmwJ2CfaPXm-kb-61riIPP2X.QX0YTN0wSOzEzNzEzW}
```

## What I learnt
I learnt how to redirect output messages, shown in the console by default, into files like COLLEGE in this case

## References
None.


# Redirecting More Output
Just like the previous challenge, the goal here is to redirect output of a command into a file.

## My Solve
**Flag:** pwn.college{IX7baoO_ZnOmB2EHKD8WMLaYP60.QX1YTN0wSOzEzNzEzW}

```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{IX7baoO_ZnOmB2EHKD8WMLaYP60.QX1YTN0wSOzEzNzEzW}
```

## What I learnt
I learnt how to redirect the output of other commands to different files.

## References
discord.gg/pwncollege (Had to change interface to VSCode)


# Appending Output
In this challenge, we learn to append output to an existing file

## My Solve
**Flag:** pwn.college{4g0cqjsN3J4LsRwkXTkrpi1A4k3.QX3ATO0wSOzEzNzEzW}

```
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
the first write directly to the file, and the second write, I'll do to stdout 
(if it's pointing at the file). If you redirect the output in append mode, the 
second write will append to (rather than overwrite) the first write, and you'll 
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 | 
\|/ This is the first half:
 v 
pwn.college{4g0cqjsN3J4LsRwkXTkrpi1A4k3.QX3ATO0wSOzEzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
```
## What I learnt
I learnt how to append contents of one file to another (by changing the output location) using >>

## References
None.


# Redirecting Errors
