# Exercise 2 - Nginx Requests over TLS

## Implementation:

For this exercise, I first created a folder `openssl` in my `/etc/nginx` directory, within which I would be storing all the keys and certificates (folder included in the repo). I cd'd into the directory and used the `openssl` command to first generate a public-private key pair named `ssyeda.key` and `ssyeda_public.key` respectively. 
Next, I created a certificate signing request (CSR) with `openssl` and named it `ssyeda.csr`. Because we are creating a self-signed certificate rather than handing the certificate over to a CA, I ran the `openssl x509` command to self-sign, which output the certificate `ssyeda.crt`. 

Next, with the key pair and certificate created, I went into my `nginx.conf` file and modified the `listen` directives (for both TCP and UNIX) to include ssl. Below that, I included the locations for the certificate and the key so nginx would know where to look when connecting over TLS. 

Then, I went into the bash script and modified all commands (both curl and h2load) for every option to listen over TLS by changing http to https in the address name, and for curl including the -k command.

Finally, I ran strace while connecting to localhost over TLS to verify that the encryption was working. The output can be found in the file `strace_output.txt`.

Note: As a group, we also took a look at the config file in Joe's repository and fixed ours to only include the root location block without having to specify all others.
