# Hidden Files
In this challenge we find out how to access hidden files.

## My solve
**Flag:** pwn.college{YlgGdo7DTWkCK7fWFxoL6iLPysz.QXwUDO0wSOzEzNzEzW}

```
hacker@commands~hidden-files:~$ ls -a
.   .ICEauthority  .cache   .dbus  .local    Desktop    a
..  .bash_history  .config  .java  .mozilla  Downloads  core
hacker@commands~hidden-files:~$ cd .
hacker@commands~hidden-files:~$ cd /.
hacker@commands~hidden-files:/$ ls -a
.                     bin        etc    lib64   nix   run   tmp
..                    boot       home   libx32  opt   sbin  usr
.dockerenv            challenge  lib    media   proc  srv   var
.flag-13342301723744  dev        lib32  mnt     root  sys
hacker@commands~hidden-files:/$ ls
bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-13342301723744
pwn.college{YlgGdo7DTWkCK7fWFxoL6iLPysz.QXwUDO0wSOzEzNzEzW}

```
## What I Learned
I learned how to access hidden files using the -a flag to the ls command

## References
None.
