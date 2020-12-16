# FFUF Report

  Command line : `ffuf -c -w /usr/share/wordlists/dirb/common.txt -u https://laboratory.htb/FUZZ -of md -o ffuf-common.md`
  Time: 2020-12-04T22:33:46&#43;05:30

  | FUZZ | URL | Redirectlocation | Position | Status Code | Content Length | Content Words | Content Lines | ResultFile |
  | :- | :-- | :--------------- | :---- | :------- | :---------- | :------------- | :------------ | :--------- |
  |  | https://laboratory.htb/ |  | 1 | 200 | 7254 | 426 | 210 |  |
  | .hta | https://laboratory.htb/.hta |  | 11 | 403 | 280 | 20 | 10 |  |
  | .htaccess | https://laboratory.htb/.htaccess |  | 12 | 403 | 280 | 20 | 10 |  |
  | .htpasswd | https://laboratory.htb/.htpasswd |  | 13 | 403 | 280 | 20 | 10 |  |
  | assets | https://laboratory.htb/assets | https://laboratory.htb/assets/ | 499 | 301 | 319 | 20 | 10 |  |
  | images | https://laboratory.htb/images | https://laboratory.htb/images/ | 1991 | 301 | 319 | 20 | 10 |  |
  | index.html | https://laboratory.htb/index.html |  | 2020 | 200 | 7254 | 426 | 210 |  |
  | server-status | https://laboratory.htb/server-status |  | 3588 | 403 | 280 | 20 | 10 |  |
  