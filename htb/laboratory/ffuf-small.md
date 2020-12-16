# FFUF Report

  Command line : `ffuf -c -w /usr/share/wordlists/dirb/small.txt -u https://laboratory.htb/FUZZ -of md -o ffuf-small.md`
  Time: 2020-12-04T22:35:03&#43;05:30

  | FUZZ | URL | Redirectlocation | Position | Status Code | Content Length | Content Words | Content Lines | ResultFile |
  | :- | :-- | :--------------- | :---- | :------- | :---------- | :------------- | :------------ | :--------- |
  | assets | https://laboratory.htb/assets | https://laboratory.htb/assets/ | 96 | 301 | 319 | 20 | 10 |  |
  | images | https://laboratory.htb/images | https://laboratory.htb/images/ | 425 | 301 | 319 | 20 | 10 |  |
  