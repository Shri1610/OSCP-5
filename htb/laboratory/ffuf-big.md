# FFUF Report

  Command line : `ffuf -c -w /usr/share/wordlists/dirb/big.txt -u https://laboratory.htb/FUZZ -of md -o ffuf-big.md`
  Time: 2020-12-04T22:25:50&#43;05:30

  | FUZZ | URL | Redirectlocation | Position | Status Code | Content Length | Content Words | Content Lines | ResultFile |
  | :- | :-- | :--------------- | :---- | :------- | :---------- | :------------- | :------------ | :--------- |
  | .htaccess | https://laboratory.htb/.htaccess |  | 15 | 403 | 280 | 20 | 10 |  |
  | .htpasswd | https://laboratory.htb/.htpasswd |  | 16 | 403 | 280 | 20 | 10 |  |
  | assets | https://laboratory.htb/assets | https://laboratory.htb/assets/ | 2716 | 301 | 319 | 20 | 10 |  |
  | images | https://laboratory.htb/images | https://laboratory.htb/images/ | 9378 | 301 | 319 | 20 | 10 |  |
  | server-status | https://laboratory.htb/server-status |  | 16215 | 403 | 280 | 20 | 10 |  |
  