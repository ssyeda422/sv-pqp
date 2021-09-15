# Exercise 1 - NGINX Server Requests with cURL and h2load

## Implementation:

This exercise 1 folder includes the basic sites-enabled folder containing a new server configuration called "warmup." This file contains the location blocks for each of the various sized zero-filled objects, under the directory /var/www/warmup. 

The /var/www/warmup folder is included as well, with each file under its own folder named based on size: tenkb, hundredkb, onemb, twomb, eightmb, and tenmb. This folder also contains the default root html page upon which the directories are expanded to include each static content page.

Finally, this folder contains a simple bash script "warmup-script" which asks the user:
- Which command to use (curl or h2load)
- If h2load, how many requests to send
- And finally, which file size to ping out of the following options: tenkb, hundredkb, onemb, twomb, eightmb, and tenmb.

Then, based on the user's input, the script will return the output of the commands, pinging the server http://localhost:81 with the specified filesize extension.

## Directions:

To run this script, you can either use bash or add it to your path and run with the command `<warmup-script>`. In addition, make sure the warmup folders under both sites-enabled and www are included in the appropriate directories.

Nginx and h2load must both be installed in your environment. As mentioned above, once the server is started up, the host will be listening on port 81. 


