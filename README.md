# smart-cooler
Smcooler system servis to control the fan on raspberry
---
smcooler - python script<br>
smcooler.service - configuration file of service<br>
Schematic_Smart-cooler.zip - electrical schematics<br>

### How to download the project:<br>
    # cd existing_folder
    # git init
    # git remote add origin git://github.com/belov-ve/smart-cooler
    # git pull origin master
    

### How to update the project and drop local changes:<br>
    # git status
      Find the modified files. We transfer them or cancel the changes with the command
      (for example file smcooler):
    # git checkout -- smcooler
    # git pull origin master

### How to install and activate the service:<br>
    # apt-get install python-rpi.gpio python3-rpi.gpio
    # chmod +x smcooler
    # sudo cp smcooler /usr/bin/
    # sudo cp smcooler.service /etc/systemd/system/
    # sudo systemctl enable smcooler.service
    # sudo systemctl start smcooler

### How to check the script and service after installation:<br>
    # smcooler
    or
    # systemctl status smcooler.service

### Service commands:<br>
    # systemctl start smcooler
    # systemctl stop smcooler
    # systemctl restart smcooler

### How to get the temperature of the raspberry processor:<br>
    # smcooler
    (to interrupt press CTRL + C)
    
