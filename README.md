# DarkScanner

```bash
apt-get update
apt-get install tor git bison libexif-dev
apt-get install python-pip
pip install stem
bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
[[ -s "$HOME/.gvm/scripts/gvm" ]] && source "$HOME/.gvm/scripts/gvm"
source /root/.gvm/scripts/gvm
gvm install go1.5 --binary
gvm use go1.5
go get github.com/s-rah/onionscan
go install github.com/s-rah/onionscan

If oninonscan fails to load:
gvm use go1.5

tor --hash-password DarkIntel
Output: "16:3E73307B3E434914604C25C498FBE5&RHTBAAF70616591AAF8"

sudo nano /etc/tor/torrc
Paste at the bottom:

ControlPort 9051
ControlListenAddress 127.0.0.1
HashedControlPassword 16:3E73307B3E434914604C25C498FBE5&RHTBAAF70616591AAF88

service tor restart
wget https://raw.githubusercontent.com/DarkIntel/DarkScanner/1.0.0-dev/DarkScanner.list
```
