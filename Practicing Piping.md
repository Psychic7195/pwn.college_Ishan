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
In this challenge, we learn to redirect multiple attributes at the same time.

## My Solve
**Flag:** pwn.college{03ir3iWbsTOoDSPjaOH2Sjv2EEu.QX3YTN0wSOzEzNzEzW}

```
hacker@piping~redirecting-errors:~$ /challenge/run 1> myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{03ir3iWbsTOoDSPjaOH2Sjv2EEu.QX3YTN0wSOzEzNzEzW}
```

## What I learned
I learned how to direct both output and errors at the same time using the > operator.

## References
None.


# Redirecting Input
In this challenge we learn how to redirect the input of a file along with the command

## My Solve
**Flag:** pwn.college{Mcx73j7RzKOfRrBdjEtlmnsqRF_.QXwcTN0wSOzEzNzEzW}

```
hacker@piping~redirecting-input:~$ /challenge/run
You have not redirected anything to my standard input. Please do so, using '<'.
hacker@piping~redirecting-input:~$ PWN < COLLEGE
bash: PWN: command not found
hacker@piping~redirecting-input:~$ COLLEGE < PWN
bash: COLLEGE: command not found
hacker@piping~redirecting-input:~$ PWN > COLLEGE
bash: PWN: command not found
hacker@piping~redirecting-input:~$ rev < PWN
EGELLOC
hacker@piping~redirecting-input:~$ /challenge/run
You have not redirected anything to my standard input. Please do so, using '<'.
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ cat PWN
COLLEGE
hacker@piping~redirecting-input:~$ rev < PWN
EGELLOC
hacker@piping~redirecting-input:~$ /challenge/run
You have not redirected anything to my standard input. Please do so, using '<'.
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{Mcx73j7RzKOfRrBdjEtlmnsqRF_.QXwcTN0wSOzEzNzEzW}
```

## What I learnt
I learnt how to redirect input using the < operator and use commands with it.

## References
None.


# Grepping Stored Results
In this challenge, we use the grep command to search for contents of a file after redirecting the output.

## My Solve
**Flag:** pwn.college{0LC9oFl63vdvoQ1eUP_qxV0scUt.QX4EDO0wSOzEzNzEzW}

```
hacker@piping~grepping-stored-results:~$ /challenge/run 1> /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep 'pwn' /tmp/data.txt
pwn.college{0LC9oFl63vdvoQ1eUP_qxV0scUt.QX4EDO0wSOzEzNzEzW}
pwning
pwn
pwns
pwned
```

## What I learned
I learned how to use the grep command again, after redirecting output of other files.

## References
None.


# Grepping Live Output
In this challenge, we learn how to use the pipe operator |

## My Solve
**Flag:** pwn.college{U9vZwEr4yQEf3f4FMLbnqRAXPLO.QX5EDO0wSOzEzNzEzW}

```
hacker@piping~grepping-live-output:~$ /challenge/run | grep "pwn"
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwned
pwning
pwns
pwn
pwn.college{U9vZwEr4yQEf3f4FMLbnqRAXPLO.QX5EDO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use the | operator to eliminate the need of using a file to store output first, and directly engaging with the file and searching for its contents at the same time.

## References
None.


# Grepping Errors
In this challenge, we learn how to redirect standard output and error together

## My Solve
**Flag:** pwn.college{Yl2gJIDeAmAr72nXKsabeKAKXVb.QX1ATO0wSOzEzNzEzW}

```
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep "pwn"
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{Yl2gJIDeAmAr72nXKsabeKAKXVb.QX1ATO0wSOzEzNzEzW}
pwns
pwning
pwned
pwn
```

## What I learnt
I learnt how to redirect standard output along with the standard error using the >& operator, while using the | operator to use the grep command at the same time.

## References
None.

# Filtering with grep -v
In this challenge, we learn how to use the -v option of the grep command.

## My Solve
**Flag:** pwn.college{8zy9yWd2Fi8Q4ReeFiS-t4QvpRO.0FOxEzNxwSOzEzNzEzW}

```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{8zy9yWd2Fi8Q4ReeFiS-t4QvpRO.0FOxEzNxwSOzEzNzEzW}
```

## What I learnt
I learnt how to use the -v flag of the grep command to filter out results and only include results which do not have certain patterns.

## References
None.

