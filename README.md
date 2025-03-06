# TUTORIAL INSTALL CLOUD9 IN VPS 
## Support : 
- Ubuntu 20.04
- Ubuntu 22.04

# Following this step ! :
Install git :
```
sudo apt install git -y
```
Install curl :
```
sudo apt install curl -y
```
Install screen :
```
sudo apt install screen -y
```
Install nodejs :
```
sudo apt install nodejs -y 
```
Install build-essential :
```
sudo apt install build-essential -y
```
Install unzip :
```
sudo apt install unzip -y
```
Install make :
```
sudo apt install make -y
```
Install gcc :
```
sudo apt install gcc -y
```
Enable firewall :
```
sudo ufw --force enable
```
Allow port 8181 & tcp 22:
```
sudo ufw allow 8181
sudo ufw allow 22/tcp
sudo ufw reload
```
Install Php7.2 :
```
sudo apt -y install php7.2 libapache2-mod-php7.2 php7.2-common
```
Update & upgrade :
```
sudo DEBIAN_FRONTEND=noninteractive apt update -y && sudo DEBIAN_FRONTEND=noninteractive apt upgrade -yq
```
Git clone cloud9 :
```
git clone https://github.com/c9/core.git c9-shareithub
```
Install sdk :
```
cd ~ && cd c9-shareithub && scripts/install-sdk.sh
```
create screen :
```
screen -S c9
```
Run server Cloud9 :
```
cd ~ && cd c9-shareithub && node server.js -p 8181 --listen 0.0.0.0 -a username:password -w /shareithub
```
# Change :

username = your username to login cloud9

password = your password to login cloud9

Example : cd ~ && cd c9-shareithub && node server.js -p 8181 --listen 0.0.0.0 -a subscribe:shareithub -w /shareithub

# # After done,  u can exit screen :

` Type CTRL+A+D ` to exit screen

Go to browser ( recommended use ignitco mode ) and open cloud9 `http://yourIPvps:8181`





















































