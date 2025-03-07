# r8188eu

### FOR TP_LINK tl wn725n v2

- To install in Linux

```bash
sudo apt update && sudo apt upgrade -y
```
```
sudo apt install build-essential dkms 
```
> Not sure if this step is need but just incase adding it.
```
git clone https://github.com/aircrack-ng/rtl8188eus.git
cd rtl8188eus
```

```
echo "blacklist r8188eu" | sudo tee -a /etc/modprobe.d/blacklist.conf
sudo modprobe -r r8188eu
```

```
make
sudo make install
sudo modprobe 8188eu
```