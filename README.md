# heartbleed
A Heartbleed (CVE-2014-0160) PoC in Python 3

```
usage: python3 heartbleed.py [-h] host [port]

Heartbleed PoC

positional arguments:
  host        hostname or IP address
  port        TCP port number (default IS 443)

options:
  -h, --help  show this help message and exit
```
After running the script check for the output file using xxd to see the result:
```
xxd response_data.bin
```
Test for heartbleed vulnerability using nmap:
```nmap -v -p443 --script ssl-heartbleed $IP```

If you want a vulnerable server, you can set it up from [here](https://github.com/jas9reet/heartbleed-lab "Heartbleed lab") 
