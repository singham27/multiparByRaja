EC2

Setup EC2 =>

Dashboard => Instance => Launch Instance
ubuntu server 20.04 LTS (HVM), SSD Volume Type(Free tier)

t2 micro (Free tier eligible) => Review and Launch =>
Launch

create new key value and pair => download => launch instance =>
Back On (View Instance) Dashboard => Instance => Select created Instance
Edit Name

select instance => Connect 
Enter username instead of ubuntu = root => connect =>
(there will be open a terminal)


Change Security Settings

Security => 
Security Groups => 
open link like this (sg-050c5f782b859490c(launch-wizard-3)) =>
Edit inbound rules

Add rules =>
Type = http
source = anywhere

Type = https
source = anywhere

Type = Custom TCP
Port range = 3000
source = anywhere

Save rules


#Update ubuntu instance
sudo apt-get update
 
#install nodejs ubuntu
sudo apt-get install curl
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install -y nodejs

To check node is install ?
node -v
npm -v

#install ngnix
sudo apt-get install nginx -y

#nginx version
nginx -v

Go into nginx
cd /var/www/html/
ls

To check nginx is run
Open Public IPv4 Address

cd / back on root

#restart nginx
sudo systemctl restart nginx

Open public IP address there will be welcome to nginx


Go to nginx folder
cd /var/www/html/

Set your node app now:- 

npx create-react-app react-tutorial
Go to your node app created app => 

sudo apt-get install git
git clone giturl

cd react-tutorial
npm run build
npm start


Run on browser =>
your public ip:3000 like this (3.7.65.14:3000)
