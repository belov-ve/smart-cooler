# Smart-Cooler
Smcooler system servis to control the fan on raspberry
---

- This branch is for OS: *`Stretch`, `Buster`, `Bullseye`*

- For OS 'Trixie' go: [Debian 13 (trixie)](https://github.com/belov-ve/smart-cooler/tree/trixie)

---
smcooler - python script<br>
smcooler.service - configuration file of service<br>
Schematic_Smart-cooler.zip - electrical schematics<br>

### How to download the project:
```bash
git clone -b buster https://github.com/belov-ve/smart-cooler.git
```
or
```bash
git clone -b buster https://github.com/belov-ve/smart-cooler.git existing_folder
```
  

### How to update the project and drop local changes:
```bash
git reset --hard HEAD
git pull origin buster
```


### How to install and activate the service:
```bash
apt-get install python-rpi.gpio python3-rpi.gpio
chmod +x smcooler
sudo cp smcooler /usr/bin/
sudo cp smcooler.service /etc/systemd/system/
sudo systemctl enable smcooler.service
sudo systemctl start smcooler
```


### How to check the script or service after installation:
```bash
# Script check
smcooler
# Service check
systemctl status smcooler.service
```


### Service commands:
```bash
systemctl start smcooler
systemctl stop smcooler
systemctl restart smcooler
```

### How to get the temperature of the raspberry processor:<br>
```bash
smcooler
# to interrupt press CTRL + C
```
    
