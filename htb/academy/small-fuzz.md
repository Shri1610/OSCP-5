# FFUF Report

  Command line : `ffuf -c -w /usr/share/wordlists/dirb/small.txt -u http://academy.htb/FUZZ -of md -o small-fuzz.md`
  Time: 2020-12-02T10:59:29&#43;05:30

  | FUZZ | URL | Redirectlocation | Position | Status Code | Content Length | Content Words | Content Lines | ResultFile |
  | :- | :-- | :--------------- | :---- | :------- | :---------- | :------------- | :------------ | :--------- |
  | images | http://academy.htb/images | http://academy.htb/images/ | 425 | 301 | 311 | 20 | 10 |  |
  