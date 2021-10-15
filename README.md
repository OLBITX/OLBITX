# OLBITX POS hedge coin

## Dependencies

1. boost_1_65_1
2. openssl-1.0.2u
3. qt 5.12

## How to build: Ubuntu 20.04
### Step 1
Download and build old version of openSSL: openssl-1.0.2u will do.
```bash
apt-get install php5-curl libcurl4-openssl-dev make
wget https://www.openssl.org/source/old/1.0.2/openssl-1.0.2u.tar.gz
tar xzvf openssl-1.0.2u.tar.gz 
cd openssl-1.0.2u
./config --prefix=/opt/openssl-1.0.2 --openssldir=/opt/openssl-1.0.2 && make && make test 
sudo make install 
```






