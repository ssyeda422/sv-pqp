# Exercise 2 - Attaching strace to Nginx

## Implementation:

To attach strace to Nginx, I first ran the command `ps aux -P | grep nginx` to find the PID of nginx root, which was 488. With this, I was able to use the PID with the -p option in strace. I then ran the actual command: `sudo strace -p <PID-HERE> -s 10000 -v -f -o strace_output.txt`, making sure to add the -f flag to follow forks, and the -o flag to save strace output to the file strace_output.txt. 
Then, while the command ran, I opened a new terminal and reloaded nginx with the command: `sudo service nginx reload`. Next, I just did a simple curl request to localhost listening on a unix socket. I exited the strace command and then checked the output file contents.

The output starts off with rt_sigsuspend and looks like it waits until it receives a signal to start. An interesting command that comes up a few lines later is openat, which seems to look into the necessary directories like `etc/nginx/nginx.conf` to open up files. Based on the output, it looks like nginx is systematically going through each file, using fstat to check the file status, and closing. A few other common commands I saw show up frequently were lseek, recvmsg, and epoll_wait.





