# OLBITX POS hedge coin

## Dependencies

1. boost_1_65_1
2. openssl-1.0.2u
3. qt 5.12

## How to build: Ubuntu 20.04
### Step 1: OpenSSL
Download and build old version of openSSL: openssl-1.0.2u will do.
```bash
apt-get update && apt-get install libcurl4-openssl-dev make perl-modules build-essential
wget https://www.openssl.org/source/old/1.0.2/openssl-1.0.2u.tar.gz
tar xzvf openssl-1.0.2u.tar.gz 
cd openssl-1.0.2u
./config --prefix=/opt/openssl-1.0.2 --openssldir=/opt/openssl-1.0.2 && make && make test 
sudo make install 
```
### Step 2: Boost
``` bash
wget https://boostorg.jfrog.io/artifactory/main/release/1.65.1/source/boost_1_65_1.tar.gz
tar xzvf boost_1_65_1.tar.gz 
cd boost_1_65_1
sudo ./b2 --prefix=/opt/boost-1.65.1 link=static threading=multi variant=release install
```
### Step 3: Qt 5
```bash
apt-get install qt5-default qttools5-dev-tools
```
### Step 4: Other dependencies
```bash
apt-get install git libcurl4-openssl-dev libdb++-dev libdb-dev libminiupnpc-dev libnss-myhostname libqrencode-dev libupnp-dev pax-utils
```
### Step 5: Build the project
```bash
git clone https://github.com/OLBITX/OLBITX.git olbitx
cd olbitx
export OPENSSL_INCLUDE_PATH=/opt/openssl-1.0.2/include
export OPENSSL_LIB_PATH=/opt/openssl-1.0.2/lib
export BOOST_INCLUDE_PATH=/opt/boost-1.65.1/include
export BOOST_LIB_PATH=/opt/boost-1.65.1/lib
qmake OLBITX-qt.pro 
```








