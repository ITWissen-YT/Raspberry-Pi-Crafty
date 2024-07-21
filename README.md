# Raspberry-Pi-Crafty Befehle
1. sudo apt update -y && sudo apt upgrade -y

2. sudo reboot

3. git clone https://gitlab.com/crafty-controller/crafty-installer-4.0.git

4. cd crafty-installer-4.0

5. sudo ./install_crafty.sh

7. sudo systemctl start crafty

8. sudo cat /var/opt/minecraft/crafty/crafty-4/app/config/default-creds.txt

9. https://127.0.0.1:8443


Auto start

1. sudo nano /etc/systemd/system/crafty.service

2. 

[Unit]
Description=Crafty Minecraft Server Manager
After=network.target

[Service]
User=crafty
WorkingDirectory=/var/opt/minecraft/crafty
ExecStart=/var/opt/minecraft/crafty/run_crafty.sh
Restart=on-failure

[Install]
WantedBy=multi-user.target


3. sudo systemctl enable crafty

4. sudo systemctl start crafty



