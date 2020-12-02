# FFUF Report

  Command line : `ffuf -c -w /usr/share/wordlists/dirb/common.txt -u http://academy.htb/FUZZ -of md -o common-ffuf.md`
  Time: 2020-12-02T10:54:58&#43;05:30

  | FUZZ | URL | Redirectlocation | Position | Status Code | Content Length | Content Words | Content Lines | ResultFile |
  | :- | :-- | :--------------- | :---- | :------- | :---------- | :------------- | :------------ | :--------- |
  |  | http://academy.htb/ |  | 1 | 200 | 2117 | 890 | 77 |  |
  | admin.php | http://academy.htb/admin.php |  | 290 | 200 | 2633 | 668 | 142 |  |
  | .htpasswd | http://academy.htb/.htpasswd |  | 13 | 403 | 276 | 20 | 10 |  |
  | .hta | http://academy.htb/.hta |  | 11 | 403 | 276 | 20 | 10 |  |
  | .htaccess | http://academy.htb/.htaccess |  | 12 | 403 | 276 | 20 | 10 |  |
  | images | http://academy.htb/images | http://academy.htb/images/ | 1991 | 301 | 311 | 20 | 10 |  |
  | index.php | http://academy.htb/index.php |  | 2021 | 200 | 2117 | 890 | 77 |  |
  | server-status | http://academy.htb/server-status |  | 3588 | 403 | 276 | 20 | 10 |  |
  