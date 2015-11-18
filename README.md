# Install rethinkdb on ubuntu 12.04
```
source /etc/lsb-release && echo "deb http://download.rethinkdb.com/apt $DISTRIB_CODENAME main" | sudo tee /etc/apt/sources.list.d/rethinkdb.list
wget -qO- http://download.rethinkdb.com/apt/pubkey.gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get -y install rethinkdb
```
```
cd /etc/rethinkdb/
sudo cp default.conf.sample instances.d/default.conf
sudo vi instances.d/default.conf
```
```
# bind=127.0.0.1
bind=0.0.0.0
```
```
sudo /etc/init.d/rethinkdb start
```
#### rethinkdb with python
```
sudo apt-get install python-pip
sudo pip install rethinkdb
```
