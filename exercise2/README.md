# Exercise 2 - Attaching strace to Nginx

## Implementation:

To attach strace to Nginx, I first ran the command `ps aux -P | grep nginx` to find the PID of nginx root, which was 488. With this, I was able to use the PID with the -p option in strace. I then ran the actual command: `sudo strace -p 488 -s 10000 -v -f -o strace_output.txt`, making sure to add the -f flag to follow forks, and the -o flag to save strace output to the file strace_output.txt. 
Then, while the command ran, I opened a new terminal and reloaded nginx with the command: `sudo service nginx reload`. Next, I just did a simple curl request to localhost. I exited the strace command and then checked the output file contents.





