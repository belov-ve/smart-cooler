# smart-cooler
smcooler system servis to control the fan on raspberry

smcooler - python script<br>
smcooler.service - configuration file of service<br>
Schematic_Smart-cooler.zip - electrical schematics<br>

How to install and activate the service:<br>
    # apt-get install python-rpi.gpio python3-rpi.gpio<br>
    # chmod +x smcooler<br>
    # cp smcooler /usr/bin/<br>
    # cp smcooler.service /etc/systemd/system/<br>
    # systemctl enable smcooler.service<br>

How to check the script and service after installation:<br>
    # smcooler<br>
    or<br>
    # systemctl status smcooler.service<br>

Service commands:<br>
    # systemctl start smcooler<br>
    # systemctl restart smcooler<br>
    # systemctl stop smcooler<br>

How to get the temperature of the raspberry processor:<br>
    # smcooler<br>
    (to interrupt press CTRL + C)<br>
