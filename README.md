In order to use this you will need to have a clean install of Ubuntu server 22.04.
You need to log in to the server with a sudoer account and perform the following:

```
timedatectl set-timezone "_YOUR_TIME_ZONE_"
sudo apt update && sudo apt upgrade
sudo adduser [frappe-user]
usermod -aG sudo [frappe-user]
```
and then log in using the `[frapp-user]` above.
the rest is to execute:
```
sudo chmod +x frappe_install.sh
./frappe_install.sh
```
And follow the instructions. You will be prompt to supply your sudo password
(the password that you gave you [frappe-user]) and a required password for your mariadb server
root acount (select something complex enough, but a password you can remember...)
When you finished installing log off and log in and then you can continue with site creation,
app creation\install, etc..
Good luck! :-)
