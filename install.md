My install instructions for linux (Ubuntu Server)

```bash
# System automatic updates
sudo apt-get install unattended-upgrades
sudo dpkg-reconfigure unattended-upgrades

# Extra libraries for file previews
sudo apt install --no-install-recommends python3-pil ffmpeg

# Install copyparty
cd /usr/local/bin/
sudo wget https://github.com/9001/copyparty/releases/latest/download/copyparty-sfx.py

# Create config
cd /etc/
sudo wget https://raw.githubusercontent.com/George9Waller/copyparty/refs/heads/hovudstraum/contrib/systemd/copyparty.conf
# Edit the file to CHANGE THE PASSWORD for my user
sudo nano copyparty.conf

# Install service
sudo useradd -r -s /sbin/nologin -m -d /var/lib/copyparty copyparty
cd /etc/systemd/system/
sudo wget https://raw.githubusercontent.com/9001/copyparty/refs/heads/hovudstraum/contrib/systemd/copyparty.service
```
