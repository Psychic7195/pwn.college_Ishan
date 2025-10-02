# Matching With *
In this challenge, we learn how to use * to reduce search results.

## My Solve
**Flag:** pwn.college{MCPE5c8OjBDcHgK0HmF7P7ujgjL.QXxIDO0wSOzEzNzEzW}

```
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /challenge
You specified the path to 'cd' to in more than 4 characters. Disallowed!
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ ls
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
Desktop  Downloads  a  core
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /cha*
You specified the path to 'cd' to in more than 4 characters. Disallowed!
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ cat ch*
cat: 'ch*': No such file or directory
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{MCPE5c8OjBDcHgK0HmF7P7ujgjL.QXxIDO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use * to navigate through directories more easily.

## References 
None.

# Matching with ?
In this challenge, we learn how to use ? as a single character query while navigating.

## My Solve
**Flag:** pwn.college{kJ_wL_3euhMHDf20xQSjo595chZ.QXyIDO0wSOzEzNzEzW}

```
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{kJ_wL_3euhMHDf20xQSjo595chZ.QXyIDO0wSOzEzNzEzW}
```
## What I learnt
I learnt how to use the ? symbol as a single character "wild card" while navigating through directories.

## References 
None.

# Matching with []
In this challenge, we learn how to use [] as a query to search for one of many characters contained within the brackets.

## My Solve
**Flag:** pwn.college{ctHmT0PKHa55CwzZP0yHNvuwPTh.QXzIDO0wSOzEzNzEzW}

```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{ctHmT0PKHa55CwzZP0yHNvuwPTh.QXzIDO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use [] to contain a possible list of search queries for a character that is unknown.

## References
None.


# Matching Paths with []

In this challenge, we learn how to use brackets [] to map to absolute paths of certain files.

## My Solve
**Flag:** pwn.college{Aa4xx8l0JeYyTzMFnJstE1qFiH1.QX0IDO0wSOzEzNzEzW}

```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{Aa4xx8l0JeYyTzMFnJstE1qFiH1.QX0IDO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use brackets [] while mapping absolute paths of files we need to search for.

## References
None.


# Multiple Globs
In this challenge, we learn how to use multiple instances of the * character t look for certain files.

## My Solve
**Flag:** pwn.college{0DNVDBlAoyLEVyGo3DQ_GNGaeOu.0lM3kjNxwSOzEzNzEzW}

```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ cat *p*
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{0DNVDBlAoyLEVyGo3DQ_GNGaeOu.0lM3kjNxwSOzEzNzEzW}
```

## What I learnt
I learnt how to use multiple * characters to narrow my search results and, accordingly, run it.

## References
None.

# Exclusionary globbing
In this challenge, we learn how to use the [] brackets to negate certain search results

## My Solve
**Flag:** pwn.college{4oi9oC5osFe3hiissucqgIDCsG7.QX2IDO0wSOzEzNzEzW}

```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]
Your expansion did not expand to the requested files (amazing beautiful 
challenging delightful educational fantastic great happy incredible jovial kind 
laughing magical optimistic queenly radiant splendid thrilling uplifting 
victorious xenial youthful zesty).
Instead, it expanded to:
[!pwn]
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{4oi9oC5osFe3hiissucqgIDCsG7.QX2IDO0wSOzEzNzEzW}
```

## What I learnt
I learnt how to use brackets [] to reduce search results by negating search results using the ! sign

## References 
None.


# Tab Completion
In this challenge we learn how to use the tab key to autocomplete the predicted search query

## My Solve
**Flag:** pwn.college{oAddMaWhGa1OVc05dt1Uu-Kd26z.0FN0EzNxwSOzEzNzEzW}

```
hacker@globbing~tab-completion:~$ cd /challenge/pwncollege
bash: cd: /challenge/pwncollege: No such file or directory
hacker@globbing~tab-completion:~$ cd /challenge
hacker@globbing~tab-completion:/challenge$ ls
DESCRIPTION.md  pwncollege​
hacker@globbing~tab-completion:/challenge$ cd pwncollege
bash: cd: pwncollege: No such file or directory
hacker@globbing~tab-completion:/challenge$ cd *n*
This level disallows the use of * globs!
hacker@globbing~tab-completion:/challenge$ cd pwncollege​ 
bash: cd: pwncollege​: Not a directory
hacker@globbing~tab-completion:/challenge$ cat pwncollege​ 
pwn.college{oAddMaWhGa1OVc05dt1Uu-Kd26z.0FN0EzNxwSOzEzNzEzW}
```

## What I learnt
I learnt how to use the tab key to autocomplete the predicted search query.

## References
None.

# Multiple Options for Tab Completion
In this challenge we learn how to find all options from using the tab key

## My Solve
**Flag:** pwn.college{89tCDK2nJ-EXCqN0PllD7wo9yAc.0lN0EzNxwSOzEzNzEzW}

```
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files/p
bash: cd: /challenge/files/p: No such file or directory
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwn
No flag in this file!
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cd pwn
bash: cd: pwn: Not a directory
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter  
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter  
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwn-college
No flag in this file!
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-flag
pwn.college{89tCDK2nJ-EXCqN0PllD7wo9yAc.0lN0EzNxwSOzEzNzEzW}
```

## What I learnt
I learnt how to find all files matching the typed query using the tab key.

## References 
None.


# Tab Completion on Commands
In this challenge we learn how to use tab complete to autocomplete commands

## My Solve
**Flag:** pwn.college{Mv6yRrNZHYfme5DxGldeh4elu1B.0VN0EzNxwSOzEzNzEzW}

```
hacker@globbing~tab-completion-on-commands:~$ pwncollege-16417 
Correct! Here is your flag:
pwn.college{Mv6yRrNZHYfme5DxGldeh4elu1B.0VN0EzNxwSOzEzNzEzW}
```

## What I learnt 
I learnt how to complete the command by pressing tab

## References
None.
