# TUTORIAL INSTALL CLOUD9 IN VPS 
## Support : 
- Ubuntu 20.04
- Ubuntu 22.04

# Following this step ! :

Add ppa ondrej/php :
```
sudo add-apt-repository ppa:ondrej/php -y
```
Add universe repository :
```
sudo apt-add-repository universe -y
```
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
Install python2 :
```
sudo apt install python2 -y
```
Install python2-minimal :
```
sudo apt install python2-minimal -y
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

## FIX ERROR BEFORE RUN SERVER CLOUD9 :
```
cd ~ && cd c9-shareithub && git reset --hard
```
```
cd ~ && cd c9-shareithub && git fetch origin && git reset origin/HEAD --hard
```
```
cd ~ && cd c9-shareithub && scripts/install-sdk.sh
```
After done , u can run again command `Run server Cloud9`

# Change :

username = your username to login cloud9

password = your password to login cloud9

Example : cd ~ && cd c9-shareithub && node server.js -p 8181 --listen 0.0.0.0 -a subscribe:shareithub -w /shareithub

## After done,  u can exit screen :

press button in keyboard `CTRL+A+D ` to exit screen

Go to browser ( recommended use ignitco mode ) and open cloud9 `http://yourIPvps:8181`





















































