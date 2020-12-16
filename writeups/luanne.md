luanne

----
# Luanne HTB [ 10.10.10.218 ]

## Foothold

- Scan with rustscan to find out the open ports.
	` rustscan -b 500 -a luanne.htb -- -sV `
	
	|PORT   |STATE |SERVICE|REASON|VERSION |
	--------|------|-------|------|--------
	|22/tcp  | open | ssh   |  syn-ack |OpenSSH 8.0 (NetBSD 	20190418-hpn13v14-lpk; protocol 2.0)
	|80/tcp  | open | http   | syn-ack| nginx 1.19.0
	|9001/tcp| open | http    |syn-ack| Medusa httpd 1.12 	(Supervisor process manager)
- Check for the robots.txt file
	![fb952a32a9ff13524e37fa0e49c5951a.png](../_resources/3f8cd9993b2b43ab9b6419fa6d91857b.png)
- The /weather endpoint returned 404, fuzz further using ffuf.
	`ffuf -c -w /usr/share/wordlists/dirb/big.txt -u http://luanne.htb/weather/FUZZ -of md -o ffuf-big.md`
	
	The above command revealed the **/weather/forecast** endpoint.
	
- Accessing the endpoint returned a json output of the weather data for city queried.

	![d80387b4aa020c6207c7ddac797e6163.png](../_resources/ae3b28b14f6a4864b1394482c7aac28b.png)
	
- 
	