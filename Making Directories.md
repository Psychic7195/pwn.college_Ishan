# Making Directories
In this challenge we learn how to use the mkdir command

## My Solve
**Flag:** pwn.college{MfWOyuNd5scZa62DkzqqzIP-Daa.QXxMDO0wSOzEzNzEzW}
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{MfWOyuNd5scZa62DkzqqzIP-Daa.QXxMDO0wSOzEzNzEzW}
```
The folder is first created and then accessed, after which a file is made within the folder.

## What I learnt
I learnt how to use the mkdir command to make a directory in linux.

## References
None.
