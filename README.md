# rethinkdb on ubuntu 14.04
```
source /etc/lsb-release && echo "deb http://download.rethinkdb.com/apt $DISTRIB_CODENAME main" | sudo tee /etc/apt/sources.list.d/rethinkdb.list
wget -qO- https://download.rethinkdb.com/apt/pubkey.gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get -y install rethinkdb
sudo apt-get -y install build-essential protobuf-compiler python \
                     libprotobuf-dev libcurl4-openssl-dev \
                     libboost-all-dev libncurses5-dev \
                     libjemalloc-dev wget m4
```
```
wget https://download.rethinkdb.com/dist/rethinkdb-2.2.1.tgz
tar xf rethinkdb-2.2.1.tgz
```
```
cd rethinkdb-2.2.1
./configure --allow-fetch
make
sudo make install
```
