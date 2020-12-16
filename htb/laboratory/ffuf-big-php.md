# FFUF Report

  Command line : `ffuf -c -w /usr/share/wordlists/dirb/big.txt -u https://laboratory.htb/FUZZ.php -of md -o ffuf-big-php.md -e .php`
  Time: 2020-12-05T18:50:30&#43;05:30

  | FUZZ | URL | Redirectlocation | Position | Status Code | Content Length | Content Words | Content Lines | ResultFile |
  | :- | :-- | :--------------- | :---- | :------- | :---------- | :------------- | :------------ | :--------- |
  | .htpasswd | https://laboratory.htb/.htpasswd.php |  | 31 | 403 | 280 | 20 | 10 |  |
  | .htaccess | https://laboratory.htb/.htaccess.php |  | 29 | 403 | 280 | 20 | 10 |  |
  | .htaccess.php | https://laboratory.htb/.htaccess.php.php |  | 30 | 403 | 280 | 20 | 10 |  |
  | .htpasswd.php | https://laboratory.htb/.htpasswd.php.php |  | 32 | 403 | 280 | 20 | 10 |  |
  