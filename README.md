# heartbleed
A Heartbleed (CVE-2014-0160) PoC in Python 3

```usage: heartbleed.py [-h] host [port]

Heartbleed PoC

positional arguments:
  host        hostname or IP address
  port        TCP port number (default IS 443)

options:
  -h, --help  show this help message and exit
```

Test for heartbleed vulnerability using nmap:
```nmap -v -p443 --script ssl-heartbleed $IP```

If you want a vulnerable server, you can set it up from [here](https://www.google.com](https://github.com/jas9reet/heartbleed-lab) "Heartbleed lab") 
[I'm an inline-style link with title](https://www.google.com "Google's Homepage")
