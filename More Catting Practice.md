# More Catting Practice
In this challenge, we find the flag hidden in a more complex directory.

## My Solve
**Flag:** pwn.college{AB5l9H-hjiGoBZ9lNp6LTXJ8aI6.QXwITO0wSOzEzNzEzW}

 The directory of the flag is given in the console, for which we need to run the command cat /lib/ssl/flag to read the contents of the flag.md file.

```
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /lib/ssl/flag. Go cat it out **without** cding into that directory!
hacker@commands~more-catting-practice:~$ cat /lib/ssl/flag
pwn.college{AB5l9H-hjiGoBZ9lNp6LTXJ8aI6.QXwITO0wSOzEzNzEzW}
```

## What I learned
I learned how to use the absolute path of a file to read it using the cat command.

## References
None.
