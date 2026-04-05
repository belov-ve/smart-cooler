# Smart-Cooler
Smcooler system servis to control the fan on raspberry
---

- This branch is for OS: *Debian 13 (`Trixie`)*

- For OS `Stretch`, `Buster`, `Bullseye` go to: [branch](https://github.com/belov-ve/smart-cooler/tree/buster)

---
smcooler - python script<br>
smcooler.service - configuration file of service<br>
Schematic_Smart-cooler.zip - electrical schematics<br>

### How to download the project:
```bash
git clone -b trixie https://github.com/belov-ve/smart-cooler.git
```
or
```bash
git clone -b trixie https://github.com/belov-ve/smart-cooler.git existing_folder
```
  

### How to update the project and drop local changes:
```bash
git reset --hard HEAD
git pull origin trixie
```

### How to test the fan control:
```bash
pinctrl set 14 op dh   # включает вентилятор?
pinctrl set 14 op dl   # выключает?
```
The command that turns on the fan is the level specified in the smcooler script's activeHigh:
- activeHigh = True if it turns on dh
- activeHigh = False if it turns on dl


### How to set the fan turn-on temperature:
	In the smcooler script, set the variable `tempOn`.

### How to set the fan turn-off temperature:
	In the smcooler script, set the variable `deltaOff`.
	The fan shut-off temperature will be equal to `tempOn`-`deltaOff`.

### How to install and activate the service:
```bash
cd <directory with git>
sudo chmod +x smcooler
sudo cp smcooler /usr/bin/
sudo cp smcooler.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable smcooler.service
sudo systemctl start smcooler.service
```


### How to check the script or service after installation:
```bash
# Script check
smcooler

# Service check
systemctl status smcooler.service

# Service operation log
journalctl -fu smcooler
```


### Service commands:
```bash
systemctl start smcooler

systemctl stop smcooler
# After turning off the service, the fan will be turned on.

systemctl restart smcooler
```

### How to get the temperature of the raspberry processor:<br>
```bash
smcooler
# to interrupt press CTRL + C
```
    
